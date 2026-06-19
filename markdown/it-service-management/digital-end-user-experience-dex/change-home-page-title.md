---
title: Customize Desktop Assistant home page
description: Modify the Desktop Assistant home page as required.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/change-home-page-title.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up Desktop Assistant, Configure, Digital End-User Experience, IT Service Management]
---

# Customize Desktop Assistant home page

Modify the Desktop Assistant home page as required.

## Before you begin

Confirm that the DEX Desktop Assistant \[sn\_dex\_desktop\] application has been installed. For more information, see [Install Application and Device Health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/install-app-device-health.md) and [Download and install Desktop Assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/download-desktop-experience.md).

Role required: sn\_dex\_desktop.admin

## Procedure

1.  Navigate to **All** &gt; **Desktop Assistant** &gt; **Configuration** &gt; **Application**.

    \[Omitted image "dex-da-home-page-form.png"\] Alt text: The Desktop Assistant page that provides options to modify your home page title or brief description, as well as activate notifications and the chat icon.

2.  On the Desktop Assistant form, edit the required fields.

<table id="table_ufz_4j2_dxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Title of the home page.

</td></tr><tr><td>

Description

</td><td>

Brief overview of the content and purpose of the product.

</td></tr><tr><td>

Employee Center URL

</td><td>

URL to the Employee Center where employees can access important resources, information, and tools related to their work.

</td></tr><tr><td>

Notifications enabled

</td><td>

Option to enable or disable the notification bell icon.

</td></tr><tr><td>

Theme

</td><td>

Option to apply theme to the Desktop Assistant application. The default theme is Employee Center \(EC\) Theme.You can customize themes by modifying specific CSS variables. For more information, see [Customize themes for Desktop Assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/customize-da-theme.md).

</td></tr><tr><td>

Virtual Agent enabled

</td><td>

Option to enable or disable the chat icon.

</td></tr></tbody>
</table>3.  Customize the logo for the Desktop Assistant home page.

    **Note:**

    -   By default, the ServiceNow logo is applied. The base system logo measures 253  px by 73  px.
    -   When uploading a custom company logo, make sure it does not exceed the maximum supported size of 10 rem by 5 rem \(approximately 160 px by 80 px\).
    1.  In the Logo field, select **Update**.

    2.  Select **Choose File** and select an image from your system.

    3.  Select **OK**.

    4.  To delete the logo, select **Delete** in the Logo field.

4.  Select **Update**.


