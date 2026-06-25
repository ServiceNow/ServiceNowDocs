---
title: Request Change Management - Standard Change Template Intelligence
description: To activate Change Management capability that uses Predictive Intelligence to identify change clusters and propose standard change templates, request the Change Management - Standard Change Template Intelligence plugin \(com.snc.change\_management.ml.sctp\) through the Now Support Customer Service system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/request-cm-std-chg-template-intelligence.html
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Change Management plugins, Configure, Change Management, IT Service Management]
---

# Request Change Management - Standard Change Template Intelligence

To activate Change Management capability that uses Predictive Intelligence to identify change clusters and propose standard change templates, request the Change Management - Standard Change Template Intelligence plugin \(com.snc.change\_management.ml.sctp\) through the Now Support Customer Service system.

## Before you begin

Role required: maint

## About this task

The Change Management - Standard Change Template Intelligence plugin \(com.snc.change\_management.ml.sctp\) plugin activates these related plugins if they are not already active.

<table id="table_fvt_nq2_plb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Change Management - Predictive Intelligence Core\[com.snc.change\_management.ml\]

</td><td>

Enables you to use Predictive Intelligence in Change Management.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Select **Request plugin** to open the **Activate Plugin** form on Now Support.

3.  On the **Activate Plugin** form, provide the following information.

<table id="table_awx_bhf_ygb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="target-instance"><td>

What is your target instance

</td><td>

Select the instance that you want to activate the plugin on.

</td></tr><tr><td>

Which plugin would you like to activate

</td><td>

Select the name of the plugin to activate.

 **Note:** If the plugin isn't listed, or if you're activating on an OEM or on-premise instance, select the **Plugin I'm looking for is not listed** check box. Enter the plugin name in the field that appears.

</td></tr><tr id="date-time"><td>

Select Maintenance Date and Time

</td><td>

Select the date and time to activate the plugin.

</td></tr></tbody>
</table>    For example, see the following form to activate the Event Management plugin on an instance named SNC Instance.

4.  Select **Submit**.

    After the maintenance window, the system installs the plugin on your instance. To confirm the installation, go to the Installed tab in the Application Manager.


-   **[Components installed with Change Management - Standard Change Template Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/installed-with-std-chg-temp-ml.md)**  
Several types of components are installed with activation of the Change Management - Standard Change Template Intelligence plugin that includes tables.

**Parent Topic:**[Change Management plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/change-plugins.md)

**Related topics**  


[Request ITSM Roles- Change Management]()

[Activate Business Stakeholder]()

[Activate Change Management - State Model]()

[Activate Change Management - Collision Detector]()

[Activate Best Practice - Change Risk Calculator]()

[Activate Change Management - Change Schedule]()

[Activate Change Management - Risk Assessment]()

[Activate Change Management - Standard Change Catalog]()

[Activate Change Management - Change Success Score]()

[Activate Change Management - Mass Update CI]()

[Activate Change Management -Approval policy]()

[Activate Change Management - CAB Workbench]()

[Activate Change Management ATF Tests]()

[Activate Change Management - Core]()

[Request Change Management - Risk Assessment]()

[Change Management - Predictive Intelligence Core]()

[Activate Change Management - Change Flows]()

[Activate Change Management - Change Velocity dashboard]()

[Activate Change Management - Change Models]()

[Activate Change Management Success Probability]()

[Activate Change Management - Data Archiving]()

[List of plugins \(Australia\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/list-of-plugins.md)

