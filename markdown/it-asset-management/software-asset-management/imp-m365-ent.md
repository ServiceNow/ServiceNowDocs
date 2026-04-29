---
title: Import Microsoft 365 subscription entitlements
description: Import Microsoft 365 subscription entitlements into the ServiceNow Software Asset Management application.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Microsoft 365 SaaS License Management success guide, Success Guides, Success portal view in Software Asset Workspace, Software Asset Workspace, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Import Microsoft 365 subscription entitlements

Import Microsoft 365 subscription entitlements into the ServiceNow Software Asset Management application.

## Before you begin

Role required: sam\_admin or sam\_user

## Procedure

1.  Gather as many Microsoft 365 subscription entitlements as possible.

2.  Fill out the entitlement template and import into the ServiceNow Software Asset Management application.

    1.  Open the **Import Software Entitlements** page.

<table id="table_pr1_2fr_cxb"><thead><tr><th>

Interface

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Core UI

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **Licensing** &gt; **Import Entitlements**.
2.  Select **Download Template File \(.xlsx\)**.


</td></tr><tr><td>

Software Asset Workspace

</td><td>

1.  Navigate to **Software Asset Workspace** &gt; **License operations**.
2.  Select **Create entitlement**.
3.  In the Create new entitlement dialog box, select **Import multiple entitlements** from an Excel file.
4.  Select **Next**.
5.  In the Create New Entitlement Import page, select **Download template** to download a spreadsheet template \(.xlsx\).


</td></tr></tbody>
</table>    2.  Open the import template and review the **Directions** tab.

    3.  Populate the import template with data from your gathered entitlements.

        For more information about the additional details on the import template, see [ServiceNow SAM Entitlement Import User Guide](https://www.servicenow.com/community/sam-blog/servicenow-sam-entitlement-import-user-guide/ba-p/2284797).

    4.  Use the following values on the template for Microsoft 365 entitlements:

        -   **Metric group**: Microsoft
        -   **License metric**: User Subscription
3.  After the template is populated with entitlement data, import the template to the Software Asset Management application.

    1.  Import the template to the Software Asset Management application.

<table id="table_kjv_3lr_cxb"><thead><tr><th>

Interface

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Core UI

</td><td>

Navigate to **All** &gt; **Software Asset** &gt; **Licensing** &gt; **Import Entitlements**.

</td></tr><tr><td>

Software Asset Workspace

</td><td>

1.  Navigate to **Software Asset Workspace** &gt; **License operations**.
2.  Select **Create entitlement**.
3.  In the Create new entitlement dialog box, select **Import multiple entitlements** from an Excel file.
4.  Select **Next**.


</td></tr></tbody>
</table>    2.  Import the completed template through **Browse files** or drag it.

    3.  Verify the imported software rights and resolve the import errors, if any.

4.  Review the imported entitlements.

    1.  Confirm that the software entitlements are linked to the correct software models.

        |Interface|Action|
        |---------|------|
        |Core UI|Navigate to **All** &gt; **Software Asset** &gt; **Licensing** &gt; **Software Entitlements**.|
        |Software Asset Workspace|Navigate to **Software Asset Workspace** &gt; **License operations** &gt; **Licensing** &gt; **Software entitlements**.|

    2.  Select the display name for a software entitlement record.

    3.  On the Software Entitlements form, select the preview icon ![](../image/preview-icon.png) next to the **Software model** field.

    4.  Confirm that the discovery map and suite components match the values on the template for Microsoft 365 entitlements.

        If the discovery map doesn't match, add or edit directly on the software model form and select **Update**.

        **Tip:** After the entitlements are imported, you might need additional subscriptions purchases during the true-up process with Microsoft. For more information, see. [Creating reserve entitlements for Microsoft online services](../concept/creating-0365-reserve-entitlements.md).


## What to do next

[Reconcile for compliance](recon-for-comp-sg.md)

