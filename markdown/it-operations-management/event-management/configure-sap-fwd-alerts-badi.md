---
title: Configure SAP to forward alerts to your BADI
description: After setting up SAP Solution Manager monitoring, you must configure SAP to forward alerts to the BADI \(Business Add-in\) you create as the first step in the SAP integration setup.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SAP Solution Manager setup configurations, Enable SAP connector configurations, Configure SAP Solution Manager connector, Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure SAP to forward alerts to your BADI

After setting up SAP Solution Manager monitoring, you must configure SAP to forward alerts to the BADI \(Business Add-in\) you create as the first step in the SAP integration setup.

## Before you begin

Role required: evt\_mgt\_admin

## About this task

Third-party alerts get forwarded globally. You can configure the alert reaction only for a specific monitoring template.

## Procedure

1.  On the SAP UI, navigate to **Application Operations** &gt; **System Monitoring**.

2.  In the ribbon at the top of the System Monitoring configuration page, select **2 Configure Infrastructure** &gt; **2.3 Default Settings**.

    The **Default Settings** page appears.

    ![Default Settings tab page](../image/sap-solman-default-settings-tab.png "Default Settings page")

3.  Configure and activate a third-party component.

    1.  Enter edit mode by clicking the **Edit** button.

    2.  Select the **Third-Party Components** tab.

    3.  Click **Add** and add the following value as the third-party connector: `Implementation: BADI Definition for Alert Reactions ZSNOW with scope = All Alerts and Metrics`.

    4.  Click **Save** to activate third-party components globally.

4.  Define the objects to which the monitoring template will be assigned.

    1.  In the ribbon at the top of the page, select **5 Define Scope**.

        The Define Scope page appears.

        ![Define Scope page](../image/sap-solman-define-scope.png)

    2.  Select the managed object to which you want to assign the monitoring template.

        The monitoring template is assigned to the selected objects.

5.  Reactivate the monitoring of templates.

    1.  Select **6 Setup Monitoring**.

    2.  Search for and locate entries with **Setup Status = Reconfigure Required** and assign the monitoring template to those entries.

    3.  Select **Apply** and **Activate**.

        When the jobs finish, verify that the **Assignment Status** is green.

        All templates and active alerts assigned to the selected objects use the new forwarding method.


## What to do next

View alerts generated in SAP Solution Manager to see any pressing issues, as described in [View alerts in the SAP Solution Manager inbox](sap-view-alerts.md).

**Parent Topic:**[SAP Solution Manager setup configurations](../concept/sap-solman-configurations.md)

