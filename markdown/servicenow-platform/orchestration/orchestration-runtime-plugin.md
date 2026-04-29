---
title: Orchestration Runtime plugin
description: The Orchestration – Runtime plugin enables other applications on the ServiceNow platform to automate tasks, without requiring an Orchestration subscription.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Activate Orchestration, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Orchestration Runtime plugin

The Orchestration – Runtime plugin enables other applications on the ServiceNow® platform to automate tasks, without requiring an Orchestration subscription.

The Orchestration – Runtime plugin can be activated as part of another plugin or application. It is used by strategic technology partners and ServiceNow applications to distribute activity packs to customers who may not own Orchestration. For example, the Security Incident Response Management \(SIRM\) application provides orchestration content, which includes activities that are available from the **Packs** tab in the Workflow Editor. Customers who purchase SIRM can consume and modify the activities that SIRM ships without having to purchase an Orchestration license.

## Included with the plugin

The Orchestration – Runtime plugin provides access to the **Packs** and **Data** tabs in the Workflow Editor. This plugin gives users access to custom activities for their applications and enables them to reuse data from the [Databus](../../../administer/orchestration-activity-designer/concept/c_OrchestrationDatabus.md#). This plugin does not provide access to custom Orchestration [activity packs](../../../administer/orchestration-activities/concept/c_OrchestrationActivityPacks.md) or to the [activity designer](../../../administer/orchestration-activity-designer/concept/c_WorkflowActivityDesigner.md). The **Custom** tab in the Workflow Editor is not available without an Orchestration subscription.

![Orchestration plugin relationships](../image/OrchestrationRuntimeDiagram.png "Orchestration plugin relationships")

## Dependencies

The Orchestration – Runtime plugin activates these application plugins:

-   Security Incident Response Orchestration
-   Service Release Automation

.

## Access to activities

Custom activities shipped with ServiceNow® applications are available in the **Packs** tab of the Workflow Editor for use in workflows. To edit these activities, navigate to **Orchestration** &gt; **Activity Designer Activities** and select the activity you want to modify. For information about the provider templates used to create these activities, see [Orchestration custom activity templates](../../../administer/orchestration-activity-designer/concept/c_ActivityDesignerComponents.md).

**Parent Topic:**[Activate Orchestration](../task/t_ActivateOrchestration.md)

