---
title: Permissions required for Azure Service Principal
description: This table provides the permissions needed to create, close or cancel an Azure subscription, download billing details, and tag subscriptions.
locale: en-US
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cloud Account Management reference, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Permissions required for Azure Service Principal

This table provides the permissions needed to create, close or cancel an Azure subscription, download billing details, and tag subscriptions.

<table id="table_qmn_lz3_s2c"><thead><tr><th>

Role

</th><th>

Action

</th><th>

Role definition ID

</th></tr></thead><tbody><tr><td>

EnrollmentReader

</td><td>

Enrollment readers can view data at the enrollment, department, and account scopes. This data includes charges for all subscriptions under these scopes, even across tenants, and displays the AzurePrepayment \(previously called monetary commitment\) balance associated with the enrollment.

</td><td>

24f8edb6-1668-4659-b5e2-40bb5f3a7d7e

</td></tr><tr><td>

DepartmentReader

</td><td>

Download the usage details for the department you administer. You can also view the usage and charges associated with your department.

</td><td>

db609904-a47f-4794-9be8-9bd86fbffd8a

</td></tr><tr><td>

Microsoft.Billing/billingAccounts/read

</td><td>

Read the list of billing accounts.

</td><td>

 

</td></tr><tr><td>

Microsoft.Management/managementGroups/subscriptions/write

 Microsoft.Management/managementGroups/write

</td><td>

Move subscription to the appropriate location once created

</td><td>

 

</td></tr><tr><td>

Microsoft.Resources/tags/write

</td><td>

Add tags to the subscription.

</td><td>

 

</td></tr><tr><td>

Microsoft.Billing/billingAccounts/billingSubscriptions/cancel/write

</td><td>

Close or cancel a subscription.

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Account Management reference](cam-reference.md)

