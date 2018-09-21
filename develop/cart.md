---
title: Cart
description: A partner places an order when a customer wants to buy a subscription from a list of offers.
ms.date: 03/16/2018
ms.localizationpriority: medium
---

# Cart


**Applies To**

-   Partner Center


A partner places an order when a customer wants to buy a subscription from a list of offers.


## <span id="cart"></span><span id="CART"></span>Cart

Describes a cart.

| Property              | Type             | Description                                                                                            |
|-----------------------|------------------|--------------------------------------------------------------------------------------------------------|
| id                    | string           | A cart identifier that is supplied upon successful creation of the cart.                               |
| creationTimeStamp     | DateTime         | The date the cart was created, in date-time format. Applied upon successful creation of the cart.      |
| lastModifiedTimeStamp | DateTime         | The date the cart was last updated, in date-time format. Applied upon successful creation of the cart. |
| expirationTimeStamp   | DateTime         | The date the cart will expire, in date-time format. Applied upon successful creation of cart.          |
| lastModifiedUser      | string           | The user who last updated the cart. Applied upon successful creation of cart.                          |
| lineItems             | Array of objects | An Array of [CartLineItem](#cart-line-item) resources.                                                 |



## <span id="cartLineItem"></span><span id="cartlineitem"></span><span id="CARTLINEITEM"></span>CartLineItem


Represents one item contained in a cart.

| Property             | Type                        | Description                                                                           |
|----------------------|-----------------------------|---------------------------------------------------------------------------------------|
| id                   | string                      | A unique identifier for a cart line item. Applied upon successful creation of cart.   |
| catalogId            | string                      | The catalog item identifier.                                                          |
| friendlyName         | string                      | Optional. The friendly name for the item defined by the partner to help disambiguate. |
| quantity             | int                         | The number of licenses or instances.                                                  |
| currencyCode         | string                      | The currency code.                                                                    |
| billingCycle         | Object                      | The type of billing cycle set for the current period.                                 |
| participants         | List of Object String pairs | A collection of PartnerId on Record (MPNID) on the purchase.                                         |
| provisioningContext  | Dictionary<string, string>  | A context used for provisioning of offer.                                             |
| orderGroup           | string                      | A group to indicate which items can be placed together.                               |
| error                | Object                      | Applied after cart is created in case of an error.                                    |

 

## <span id="cartError"></span><span id="carterror"></span><span id="CARTERROR"></span>CartError


Represents an error that occurs after a cart is created.

| Property         | Type                                   | Description                                                                                   |
|------------------|----------------------------------------|-----------------------------------------------------------------------------------------------|
| errorCode        | [CartErrorCode](cart.md#carterrorcode) | The type of cart error.                                                                       |
| errorDescription | string                                 | The error description, including any notes about supported values, default values, or limits. |



## <span id="cartErrorCode"></span><span id="carterrorcode"></span><span id="CARTERRORCODE"></span>CartErrorCode


An [Enum](https://docs.microsoft.com/en-us/dotnet/api/system.enum) with values that indicate a type of cart error.

| Value                                | Position | Description                                             |
|--------------------------------------|----------|---------------------------------------------------------|
| Unknown                              | 0        | Default value.                                          |
| CurrencyIsNotSupported               | 10000    | The currency is not supported for the specified market. |
| CatalogItemIdIsNotValid              | 10001    | The catalog item ID is not valid.                       |
| QuotaNotAvailable                    | 10002    | There is not enough quota available.                    |
| InventoryNotAvailable                | 10003    | The inventory is not available for the selected offer.  |
| ParticipantsIsNotSupportedForPartner | 10004    | Setting participants is not supported for this partner. |
| UnableToProcessCartLineItem          | 10006    | Unable to process the cart line item.                   |
| SubscriptionIsNotValid               | 10007    | The subscription is not valid.                          |
| SubscriptionIsNotEnabledForRI        | 10008    | The subscription is not enabled for Azure reservations. |
| SandboxLimitExceeded                 | 10009    | The sandbox limit has been exceeded.                    |



## <span id="cartCheckoutResult"></span><span id="cartcheckoutresult"></span><span id="CARTCHECKOUTRESULT"></span>CartCheckoutResult


Represents the result of a cart checkout.

| Property    | Type                                              | Description                     |
|-------------|---------------------------------------------------|---------------------------------|
| orders      | List of [Order](orders.md#order) objects.         | The collection of orders.       |
| orderErrors | List of [OrderError](cart.md#ordererror) objects. | The collection of order errors. |
 


## <span id="orderError"></span><span id="ordererror"></span><span id="ORDERERROR"></span>OrderError


Represents an error that occurs during a cart checkout when an order is created.

| Property     | Type   | Description                                     |
|--------------|--------|-------------------------------------------------|
| orderGroupId | string | The order group ID of the order with the error. |
| code         | int    | The error code.                                 |
| description  | string | The description of the error.                   |

