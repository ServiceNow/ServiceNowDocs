---
title: Create a manifest file
description: Create and download a manifest file with the configurations that you want to enable for the ServiceNow Add-in for Microsoft 365.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure, ServiceNow Add-in for Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Create a manifest file

Create and download a manifest file with the configurations that you want to enable for the ServiceNow Add-in for Microsoft 365.

## Before you begin

Role required: sn\_outlook\_addin.outlook\_addin\_setup, sn\_hr\_sp.admin, sn\_hr\_sp.esc\_admin

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Add-Ins for Office** &gt; **Office Add-In Manifests**.

2.  On the Office Manifests list, select **New**.

3.  On the form, fill in the fields.

    For a description of the field values, see [Office Manifest form](../reference/office-manifest-form.md).

    You can also configure single sign-on \(SSO\) for your add-in. For more information, see [Configure single sign-on for ServiceNow Add-in for Microsoft 365](configure-sso-sn-addin-ms365.md).

4.  Save the record.

5.  On the Office Control related list, select **New**.

6.  On the form, fill in the fields.

    For a description of the field values, see [Office Control form](../reference/office-control-form.md).

    **Note:** For Office Controls of the type Menu, you can create menu items by using the related list in the Office Control record.

7.  On the Office Controls related list, set the Order and Domain for the records.

8.  On the Office Manifest record, select **Activate**.

    This step is applicable if you did not select the **Active** field while creating the record.


## Result

The manifest is configured and activated for the ServiceNow Add-in for Microsoft 365. You can download the manifest file by selecting **Download Manifest** on the Office Manifest record.

## What to do next

-   [Configure single sign-on for ServiceNow Add-in for Microsoft 365](configure-sso-sn-addin-ms365.md)
-   [Upload a manifest to the Microsoft admin center](upload-manifest-ms-admin-center.md)

**Parent Topic:**[Configuring ServiceNow Add-in for Microsoft 365](../concept/configuring-sn-addin-for-ms365.md)

