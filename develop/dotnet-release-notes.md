---
title: Partner Center .NET SDK release notes
description: Release notes for the latest version of the Partner Center .NET SDK.
ms.date: 09/18/2020
ms.service: partner-dashboard
ms.subservice:  partnercenter-sdk
---

# .NET SDK release notes

The following release notes are available for new versions of [Microsoft Partner Center .NET SDK](https://www.nuget.org/packages/Microsoft.Store.PartnerCenter). You can find [.NET SDK samples](https://github.com/Microsoft/Partner-Center-DotNet-Samples) on GitHub. You can find the [Partner Center .NET API reference](/dotnet/api/?view=partnercenter-dotnet-latest&preserve-view=true) in the .NET API Browser.

## Version 1.17.0

[Microsoft Partner Center .NET SDK](https://www.nuget.org/packages/Microsoft.Store.PartnerCenter/1.17.0) v1.17.0 is now general availability. Updated [GitHub samples](https://github.com/Microsoft/Partner-Center-DotNet-Samples) are also available. The following changes are included in this version:

* Audit Updated - Added new operation types for knowing when the customer approved and terminated DAP
  * [DapAdminRelationshipApproved](https://docs.microsoft.com/en-us/partner-center/develop/auditing-resources)
  * [DapAdminRelationshipTerminated](https://docs.microsoft.com/en-us/partner-center/develop/auditing-resources)

* Audit Updated – Added new resource and operation types for supporting the customer directory role scenario
  * Resource type "[CustomerDirectoryRole](https://docs.microsoft.com/en-us/partner-center/develop/auditing-resources)"
  * Operation types "[AddUserMember](https://docs.microsoft.com/en-us/partner-center/develop/auditing-resources)" and "[RemoveUserMember](https://docs.microsoft.com/en-us/partner-center/develop/auditing-resources)"

* SDK Updates to Customers Account - Support for following API's
  * GET /customers/{customer-tenant-id}/directSignedMicrosoftCustomerAgreementStatus
  * GET /customers/{customer-tenant-id}/qualifications 
  * POST /customers/{customer_id}/qualifications?code={validationCode}

* **Following changes introduced as part of New Commerce which are currently available based on invitation only to partners who are part of the M365/D365 new commerce experience technical preview.** Partners who are not part of New commerce private preview should not notice impacts and should be backward compatible.
  * Catalog Changes:
    * GET /products/{product-id}/skus/{sku-id}
  * Purchase and Manage:
    * GET /customers/{customerId}/subscriptions
    * GET /customers/{customerId}/subscriptions/{subscriptionId}
    * PATCH /customers/{customerId}/subscriptions/{subscriptionId}
    * GET /customers/{customerId}/subscriptions/{subscriptionId}/transitioneligibilities
    * GET /customers/{customerId}/subscriptions/{subscriptionId}/transitions
    * POST /customers/{customerId}/subscriptions/{subscriptionId}/transitions
    
  
## Version 1.16.3

[Microsoft Partner Center .NET SDK](https://www.nuget.org/packages/Microsoft.Store.PartnerCenter/1.16.3) v1.16.3 is now general availability. Updated [GitHub samples](https://github.com/Microsoft/Partner-Center-DotNet-Samples) are also available. The following changes are included in this version:

* SelfServePolicies - new functionality added
  * [GetSelfServePolicies](get-a-self-serve-policy-by-id.md)
  * [GetListOfSelfServicePolicies](get-a-list-of-self-serve-policies.md)
  * [CreateSelfServePolicies](create-a-self-serve-policy.md)
  * [UpdateSelfServePolicies](update-a-self-serve-policy.md)
  * [DeleteSelfServePolicies](delete-a-self-serve-policy.md)

* Customers Company Profile
  * Added [OrganizationRegistrationNumber](create-a-customer.md)

* CustomerBillingProfile.DefaultAddress
  * Added MiddleName

## Version 1.16.2

[Microsoft Partner Center .NET SDK](https://www.nuget.org/packages/Microsoft.Store.PartnerCenter/1.16.2) v1.16.2 is now general availability. Updated [GitHub samples](https://github.com/Microsoft/Partner-Center-DotNet-Samples) are also available. The following changes are included in this version:

* Update supported operation types for Audit Record. The newly added ones are:
  * CreateSelfServePolicy
  * UpdateSelfServePolicy
  * DeleteSelfServePolicy
  * RemovePartnerRelationship
  * DeleteTipCustomer
  * CreateRelatedReferral
  * UpdateRelatedReferral

* Service request creation is now deprecated
* Support topics are now deprecated


## Version 1.16.1

[Microsoft Partner Center .NET SDK](https://www.nuget.org/packages/Microsoft.Store.PartnerCenter/1.16.1) v1.16.1 is now general availability. Updated [GitHub samples](https://github.com/Microsoft/Partner-Center-DotNet-Samples) are also available. The following changes are included in this version:

We have migrated the existing Microsoft Partner Center SDK from .NET Framework to .NET Standard 2.0 platform. This will make the SDK compatible with existing applications using .NET Framework 4.6.1 and above. The SDK will support .NET Core 2.0 and above. Check [.NET implementation support](/dotnet/standard/net-standard) before porting it to existing applications.   


## Version 1.15.3
[Microsoft Partner Center .NET SDK](https://www.nuget.org/packages/Microsoft.Store.PartnerCenter/1.15.3) v1.15.3 is now general availability. Updated REST APIs and [GitHub samples](https://github.com/Microsoft/Partner-Center-DotNet-Samples) are also available. The following changes are included in this version:

* Partner Agreement
  * Added the ability for indirect providers to [verify Microsoft Partner Agreement status of indirect resellers](verify-indirect-reseller-mpa-status.md).
* Products
  * The following two interfaces were incorrectly placed under the Microsoft.Store.PartnerCenter.Products namespace. Now, they are located under the Microsoft.Store.PartnerCenter.Customers.Products namespace.
    * ICustomerProductByReservationScope
    * ICustomerSkuByReservationScope
