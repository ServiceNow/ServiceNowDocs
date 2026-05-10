---
title: Validate subscription, installation, and usage data
description: Validate subscription, installation, and usage data before running a reconciliation for completeness and accuracy of your reports.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Microsoft 365 SaaS License Management success guide, Success Guides, Success portal view in Software Asset Workspace, Software Asset Workspace, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Validate subscription, installation, and usage data

Validate subscription, installation, and usage data before running a reconciliation for completeness and accuracy of your reports.

## Before you begin

Role required: sam\_admin, sam\_user

## Procedure

1.  Validate user subscription data from the Microsoft cloud integration.

    1.  Log in to your ServiceNow instance.

        |Interface|Action|
        |---------|------|
        |Core UI|Navigate to **All** &gt; **Software Asset** &gt; **Discovery** &gt; **Software Subscriptions**.|
        |Software Asset Workspace|Navigate to **Software Asset Workspace** &gt; **License operations** &gt; **User subscription** &gt; **User subscription**.|

    2.  Review the data in the User Subscription table by verifying the number of Microsoft 365 subscription records.

        For more information about personalizing and filtering data, see [Configure user experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_NavigationAndTheUserInterface.md).

        -   If the number of Microsoft 365 subscriptions records isn't accurate, verify that the **SAM - Import M365 User Subscriptions** scheduled job in the SAMP job log \[samp\_job\_log\] has completed successfully to pull the subscriptions.
            -   Confirm that the existing integrations are working properly.
            -   Determine if additional integrations are required for other Microsoft environments.
        -   If the Microsoft 365 records appear accurately, verify the values in the **Display name**, **User principal name**, **Software model**, and **Subscription identifier** fields.

            **Note:** Subscription identifiers uniquely identify SaaS applications. Each identifier is associated with a discovery map and a software model, which normalizes software installations to Microsoft 365 subscriptions from the cloud.

            -   Check if the software model is resolved correctly as per the subscription product definition.
            -   Check if the **User** field on the subscription records is resolved. If it is not resolved, check the email of the user, which must match with the user principal name. You can also match the user name from the user principal with the user\_name on the sys\_user record.
            -   If subscription identifiers are incorrect or empty, manage and resolve the subscription identifiers. For more information, see [Subscription identifiers for SaaS and SSO applications](../concept/subscription-identifiers.md#).
2.  Validate installation and usage data from inventory tools.

    **Note:**

    Establish a validation scope, as a proxy for full inventory validation, with a sample set of devices known to have Microsoft 365 product installations. The sample size must be no larger than necessary to validate installation data from the integration. If there are multiple integrations, compile separate sample sets for each integration.

    1.  Navigate to the Software Installations \[cmdb\_sam\_sw\_install\] table, which lists the Microsoft 365 installations.

<table id="table_obb_xkl_cxb"><thead><tr><th>

Interface

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Core UI

</td><td>

In the application filter navigator, search and select **cmdb\_sam\_sw\_install.list**.

</td></tr><tr><td>

Software Asset Workspace

</td><td>

1.  Navigate to **Software Asset Workspace** &gt; **License operations** &gt; **Discovery** &gt; **Discovery models**.
2.  Select a discovery model name.
3.  Select the **Software Installations** tab.


</td></tr></tbody>
</table>    2.  Locate the **Installed on** column field and filter to one or more devices that are part of the validation scope.

        1.  Filter the list further to see all the Microsoft 365 product installations for devices.
            -   If the number of Microsoft 365 records is lower than expected, do the following:
                -   Confirm that the existing discovery or inventory tools are working properly.
                -   Determine if additional inventory tool integrations are required.
            -   If the number of Microsoft 365 records is higher than expected, confirm that the existing discovery or inventory tools are working properly. If the inventory tool integrations are working properly, then the high number of records might indicate potential savings chances.
        2.  Verify computer records for devices within the validation scope.
            1.  Select the hyper-linked device name in the **Installed on** column field.
            2.  Review the data values such as **Name**, **Assigned to**, and **Operating System**.
                -   If the number of computer device records is lower than expected, do the following:
                    -   Confirm that the existing discovery or inventory tools are working properly.
                    -   Determine if additional inventory tool integrations are required for missing data.
                -   If the number of computer device records is higher than expected, confirm that the existing discovery or inventory tools are working properly. If the inventory tool integrations are working properly, then the high number of records might indicate potential savings chances.

## What to do next

[Import Microsoft 365 subscription entitlements](imp-m365-ent.md)

