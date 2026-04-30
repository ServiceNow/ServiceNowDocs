---
title: Configure the Info tab in the DPM Admin Center
description: Configure the general information fields for your solutions in the DPM Admin Center. Your configuration determines how the fields are displayed in the General info section of the Info tab in the DPM Workspace.
locale: en-US
release: xanadu
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Use the Admin Center in Digital Portfolio Management, Configuring Digital Portfolio Management, Digital Portfolio Management, IT Service Management]
---

# Configure the Info tab in the DPM Admin Center

Configure the general information fields for your solutions in the DPM Admin Center. Your configuration determines how the fields are displayed in the **General info** section of the **Info** tab in the DPM Workspace.

## Before you begin

Role required: sn\_dpm.dpm\_admin

## About this task

Each solution has an **Info** tab that displays general information about the solution. For example, for a service, the **Info** tab **General info** section may display the associated service portfolio, the taxonomy node, the service classification \(technical or business\), the phase, the status, and more. You can configure the **General info** section to best suit the needs of your organization. The DPM Admin Center enables you to configure the **General info** fields for the following solutions:

-   Services and service offerings \(both business and technical\)
-   Business applications
-   Application services
-   Service portfolios and taxonomies
-   Enterprise portfolios and taxonomies

## Procedure

1.  Navigate to **All** &gt; **Digital Portfolio Management** &gt; **DPM Admin Center** &gt; **Settings**.

2.  Select the **Info** tab for the solution that you want to configure the **General info** fields.

    **Note:** For the **Portfolio properties** option, select **General info**.

3.  Select **Configure**.

    You must be in the correct application scope to edit the record. If you're in a different scope, then a text banner displays for you to select a link to edit the record.

4.  Review the field names in the **Secondary Values** tab.

    The field names represent the information displayed in the **General info** section of the **Info** tab in the DPM Workspace.

5.  Configure the fields from the list view.

    You can do some minor configuring in the list view to affect the **General info** display in a solution's **Info** tab.

    -   You can set the **Active** value to true or false. After a field is set to false, it doesn't display in the **General info** section.
    -   You can change the order in which the active fields are displayed in the **General info** section.
6.  Configure the fields individually.

    -   Select a field to configure. You must be in the correct application scope to edit the record. If you're in a different scope, then a text banner displays for you to select a link to edit the record.
    -   Review or change the information.

        |Field|Description|Editable|
        |-----|-----------|--------|
        |Table|The table name for the item.|No|
        |Field|The field name for the item that displays on the **General info** section of the DPM Workspace.|Yes|
        |Order|The order that the item displays on the **General info** section of the DPM Workspace.|Yes|
        |Application|The application for the item.|No|
        |Workspace|The workspace for the item.|No|
        |Active|The flag that determines if the item displays \(or not\) on the **General info** section of the **Info** tab in the DPM Workspace.|Yes|
        |Conditions|Configuration options where you can set conditions for the item.|Yes|

7.  Select **Update**.


**Parent Topic:**[Use the Admin Center in Digital Portfolio Management](../concept/dpm-admin-center.md)

