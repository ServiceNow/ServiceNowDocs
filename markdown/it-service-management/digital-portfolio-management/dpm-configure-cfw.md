---
title: Configuring Digital Portfolio Management
description: Enable the Digital Portfolio Management \(DPM\) Workspace and configure the settings for your organization. Set it up to show data so you can monitor services, service offerings, business applications, and service instances. All configuration tasks require the DPM admin role \[sn\_dpm.dpm\_admin\].
locale: en-US
release: zurich
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Digital Portfolio Management, IT Service Management]
---

# Configuring Digital Portfolio Management

Enable the Digital Portfolio Management \(DPM\) Workspace and configure the settings for your organization. Set it up to show data so you can monitor services, service offerings, business applications, and service instances. All configuration tasks require the DPM admin role \[sn\_dpm.dpm\_admin\].

## Using guided setup to implement Digital Portfolio Management \(DPM\)

Guided setup provides a sequence of tasks that help you configure the DPM Workspace on your ServiceNow instance. To open the guided setup for DPM, navigate to **All** &gt; **Digital Portfolio Management** &gt; **DPM Admin Center**.

For more information, see [Use the Admin Center in Digital Portfolio Management](dpm-admin-center.md).

**Note:** The DPM Workspace uses the taxonomy structures from the Service Portfolio Management application. For more information, see [Service Portfolio Management taxonomy](../../service-portfolio-management2/concept/SPM2-taxonomy.md).

## Configuration overview

Configuring the DPM Workspace involves setting up environments, tools, and user access. To configure, you must have the DPM admin role \[sn\_dpm.dpm\_admin\]. You perform most of these configuration tasks in each instance that you're using.

1.  [Activate Digital Portfolio Management](../task/dpm-activate.md).

    You can activate DPM by searching for it on the ServiceNow® Store.

2.  [Use the Admin Center in Digital Portfolio Management](dpm-admin-center.md).

    Use the DPM Admin Center for a guided walk-through to do the following configuration tasks.

    1.  Identify the solutions that are ready to configure for the organization. Solutions could be services, service offerings, business applications, and service instances.
    2.  Identify the service portfolios or the enterprise portfolios that are ready to configure for the organization.
    3.  Assess planning items for the plan portion of the solution life cycle. If your organization doesn’t use the planning portion of the life cycle, then follow the prompts to remove the plan view for the organization.
    4.  Assess build metrics to show a solution's performance in the build portion of the solution life cycle.
    5.  Map key performance indicator \(KPI\) groups to track the performance of the solutions.
    6.  Assess other tasks to complete verifying that the DPM Workspace is ready for the organization.
3.  [Apply the CSDM guidelines to Digital Portfolio Management](../reference/dpm-csdm.md).

    Service data relates to each other using different applications and in different ways. DPM references the Common Service Data Model \(CSDM\) to bring service-related data together in a single view.


Even though you can return to the DPM Admin Center at any time to update configuration settings, you can also complete most of the following configuration tasks independently.

-   **[Activate Digital Portfolio Management](../task/dpm-activate.md)**  
The Digital Portfolio Management plugin is available from the ServiceNow® ServiceNow Store.
-   **[Use the Admin Center in Digital Portfolio Management](dpm-admin-center.md)**  
The Admin Center in Digital Portfolio Management \(DPM\) provides administrators a guided walk-through to set up and configure the DPM Workspace for the organization. The provided information and configuration prompts enable visibility into the end-to-end service and application life-cycle.
-   **[Apply the CSDM guidelines to Digital Portfolio Management](../reference/dpm-csdm.md)**  
Service data relates to each other using different applications and in different ways. Digital Portfolio Management \(DPM\) references the Common Service Data Model \(CSDM\) framework to bring service-related data together in a single view.
-   **[Integrate Digital Portfolio Management with other ServiceNow applications](dpm-integrations.md)**  
Bring in data from other ServiceNow applications to see a comprehensive view of your solutions in the Digital Portfolio Management \(DPM\) Workspace. You can see data for services and service offerings, for business applications, and for service instances.
-   **[Configure KPI groups in Digital Portfolio Management](dpm-configure-kpi-groups.md)**  
Configure key performance indicator \(KPI\) groups in Digital Portfolio Management \(DPM\) to surface performance information in the context of your organization's solutions.
-   **[Configure Needs attention panels in Digital Portfolio Management](../task/dpm-configure-needs-attention.md)**  
Each solution page in Digital Portfolio Management \(DPM\) has a Needs attention panel with items that need attention in the context of the page. You can configure the Needs attention attributes to meet your organization's needs.
-   **[Configure the Digital Portfolio Management experience](../task/dpm-configure-experience.md)**  
If your organization doesn't use certain modules or life-cycle phases in Digital Portfolio Management \(DPM\), then configure the experience by hiding those elements from user views.
-   **[Relate business capabilities to view in Digital Portfolio Management](../task/dpm-business-capability.md)**  
You can relate business capabilities for a service or for a business application to see them in the Digital Portfolio Management \(DPM\) Workspace.
-   **[Configure Digital Portfolio Management to integrate with Process Mining](dpm-setup-po.md)**  
Use Process Mining in Digital Portfolio Management \(DPM\) to see the status of a key performance indicators \(KPI\) on your solutions, and adjust as needed.
-   **[Create Process Mining projects for KPI groups in Digital Portfolio Management](../task/dpm-create-project-po.md)**  
Create Process Mining projects for each key performance indicator \(KPI\) group in Digital Portfolio Management \(DPM\) to see KPI performance and analyze anomalies.

**Parent Topic:**[Digital Portfolio Management](../reference/dpm-landing.md)

**Related topics**  


[Use the Admin Center in Digital Portfolio Management](dpm-admin-center.md)

