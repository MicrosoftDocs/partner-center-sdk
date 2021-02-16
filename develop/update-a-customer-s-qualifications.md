---
title: Update a customer's qualifications
description: Updates a customer's qualifications asynchronously, including the address associated with the profile.
ms.date: 02/16/2021
ms.service: partner-dashboard
author: jobiesel
ms.author: jobiesel
---

# Update a customer's qualifications asynchronously

**Applies To**

- Partner Center

Updates a customer's qualifications asynchronously.

A partner can update a customer's qualifications asynchronously to be "Education" or "GovernmentCommunityCloud". Other values, "None" and "Nonprofit", cannot be set.

## Prerequisites

- Credentials as described in [Partner Center authentication](partner-center-authentication.md). This scenario supports authentication with App+User credentials only.

- A customer ID (`customer-tenant-id`). If you don't know the customer's ID, you can look it up in the Partner Center [dashboard](https://partner.microsoft.com/dashboard). Select **CSP** from the Partner Center menu, followed by **Customers**. Select the customer from the customer list, then select **Account**. On the customer's Account page, look for the **Microsoft ID** in the **Customer Account Info** section. The Microsoft ID is the same as the customer ID  (`customer-tenant-id`).

## REST request

### Request syntax

| Method  | Request URI                                                                                             |
|---------|---------------------------------------------------------------------------------------------------------|
| **POST** | [*{baseURL}*](partner-center-rest-urls.md)/v1/customers/{customer_id}/qualifications?code={validationCode} HTTP/1.1 |

### URI parameter

Use the following query parameter to update the qualification.

| Name                   | Type | Required | Description                                                                                                                                            |
|------------------------|------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **customer-tenant-id** | GUID | Yes      | The value is a GUID formatted **customer-tenant-id** that allows the reseller to filter the results for a given customer that belongs to the reseller. |
| **validationCode**     | int  | No       | Only needed for Government Community Cloud.                                                                                                            |

### Request headers

For more information, see [Partner Center REST headers](headers.md).

### Request body

This table describes the qualification object in the request body.

Property | Type | Required | Description
-------- | ---- | -------- | -----------
Qualification | string | Yes | The string value from the [**CustomerQualification**](/dotnet/api/microsoft.store.partnercenter.models.customers.customerqualification) enum.
---

### Request example

```http
POST https://api.partnercenter.microsoft.com/v1/customers/<customer-tenant-id>/qualifications?code=<validation-code> HTTP/1.1
Accept: application/json
Content-Type: application/json
MS-CorrelationId: 7d2456fd-2d79-46d0-9f8e-5d7ecd5f8745
MS-RequestId: 037db222-6d8e-4d7f-ba78-df3dca33fb68

{
    "Qualification": "Education"
}

```

## REST response

If successful, this method returns a qualifications object in the response body. Below is an example of the **POST** call on a customer (with a previous qualification of **None**) with the **Education** qualification.

### Response success and error codes

Each response comes with an HTTP status code that indicates success or failure and additional debugging information. Use a network trace tool to read this code, error type, and additional parameters. For the full list, see [Error Codes](error-codes.md).

### Response example

```http
HTTP/1.1 201 CREATED
Content-Length: 29
Content-Type: application/json
MS-CorrelationId: 7d2456fd-2d79-46d0-9f8e-5d7ecd5f8745
MS-RequestId: 037db222-6d8e-4d7f-ba78-df3dca33fb68
{
    "qualification": "Education",
    "vettingStatus": "InReview",
    "vettingCreateDate": "2020-12-04T20:54:24Z" // UTC
}
```

## Related articles

- [Get a customer's qualifications](get-a-customer-s-qualifications.md)
- [Get a partner's validation codes](get-a-partner-s-validation-codes.md)