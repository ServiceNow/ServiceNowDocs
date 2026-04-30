---
title: Configure page headers in the DPM Admin Center
description: Configure the page header fields for your solutions in the DPM Admin Center. Your configuration determines how the header fields are displayed in the DPM Workspace.
locale: en-US
release: zurich
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure the Admin Center, Configure, Digital Portfolio Management, IT Service Management]
---

# Configure page headers in the DPM Admin Center

Configure the page header fields for your solutions in the DPM Admin Center. Your configuration determines how the header fields are displayed in the DPM Workspace.

## Before you begin

Role required: sn\_dpm.dpm\_admin

## About this task

Each solution displays header information for that solution. For example, for a service, the header information may display the owner name, the consumer type, the phase, the status, and the business criticality. You can configure the header information to best suit the needs of your organization. The DPM Admin Center enables you to configure the header information for the following solutions:

-   Services and service offerings \(both business and technical\)
-   Business applications
-   Service instances
-   Service portfolios and taxonomies
-   Enterprise portfolios and taxonomies

## Procedure

1.  Navigate to **All** &gt; **Digital Portfolio Management** &gt; **DPM Admin Center** &gt; **Settings**.

2.  Select **Header** for the solution that you want to configure the header information.

3.  Select **Configure**.

    You must be in the correct application scope to edit the record. If you're in a different scope, then a text banner displays for you to select a link to edit the record.

4.  Review the field names in the **Secondary Values** tab.

    The field names represent the information displayed on the solution header in the DPM Workspace.

5.  Configure the fields from the list view.

    You can do some minor configuring in the list view.

    -   You can set the **Active** value to true or false. After a field is set to false, it doesn't display on the solution header in the DPM Workspace.
    -   You can change the order that the active fields display on the solution header in the DPM Workspace.
6.  Configure the fields individually.

    -   Select a field to configure. You must be in the correct application scope to edit the record. If you're in a different scope, then a text banner displays for you to select a link to edit the record.
    -   Review or change the information.

        |Field|Description|Editable|
        |-----|-----------|--------|
        |Table|The table name for the item.|No|
        |Field|The field name for the item that displays in the DPM Workspace.|Yes|
        |Order|The order that the item displays on the solution header in the DPM Workspace.|Yes|
        |Application|The application for the item.|No|
        |Workspace|The workspace for the item.|No|
        |Active|The flag that determines if the item displays \(or not\) on the solution header of the DPM Workspace.|Yes|
        |Conditions|Configuration options where you can set conditions for the item.|Yes|

7.  Select **Update**.


**Parent Topic:**[Use the Admin Center in Digital Portfolio Management](../concept/dpm-admin-center.md)

