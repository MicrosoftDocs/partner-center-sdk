---
title: Self Serve Policy resources
description: A partner sets self serve policies for a customer.
ms.date: 04/13/20200
ms.service: partner-dashboard
ms.subservice:  partnercenter-sdk
ms.localizationpriority: medium
---

# SelfServePolicy resource

Applies to:

- Partner Center

A partner sets self serve policies for a customer.

## SelfServePolicy

Describes a cart.

| Property              | Type             | Description                                                                                            |
|-----------------------|------------------|--------------------------------------------------------------------------------------------------------|
| id                    | string           | A self serve policy identifier that is supplied upon successful creation of the self serve policy.     |
| SelfServeEntity       | SelfServeEntity  | The self serve entity that is being granted access.                                                     |
| Grantor               | Grantor          | The grantor that is granting access.                                                                    |
| Permissions           | Array of Permission| An Array of [Permission](#permission) resources.                                                                     |

## SelfServeEntity

Represents the entity being granted permissions.

| Property             | Type|Description|
|----------------------|----------------------------------|--------------------------------------------------------------------------------------------|
| SelfServeEntityType  | string                           | The entity being granted access, accepted values: Customer.                                 |
| TenantID             | string                           | The tenant identifier of the entity being granted access.                                   |

## Grantor

Represents the grantor granting the permissions.

| Property             | Type|Description|
|----------------------|----------------------------------|--------------------------------------------------------------------------------------------|
| GrantorType          | string                           | The grantor granting access, accepted values: BillToPartner.                               |
| TenantID             | string                           | The tenant identifier of the entity granting access.                                       |


## Permission

Represents a permission in the self serve policy.

| Property             | Type|Description|
|----------------------|----------------------------------|--------------------------------------------------------------------------------------------|
| Resource             | string                           | The resource access is being granted too: AzureReservedInstances.                          |
| Action               | string                           | The action access is being granted for: Purchase                                           |
