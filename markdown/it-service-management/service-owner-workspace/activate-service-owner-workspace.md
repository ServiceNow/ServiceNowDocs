---
title: Activate Service Owner Workspace
description: The Service Owner Workspace plugin \(com.spm\_owner\_workspace\) is available as a separate subscription. It activates related plugins, including the Service Portfolio Management Premium plugin \(com.snc.spm\). Subscribing to Service Owner Workspace adds the service-owner user interface and premium functionality to your Service Portfolio Management environment.
locale: en-US
release: xanadu
product: Service Owner Workspace
classification: service-owner-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Setting up Service Owner Workspace, Service Owner Workspace, IT Service Management]
---

# Activate Service Owner Workspace

The Service Owner Workspace plugin \(com.spm\_owner\_workspace\) is available as a separate subscription. It activates related plugins, including the Service Portfolio Management Premium plugin \(com.snc.spm\). Subscribing to Service Owner Workspace adds the service-owner user interface and premium functionality to your Service Portfolio Management environment.

## Before you begin

Role required: admin

## About this task

**Important:** As of the San Diego release, Service Owner Workspace is in a planned deprecation. New customers can't find or activate Service Owner Workspace. ServiceNow® continues to support existing customers with Service Owner Workspace. For information on the product replacement and the deprecation process, see [Service Owner Workspace](../concept/SPM2-premium.md).

<table id="table_e2x_rbr_nkb"><tbody><tr><td>

![Set up Service Owner Workspace](../image/SOWSetupBanner2.png "Navigate")

</td></tr></tbody>
</table>A subscription to Service Owner Workspace includes full access to Performance Analytics.

The Performance Analytics - Premium plugin \(com.snc.pa.premium\) is necessary for Service Owner Workspace feature functionality. It must be activated before you can activate the Service Owner Workspace plugin.

The Service Owner Workspace plugin \(com.spm\_owner\_workspace\) activates related plugins if they are not already active.

![Activate Service Owner Workspace](../image/SOW_activateplugin.gif)

<table id="table_lgc_pwq_g3b"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Performance Analytics — Premium\[com.snc.pa.premium\]

 **Note:** This plugin must be activated before activating the Service Owner Workspace plugin \(com.spm\_owner\_workspace\).

</td><td>

Adds the following functionality to Service Portfolio Management: -   Create indicators, breakdowns, and other records.
-   Create text analytics widgets.
-   Use Performance Analytics with external data.
-   Preserve performance scores beyond 180 days.

</td></tr><tr><td>

Service Portfolio Management Premium \[com.snc.spm\]

</td><td>

Collects service offering metrics and rolls these calculations up to parent services and taxonomy nodes for performance scores and other metrics viewed via Service Owner Workspace.

</td></tr><tr><td>

Service Portfolio Management Estimated Spend\[com.snc.spm.spend\]

</td><td>

Provides a simple cost model.

</td></tr><tr><td>

Agent Workspace - Form\[com.snc.agent\_workspace.form\]

</td><td>

Provides workspace form configurations.

</td></tr><tr><td>

Agent Workspace - List\[com.snc.agent\_workspace.list\]

</td><td>

Provides workspace list configurations.

</td></tr><tr><td>

Agent Workspace - Highlighted Values\[com.snc.agent\_workspace.highlighted\_values\]

</td><td>

Provides support for highlighted values in workspace.

</td></tr><tr><td>

Agent Workspace - Declarative Actions\[com.snc.agent\_workspace.declarative\_actions\]

</td><td>

Provides support for declarative actions in workspace.

</td></tr><tr><td>

Service Workspace\[com.snc.service\_workspace\]

</td><td>

Provides the Service Workspace application.

</td></tr></tbody>
</table>Several additional plugins offer increased functionality to Service Owner Workspace. Activate these plugins to enhance your monitoring experience.

<table id="table_ily_qwq_g3b"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Vendor Manager Workspace \[com.snc.vlm.vmw\]

</td><td>

Provides integration with the Vendor Manager Workspace as part of the Service Owner Workspace monitoring experience.

</td></tr><tr><td>

Continual Improvement Management CIM\[com.sn\_cim\]

</td><td>

Enables display of existing CIM records in Service Owner Workspace when a service relation is indicated on associated forms. Service owners can initiate a CIM record to address a performance issue with a service or offering.

</td></tr><tr><td>

Incident Management - Major Incident Management \[com.snc.incident.mim\]

</td><td>

Provides a consolidated workbench to view major incidents via Service Owner Workspace.

</td></tr><tr><td>

Financial Management for SPM\[com.snc.financial\_management\_for\_spm\]

</td><td>

Enables integration of Financial Management with Service Portfolio Management, providing preconfigured service offering cost models to view in Service Owner Workspace. Collects service offering cost and enables you to select between your local cost model and the Financial Management application model, when used.

**Note:** Users can also choice not to use the local cost model or the Financial Management model, by selecting **None** in the

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


**Related topics**  


[Installed with Service Owner Workspace](../reference/installed-with-SOW.md)

[List of plugins \(New York\)](https://www.servicenow.com/docs/access?context=list-of-plugins&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

