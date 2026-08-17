---
title: Add Telecom Customer 360 to any record page
description: Follow this procedure to add the Customer 360 to any record page and enable recommended actions and diagnostics in the contextual side panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/c360-add-page-collection.html
release: australia
topic_type: task
last_updated: "2026-07-26"
reading_time_minutes: 3
breadcrumb: [Add the Customer 360 tab to a record page, Configure, Telecommunications Customer 360, Telecommunications, Media, and Technology \(TMT\)]
---

# Add Telecom Customer 360 to any record page

Follow this procedure to add the Customer 360 to any record page and enable recommended actions and diagnostics in the contextual side panel.

## Before you begin

Role required: `sn_telecom_c360.admin`

## About this task

This variant provides two page collections that can be added to any record page:

-   **Telecom Customer 360 Main Tabs**: Adds a Customer 360 tab to the main tab area of the record page.
-   **Telecom Customer 360 Contextual Side Panel Tabs**: Adds Recommended Actions and Run Diagnostics icons to the contextual side panel.

**Note:**

-   The **Telecom Customer 360** tab and contextual side panel icons are visible only to users with the `sn_telecom_c360.user` role.
-   The Recommended Actions and Run Diagnostics options are displayed only if the record context is a consumer or a customer account.

## Procedure

1.  Add the **Telecom Customer 360 Main Tabs** page collection to the main tab area.

    1.  In UI Builder, open the record page where you want to add the page collection.

    2.  In the content tree, select **Main Tab** and select **Add**.

    3.  Select **Add a page collection** and select **Next**.

    4.  Select **Telecom Customer 360 Main Tabs** and select **Continue**.

        When this page collection is added, the [Telecom Customer 360](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/c360-component.md) component and the Telecom Customer 360 Tabs Controller are added.

2.  Add the **Setup Customer360 Context** data resource to the record page.

    This data resource identifies whether the record is associated with a consumer or an account and provides the table name and sysID for the Customer 360 component. For details on configuring this data resource, see [Add the Setup Customer360 Context data resource](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/c360-add-data-resource.md).

3.  Locate the **Telecom Customer 360 Tabs Controller** and associate the table and sysID to the output of the **Setup Customer360 Context** data resource.

4.  Add the **Telecom Customer 360 contextual side panel tabs** page collection to the tab sidebar.

    1.  In the content tree, select **Tab Sidebar** and select **Add**.

    2.  Select **Add a page collection** and select **Next**.

    3.  Select **Telecom Customer 360 contextual side panel tabs** and select **Continue**.

    4.  Locate the **Telecom Customer 360 Data Controller** and associate the following inputs with the outputs of the **Telecom Customer 360 Tabs Controller**:

        -   AllProductsList
        -   ConfigSettingID
        -   productTable

## Result

You will see the **Customer 360** tab on the record page to which the page collections have been added. When you navigate to this tab, the Recommended Actions and Run Diagnostics options appear in the contextual side panel.

**Parent Topic:**[Add the Customer 360 tab to a record page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/c360-configure-c360.md)

**Related topics**  


[Telecommunications Customer 360 component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/c360-component.md)

[Add the Telecom Customer 360 component to a record page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/c360-add-component.md)

[Add the Setup Customer360 Context data resource](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/c360-add-data-resource.md)

