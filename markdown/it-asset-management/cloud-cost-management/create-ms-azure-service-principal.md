---
title: Create a Microsoft Azure service principal
description: Give Cloud Cost Management access to Microsoft Azure billing and usage data by creating a Microsoft Azure service principal.
locale: en-US
release: xanadu
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Set up access to Microsoft Azure billing and usage data, Configure Cloud Cost Management for Microsoft Azure, Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Create a Microsoft Azure service principal

Give Cloud Cost Management access to Microsoft Azure billing and usage data by creating a Microsoft Azure service principal.

## Before you begin

Microsoft Azure Role required: Azure Cloud admin

## About this task

Cloud Cost Management supports Microsoft Azure billing and cost usage data for two types of billing agreements: Enterprise Agreement \(EA\) and Microsoft Customer Agreement \(MCA\). There are specific roles that you must assign to the service principal depending on your billing agreement type. For more information on EA and MCA agreement types, see [Billing information for Microsoft Azure](https://learn.microsoft.com/en-us/azure/cost-management-billing/manage/manage-billing-access).

## Procedure

1.  From a web browser, open the [App Registrations page](https://portal.azure.com/?Microsoft_AAD_RegisteredApps=true#view/Microsoft_AAD_RegisteredApps/ApplicationsListBlade) of the Microsoft Entra ID portal.

2.  Log in using your global administrator credentials.

3.  In the **Name** field of the Register an application form, enter a name for the application.

4.  In the **Supported account types** field, select **Accounts in any organizational directory \(Any Microsoft Entra ID – Single tenant\)**.

5.  Select **Register**.

    The application is registered and you’re redirected to the Overview page of the new application.

6.  On the Overview page, copy the values in the **Application \(client\) ID** and **Directory \(tenant\) ID** fields.

    Save them in a secure location for later use.

7.  Generate a Client secret for your application.

    1.  From the side navigation menu, navigate to **Manage** &gt; **Certificates &amp; secrets**.

    2.  In the Client secrets section, generate a client secret for the application by selecting **New client secret**.

    3.  In the dialog box, fill in the fields.

<table id="table_oqr_qkn_sfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Description

</td><td>

Description of the client secret.

</td></tr><tr><td>

Expires

</td><td>

Expiration of the client secret.**Note:** Your organization might apply policies to restrict client secret durability. Select an appropriate expiration period.

</td></tr></tbody>
</table>    4.  Select **Add**.

    5.  Copy the client secret that is generated and save at a secure location for later use.

8.  Get **Subscription ID** to enable the service principal to work with various Azure subscriptions.

    1.  Navigate to **Subscriptions**.

    2.  Select the **Subscription ID** to which the service principal needs access.

    3.  Copy the **Subscription ID** from the Subscription Overview page.

9.  Assign access roles and permissions to the service principal depending on your billing agreement type.

    Refer to the table for required roles and permissions for the service principal.

<table id="table_xcg_xln_sfc"><thead><tr><th>

Billing agreement type

</th><th>

Role required

</th><th>

Permissions

</th></tr></thead><tbody><tr><td>

Enterprise Agreement \(EA\)

</td><td>

-   Enrollment Reader
-   Storage Blob Data Reader


</td><td rowspan="2">

These permissions are required for the service principal for both EA and MCA.

 -   Microsoft.Compute/virtualMachines/instanceView/read
-   Microsoft.Compute/virtualMachines/deallocate/action
-   Microsoft.Compute/virtualMachines/start/action
-   Microsoft.Compute/virtualMachines/delete
-   Microsoft.Compute/virtualMachines/write
-   Microsoft.Compute/virtualMachines/read
-   Microsoft.Compute/locations/usages/read
-   Microsoft.Advisor/recommendations/read
-   Microsoft.Advisor/generateRecommendations/read
-   Microsoft.Advisor/generateRecommendations/action
-   Microsoft.Compute/disks/delete
-   Microsoft.Compute/disks/read
-   Microsoft.CostManagement/forecast/read
-   Microsoft.Compute/locations/diskOperations/read
-   Microsoft.Insights/Metrics/Read
-   Microsoft.Compute/locations/operations/read
-   Microsoft.Sql
-   Microsoft.DBforMariaDB
-   Microsoft.DBforMySQL


</td></tr><tr><td>

Microsoft Customer Agreement \(MCA\)

</td><td>

-   Billing Account Reader
-   Both Billing Profile Reader and Billing Reader
-   Storage Blob Data Reader


</td></tr></tbody>
</table>
## What to do next

[Create a record of Microsoft Azure credentials in Cloud Cost Management](create-azure-credential-record-ccm.md)

**Related topics**  


[Add the Enrollment Reader role to the Microsoft Azure service principal](add-enrollment-reader-ms-azure.md)

[Add the Billing Profile Reader role to the Microsoft Azure service principal](add-billing-profile-reader-azure.md)

