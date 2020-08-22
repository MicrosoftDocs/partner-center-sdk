---
title: Check inventory
description: Check the inventory for a specific set of catalog items.
ms.date: 05/22/2019
ms.service: partner-dashboard
ms.subservice:  partnercenter-sdk
---

# Check inventory

**Applies to:**

- Partner Center

How to check the inventory for a specific set of catalog items.

## Prerequisites

- Credentials as described in [Partner Center authentication](partner-center-authentication.md). This scenario supports authentication with both standalone App and App+User credentials.

- One or more product IDs. Optionally, SKU IDs can also be specified.

- Any additional context needed for verifying the inventory of the SKU(s) referenced by the provided product/SKU ID(s). These requirements may vary by type of product/SKU and can be determined from the [SKU's](product-resources.md#sku) **InventoryVariables** property.

## C\#

To check the inventory, build an [InventoryCheckRequest](product-resources.md#inventorycheckrequest) object using an [InventoryItem](product-resources.md#inventoryitem) object for each item to be checked. Then, use an **IAggregatePartner.Extensions** accessor, scope it down to **Product** and then select the country using the **ByCountry()** method. Finally, call the **CheckInventory()** method with your **InventoryCheckRequest** object.

``` csharp
IAggregatePartner partnerOperations;
string customerId;
string subscriptionId;
string countryCode;
string productId;

// Build the inventory check request details object.
var inventoryCheckRequest = new InventoryCheckRequest()
{
    TargetItems = new InventoryItem[]{ new InventoryItem { ProductId = productId } },
    InventoryContext = new Dictionary<string, string>()
    {
      { "customerId", customerId },
      { "azureSubscriptionId", subscriptionId }
      { "armRegionName", armRegionName }
    }
};

// Get the inventory results.
var inventoryResults = partnerOperations.Extensions.Product.ByCountry(countryCode).CheckInventory(inventoryCheckRequest);
```

## REST request

### Request syntax

| Method   | Request URI                                                                                                                              |
|----------|------------------------------------------------------------------------------------------------------------------------------------------|
| **POST** | [*{baseURL}*](partner-center-rest-urls.md)/v1/extensions/product/checkInventory?country={country-code} HTTP/1.1                        |

### URI parameter

Use the following query parameter to check the inventory.

| Name                   | Type     | Required | Description                                                     |
|------------------------|----------|----------|-----------------------------------------------------------------|
| country-code           | string   | Yes      | A country/region ID.                                            |

### Request headers

For more information, see [Partner Center REST headers](headers.md).

### Request body

The inventory request details, consisting of an [InventoryCheckRequest](product-resources.md#inventorycheckrequest) resource containing one or more [InventoryItem](product-resources.md#inventoryitem) resources.

### Request example

```http
POST https://api.partnercenter.microsoft.com/v1/extensions/product/checkinventory?country=US HTTP/1.1
Authorization: Bearer <token>
Accept: application/json
MS-RequestId: d1b1981a-e088-4610-870a-eebec96d6bcd
MS-CorrelationId: 4acb26a1-3536-4081-bc7d-092869a4961a
X-Locale: en-US
MS-PartnerCenter-Client: Partner Center .NET SDK
Content-Type: application/json

{"TargetItems":[{"ProductId":"DZH318Z0BQ3P"}],"InventoryContext":{"customerId":"d6bf25b7-e0a8-4f2d-a31b-97b55cfc774d","azureSubscriptionId":"3A231FBE-37FE-4410-93FD-730D3D5D4C75","armRegionName":"Europe"}}
```

## REST response

If successful, the response body contains a collection of [InventoryItem](product-resources.md#inventoryitem) objects populated with the restriction details, if any apply.

>[!NOTE]
>If an input InventoryItem represents an item that could not be found in the catalog, it will not be included in the output collection.

### Response success and error codes

Each response comes with an HTTP status code that indicates success or failure and additional debugging information. Use a network trace tool to read this code, error type, and additional parameters. For the full list, see [Partner Center error codes](error-codes.md).

### Response example

```http
HTTP/1.1 200 OK
Content-Length: 1021
Content-Type: application/json; charset=utf-8
MS-CorrelationId: 4acb26a1-3536-4081-bc7d-092869a4961a
MS-RequestId: d1b1981a-e088-4610-870a-eebec96d6bcd
X-Locale: en-US
[
    {
        "productId": "DZH318Z0BQ3P",
        "skuId": "0039",
        "isRestricted": true,
        "restrictions": [
            {
                "reasonCode": "NotAvailableForSubscription",
                "description": "Restriction identified of type 'Location' with values 'japanwest'.",
                "properties": {
                    "type": "Location",
                    "values": "japanwest"
                }
            }
        ]
    },
    {
        "productId": "DZH318Z0BQ3P",
        "skuId": "0038",
        "isRestricted": true,
        "restrictions": [
            {
                "reasonCode": "NotAvailableForSubscription",
                "description": "Restriction identified of type 'Location' with values 'japanwest'.",
                "properties": {
                    "type": "Location",
                    "values": "japanwest"
                }
            }
        ]
    },
    {
        "productId": "DZH318Z0BQ3P",
        "skuId": "000S",
        "isRestricted": false,
        "restrictions": []
    },
    {
        "productId": "DZH318Z0BQ3P",
        "skuId": "0011",
        "isRestricted": false,
        "restrictions": []
    }
]
```