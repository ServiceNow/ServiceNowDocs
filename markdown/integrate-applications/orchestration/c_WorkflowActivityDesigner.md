---
title: Orchestration activity designer
description: The Orchestration activity designer enables a user with either the workflow\_admin or activity\_creator and workflow\_creator roles to construct reusable activities that suit an organization's business needs.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Classic Orchestration, Workflow Data Fabric]
---

# Orchestration activity designer

The Orchestration activity designer enables a user with either the workflow\_admin or activity\_creator and workflow\_creator roles to construct reusable activities that suit an organization's business needs.

Activities created by the activity designer offer the following advantages over core activities offered in previous releases:

-   Reuse [custom activities](../task/create-custom-activities.md) in multiple workflows.
-   Upload and download custom activities from the ServiceNow Store.
-   Parse data from standard input formats.
-   Test input variables against a target host or endpoint and inspect the payload.
-   Automatically map values from a test payload to an activity's output variables.
-   Share data between activities.
-   View previous versions of an activity.

Access to the activity designer requires activation of ServiceNow Orchestration. For instructions about managing transitions and conditions for all activities, see Workflow activities.

Orchestration provides numerous pre-defined activities, which are reusable components that can be used in numerous workflows without having to understand the complexities of the underlying system. These activities are grouped into activity packs, which address specific business needs, such as: Active Directory, Azure AD, Exchange, Infoblox DDI, and PowerShell. There are other ServiceNow applications which provide and maintain their own separate activity packs, such as Security Incident Response, Cloud Management, or Release Automation.

Customers can also build their own activities and activity packs. You can construct custom activities with a specified template through the Orchestration Activity Designer. Custom-built activities built with the Activity Designer are referred to as activity elements. Activity elements provide optimal operations, enable code reuse, and minimize the need to write code. They also enable you to follow the flow of data within a given workflow across orchestration activities. Incorporating activity elements limits the dependency on the scratchpad which reduces problems in complex workflows. Limit the use of core activities, like ‘Run Script’, unless you need direct access the scratchpad, for example, for a counter. Activity elements do not have direct access to the scratchpad. You can, however, pass scratchpad variables as inputs into your activities.

Orchestration activities created by the activity designer:

-   Can be uploaded and shared in the ServiceNow App Store
-   Use the databus, which allows the activity to have well-defined inputs and outputs
-   Share data across activities within a workflow
-   Use versioning
-   Provide a consistent approach for activity development regardless protocol

**Note:** Prior to the Fujirelease, activities were built with Activity Definitions. In Fuji, a new architecture was introduced using the Activity Designer. Orchestration Core activities, built originally as Activity Definitions, have been converted to use the new template format \(Activity Elements\) and the databus offered with the activity designer. Workflows in upgraded instances that use legacy activities continue to work normally.

For instructions on using activities to construct a workflow, see Add an activity to a workflow.

-   **[Introduction to credentials, connections, and aliases for Orchestration](credentials-conn-alias-orch.md#)**  
All application integrations in Orchestration require connection information, credentials, and connection and credential aliases to their respective applications to access resources.
-   **[Create custom activities using custom activity designer templates](../task/create-custom-activities.md)**  
You can create and update different types of custom activities in the Workflow Editor using a custom template.
-   **[Orchestration custom activity templates](c_ActivityDesignerComponents.md)**  
Orchestration provides customizable activity templates to create and manage custom activities in the Workflow Editor.
-   **[Activity scoping](c_ActivityScoping.md)**  
Custom activities run in their own scope, even if it is different from that of the workflow.
-   **[Publish a custom activity](../task/t_PublishACustomActivity.md#)**  
When a user creates a custom activity and saves or submits it, that activity appears in the **Custom** and **Packs** tabs of the designer palette, but is visible only to the user who created it.
-   **[Copy a custom activity](../task/t_CopyACustomActivity.md)**  
You can copy activities for reuse from the **Custom** tab in the global scope.

**Parent Topic:**[Classic Orchestration](../../../product/orchestration/reference/r-orchestration.md)

