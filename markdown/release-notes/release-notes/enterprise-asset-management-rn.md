---
title: Enterprise Asset Management release notes
description: The ServiceNow Enterprise Asset Management application manages the entire life cycle of your enterprise's connected and non-connected assets, which enables you to maintain and maximize the life of your assets while minimizing any costly downtimes. Enterprise Asset Management was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
---

# Enterprise Asset Management release notes

The ServiceNow® Enterprise Asset Management application manages the entire life cycle of your enterprise's connected and non-connected assets, which enables you to maintain and maximize the life of your assets while minimizing any costly downtimes. Enterprise Asset Management was enhanced and updated in the Australia release.

## Enterprise Asset Management highlights for the Australia release

[Australia Patch 1](../quality/australia-patch-1.md)

-   Streamline the enterprise asset request process by using the help manage enterprise asset requests agentic workflow.
-   Automatically generate troubleshooting, diagnostics, and repair instructions for your enterprise asset repairs by using the help repair enterprise assets agentic workflow.

Early Availability

-   Streamline complex maintenance activities across assets, asset groups, or locations with unified work order plans.
-   Streamline inventory asset management with the expanded and efficient inventory auditing process.

See [Enterprise Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/enterprise-asset-management.md) for more information.

**Important:** The following applications are available in the ServiceNow Store:

-   Enterprise Asset Management
-   Enterprise Asset Management for Healthcare
-   Enterprise Asset Management for Facilities
-   Operational Technology \(OT\) Asset Management
-   Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\)
-   Enterprise Asset Management for Providers
-   Expanded Model and Asset Classes

For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Automate enterprise asset sourcing by using an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/now-assist-eam-help-manage-enterprise-asset-requests-workflow.md)**

    Use the help manage enterprise asset requests agentic workflow to automate the process of sourcing assets for your enterprise asset requests. The workflow uses AI agents to fulfill these requests by allocating assets from local stockrooms, creating transfer orders to move assets between stockrooms, or generating purchase orders for the requested assets.

-   **[Automatically generate instructions for enterprise asset repairs by using an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/now-assist-eam-help-repair-enterprise-assets-workflow.md)**

    Use the help repair enterprise assets agentic workflow, which is driven by AI agents, to automatically generate step-by-step troubleshooting, diagnostics, and repair instructions for your enterprise asset repairs in real time.

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[Define, schedule, and track complex asset-centric work tasks through work order plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/manage-work-order-plans.md)**

    Manage complex asset-centric work tasks with unified work order plans that can be applied across assets, asset groups, or locations. The work order plans offer the following benefits:

    -   Save work order plans as reusable templates for use across assets.
    -   Organize sequential operations—shutdowns, safety inspections, calibrations, asset conditions, and restarts—using the structured playbook.
    -   Assign, schedule, and track work order tasks for technicians within the playbook.
    -   Enable technicians to receive assigned work order tasks and update task status through the ServiceNow Mobile Agent application.
-   **[Manage multimedia production equipment models and assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/create-model-eam.md)**

    Create, track, and manage multimedia production equipment models and assets in the Enterprise Asset Workspace. Get a comprehensive view of these models and assets so that you can manage them effectively throughout their life cycles.

-   **[Replace broad admin checks with granular admin roles and ACL updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/eam-roles.md)**

    Manage admin access precisely with granular admin roles. Instead of giving full admin privileges to the users, you can assign specific roles based on the tasks they perform.

-   **[Enhanced and unified enterprise asset inventory auditing experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/audit-eam-assetinventory.md)**

    Streamline and improve your inventory auditing experience with the enhanced and unified enterprise asset inventory process:

    -   Initiate a single audit that covers both hardware and enterprise assets assigned to a specific location or stockroom, eliminating the need to switch between multiple workspaces.
    -   Include consumable assets in the inventory audit to avoid asset shrinkage and ensure that inventory data remains accurate.
    -   The ServiceNow Agent app features selectable audit results, enabling you to view a real-time list of all scanned assets.
    -   When new assets are identified during the single scan audit, essential information is collected in real time through the ServiceNow Agent app to initiate asset creation.
    -   Scanned asset locations are automatically updated to reflect their precise aisle, space, or sub location during the audit, supporting the accuracy and quality of inventory records.

## UI changes

-   **[Work order plan reports in the Work management view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/work-management-overview-eam.md)**

    The Work management view of the Enterprise Asset Workspace includes work order plan status and task reports.

-   **[Work order plan tabs in the Work management view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/work-management-overview-eam.md)**

    The Work management view of the Enterprise Asset Workspace includes two new tabs:

    -   Work order plans- View existing work order plans and create plans
    -   Work order plan templates- Access available templates and create reusable templates
-   **[Affected assets tab in work orders and work order tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/work-management-overview-eam.md)**

    The **Affected assets** tab provides a comprehensive view of all assets associated with a work order. When a work order includes an asset group, the tab lists every asset belonging to that group.


## Changed in this release

-   **[Multiple assets and asset groups in a work order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/create-eam-work-order-task.md)**

    A work order and work order task can now be created for asset groups in addition to individual assets. Additionally, the sn\_eam.enterprise\_asset\_manager role can add more assets to tasks while they're in the draft stage. When technicians start the task, they can take action on all included assets. The Deploy Asset, Swap Asset, and Remove Asset actions within work order tasks support multiple assets and asset groups.

-   **[Shutdown and Startup work types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/create-eam-work-order-task.md)**

    The **Shutdown** and **Startup** work types available in the work order tasks enable you to manage asset shutdown and restart tasks.

-   **[Multiple calibration playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/complete-eam-work-order.md)**

    When a calibration work order is created for multiple assets or an asset group, the system generates a separate calibration playbook for each asset in the Affected assets list.

-   **[Multiple condition lines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/perform-condition-assessment-webui.md)**

    When an asset condition work order is created for multiple assets or an asset group, the system generates a separate condition line for each asset in the Affected assets list. All condition lines must be evaluated before the work order can be completed.


## Activation information

Install the following applications by requesting them from the ServiceNow Store:

-   Enterprise Asset Management
-   Enterprise Asset Management for Healthcare
-   Enterprise Asset Management for Facilities
-   OT Asset Management
-   Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\)
-   Enterprise Asset Management for Providers
-   Expanded Model and Asset Classes

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/fsm-application-landing-page.md)**

    The ServiceNow® Field Service Management application enables your organization to manage location-based work more efficiently and safely.

-   **[Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/contract-management/c_ContractManagement.md)**

    The ServiceNow® Contract Management application enables you to track and manage your contracts.

-   **[Procurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/procurement/c_Procurement.md)**

    The ServiceNow® Procurement application helps you create purchase orders and obtain items for fulfilling service catalog requests.


**Parent Topic:**[IT Asset Management release notes](it-asset-management-rn-landing.md)

