---
title: Map logs to service instances, components, and source types for contextual alerts in Health Log Analytics
description: Map your logs to service instances, components, and source types so that Health Log Analytics \(HLA\) can generate contextual alerts.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-10-12"
reading_time_minutes: 4
keywords: [integration, mapping, automatic, log context, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Mapping logs for contextual alerts, Set up integrations from Integrations Launchpad, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Map logs to service instances, components, and source types for contextual alerts in Health Log Analytics

Map your logs to service instances, components, and source types so that Health Log Analytics \(HLA\) can generate contextual alerts.

## Before you begin

Configure and activate an integration before you perform this procedure. For more information, see [Set up integrations for Health Log Analytics from the Integrations Launchpad](../concept/hla-data-input-setup-integrations.md).

Role required: evt\_mgmt\_admin

## About this task

HLA uses the settings that you define in this procedure to identify service instances, components, and source types in log examples and map log data to them automatically. HLA links logs to the corresponding service instances, components, and source types for contextualized analysis. By default, automatic log context mapping is enabled.

AI suggests the optimal log field for mapping to service instances and components. When you use the AI-suggested field or if it’s the default field, an AI sparkle icon \(![](../../../common/image/icon-ai-sparkle.png)\) appears. You can select a different field if needed. If AI can't find an optimal match or if your selected field is missing from the sample log, HLA uses the system default.

**Important:** If a manually defined mapping script exists in the **Data Input Mapping** page, automatic mapping overwrites it.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the bottom of the navigation pane, select the AIOps configuration center icon ![ITOM AIOps configuration center icon](../image/icon-itom-aiops-config.png).

    The ITOM AIOps configuration center page appears. The configuration center is a centralized workspace. Use it to configure and manage AIOps features from a single place.

3.  Under Integrations, select **Manage installed integrations**.

    The Integrations Launchpad appears.

4.  On the **Installed integrations** tab, search for an integration and open it.

    The **Overview** screen displays.

5.  Under **Next steps**, on the **Log context mapping** card, select **View mapping**.

    The **Log context mapping** table displays.

6.  Select the relevant integration.

    The integration's **Log context mapping** page displays.

    **Note:** If the selected integration has features that are unsupported in Service Operations Workspace, you’re referred to the **Data Input Mapping** page. For more information, see [Map raw log data in Health Log Analytics](hla-data-input-mapping.md).

7.  Turn off automatic service instance and component mapping by using the toggle.

    If you turn off automatic mapping, you must define a mapping script manually in the **Data Input Mapping** page. For more information, see [Map raw log data in Health Log Analytics](hla-data-input-mapping.md).

    The remaining steps in this procedure are only relevant when automatic mapping is enabled.

    **Note:** When you open the **Log context mapping** form for the first time, the system default values display in all fields.

8.  Configure the log field by which HLA identifies a service instance from the **Raw log field** drop-down list.

    A service instance represents a complete business process.

9.  Configure the log field by which HLA identifies a component from the **Raw log field** drop-down list.

    A component represents the smallest part of a service instance. A single service instance typically comprises multiple components.

10. Select **Preview** to view the service instances and components the system has identified based on your settings in the previous steps.

    The service instances and components are grouped by service.

11. In **Advanced settings**, review the fallback service and set the log field by which the system identifies a source type.

    1.  In the **Selected fallback service** field, review the fallback service the system uses if it can't identify the service instance in the log data.

        The displayed fallback service is the default service instance that you selected when you configured the integration.

        **Note:** For some integrations, such as Filebeat, this field shows `N/A` instead of a value. In these integrations, if HLA can't identify the service instance, it uses the system default value rather than the fallback service.

    2.  Configure the log field by which HLA identifies a source type from the **Raw log field** drop-down list.

    3.  Select **Preview** to view the log sources the system has identified based on your source type settings.

12. In the Simulator, review a log processing simulation based on your current mapping.

    The provided simulation helps you understand how the current mapping impacts HLA log processing. Use this information to fine-tune your settings:

    -   The **Log fields** tab shows the default service, component, and source type and the raw log.
    -   The **Extracted values** tab shows the service instance, component, and source type that the system has extracted from the raw log based on your current settings.
13. Select **Save mapping** to save your settings.


**Parent Topic:**[Set up Health Log Analytics on your ServiceNow instance](../concept/hla-implement.md)

