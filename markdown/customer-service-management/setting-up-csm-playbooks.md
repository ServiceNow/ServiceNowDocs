---
title: Playbooks in Customer Service Management
description: Playbooks provide customer service agents with step-by-step guidance for resolving specific types of cases. Agents can follow a playbook in CSM Configurable Workspace and complete guided activities to resolve customer issues.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Playbooks in Customer Service Management

Playbooks provide customer service agents with step-by-step guidance for resolving specific types of cases. Agents can follow a playbook in CSM Configurable Workspace and complete guided activities to resolve customer issues.

![Playbook with a horizontal stage picker that displays stages across the top of the record and activities in the currently selected stage along the side of the record.](../image/case-playbook-template-horizontal-stages.png "Playbook with horizontal stages")

## Playbook overview

A [playbook](https://www.servicenow.com/docs/access?context=process-automation-designer&version=australia&pubname=australia-build-workflows&ft:locale=en-US) is an end-to-end workflow that includes the stages, steps, and guidance to lead users through a business process. A playbook visualizes a workflow in a task-oriented view and guides users through sequences of tasks.

A playbook takes a workflow and breaks it into multiple stages. Each stage in a playbook includes a logical group of sequential activities for an agent to complete. Stages can also include automated activities, such as sending an email to a customer when a stage or activity is complete.

Playbooks include:

-   A series of steps that a user must complete in order to achieve a particular goal and the necessary guidance for completing those steps.
-   One or more stages, or groups of tasks, and sequences of activities within each stage.

Playbooks are created in the [Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=australia&pubname=australia-build-workflows&ft:locale=en-US) application. Pages that display playbooks in a workspace are created in the [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=australia&pubname=australia-application-development&ft:locale=en-US) application. Agents use playbooks in [CSM Configurable Workspace](csm-workspaces-configure.md) to complete activities. End users can also use playbooks from service portals to create requests and provide information. For more information, see the following sections in this topic:

-   [Playbook users and tools](setting-up-csm-playbooks.md#section_lff_qpc_ybc)
-   [Configuring and configuring playbooks](setting-up-csm-playbooks.md#section_mvs_sqc_ybc)

## Playbook users and tools

The following table describes the different user roles that are involved in the creation, configuration, and use of playbooks. It also describes the tools and applications used by each of those roles.

<table id="table_jd2_s2d_ybc"><thead><tr><th>

User role

</th><th>

Tool / application

</th></tr></thead><tbody><tr><td>

Playbook admin\[playbook.admin\]

</td><td>

Uses the [Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=australia&pubname=australia-build-workflows&ft:locale=en-US) application to author, configure, and monitor playbooks.Workflow Studio is the design environment where playbook owners build playbooks.

</td></tr><tr><td>

Playbook experience admin\[playbook\_experience.admin\]

</td><td>

Uses the [About Playbook Experience](https://www.servicenow.com/docs/access?context=playbook-ui&version=australia&pubname=australia-build-workflows&ft:locale=en-US) application to create playbook experience records. These records define how playbook activities appear within a playbook.

</td></tr><tr><td>

UI Builder admin\[ui\_builder\_admin\]

</td><td>

Uses the [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=australia&pubname=australia-application-development&ft:locale=en-US) application to create or customize pages that display playbooks in [CSM Configurable Workspace](csm-workspaces-configure.md).UI Builder is a web user interface builder. Users with the UI Builder admin role use the tool to create pages, which are collections of components that make up a workspace user interface.

**Note:** [Playbook page templates](csm-playbook-templates.md) are available for UI Builder admins to use as a starting point for creating playbook pages.

</td></tr><tr><td>

Customer service agent\[sn\_customerservice\_agent\]

</td><td>

Uses playbooks in CSM Configurable Workspace to complete activities and resolve cases.The playbook runtime experience is where end users, such as agents, follow the playbook to complete a business process.

</td></tr><tr><td>

End user\[sn\_customerservice.customer\]

</td><td>

Uses playbooks create cases, provide requested information, and complete assigned tasks. For more information, see [Playbooks for portals](playbooks-for-portals.md).

</td></tr></tbody>
</table>## Creating and configuring playbooks

Creating and configuring a playbook involves different tools and applications. Playbooks are created using the Workflow Studio application. Some of the configuration for a playbook is performed in UI Builder as part of the playbook component configuration. Additional settings can be configured in the playbook experience record in the Core UI. These settings include selecting the playbook activity view and configuring playbook stage and activity visibility. For more information, see [Configure Playbooks for Customer Service Management](csm-playbooks-configuring.md).

<table id="table_lwt_dbd_ybc"><thead><tr><th>

Tools

</th><th>

Tasks

</th></tr></thead><tbody><tr><td>

[Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

</td><td>

Workflow Studio is the design environment where playbook owners \(users with the playbook.admin role\) build playbooks. For more information, see the following topics:-   [Exploring Workflow Studio](https://www.servicenow.com/docs/access?context=exploring-workflow-studio&version=australia&pubname=australia-build-workflows&ft:locale=en-US)
-   [Getting started with Playbooks](https://www.servicenow.com/docs/access?context=getting-started-processes&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

</td></tr><tr><td>

[About Playbook Experience](https://www.servicenow.com/docs/access?context=playbook-ui&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

</td><td>

Playbook experience records define how playbook activities appear within a playbook.-   Users with the playbook\_experience.admin role can create playbook experience records.
-   Users with the ui\_builder\_admin role can select a playbook experience when adding a playbook to a page in UI Builder.

The playbook experience record includes settings for the playbook stage and activity visibility, such as hiding or displaying playbook activities based on user role or activity state.

</td></tr><tr><td>

[UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=australia&pubname=australia-application-development&ft:locale=en-US)

</td><td>

Users with the ui\_builder\_admin role can use UI Builder to create or customize pages, which are collections of components that make up a workspace user interface. Some of the playbook configuration tasks in UI Builder include:-   **Selecting a playbook activity view**: The activity view determines how the stages and activities are displayed in the playbook. Select a playbook activity view in the playbook component configuration in UI Builder.
-   **Selecting a playbook experience**: The playbook experience determines how the system renders a playbook in a workspace. You can use playbook experiences to customize the look and feel of a playbook, map user actions, and override activities. Select a playbook experience when adding a playbook to a page in UI Builder.
-   **Configuring a playbook to use compact mode**: Compact mode moves the playbook to the contextual side panel. Agents can complete playbook activities in the side panel while viewing other information in the record page. Configure a playbook to use compact mode in the playbook component configuration in UI Builder.

</td></tr></tbody>
</table>## Using playbooks

Customer service agents can use the guidance available with playbooks to complete the tasks and activities that are needed to resolve specific types of cases.

A playbook includes multiple stages and each stage includes one or more activities for an agent to complete. When using a playbook, agents can:

-   View the stages and activities.
-   Select an activity and perform the work necessary to complete that activity.
-   Mark an activity as complete and move to the next activity or stage.
-   Complete the stages and activities necessary to resolve the case.

For more information, see [Using Playbooks for Customer Service Management](csm-playbooks-using.md).

## Playbook applications

Several applications are available that enable you to create and use playbooks with Customer Service Management. See [Playbook plugins](setting-up-csm-playbooks.md#section_qgq_ylk_llb) for detailed plugin and dependency information.

|Application|Description|
|-----------|-----------|
|Playbooks for Customer Service Management|Use this application to create or customize playbooks based on your individual business needs. Create playbooks that support case types or the base customer service case.|
|[Case Playbook for Onboarding](csm-case-type-onboarding.md)|Use this application to manage the process for taking on new customers or enrolling customers in new products. An onboarding case captures the details of the new customer, including their selection of products and services.|
|[Case Playbook for Complaints](csm-playbook-complaint-overview.md)|Use this application to manage the process for handling customer complaints. A complaint case captures the details of the problem reported by the customer and the expected resolution.|
|[Case Playbook for Product Support](csm-playbook-product-support.md)|Use this application to guide agents through the steps that are needed to resolve product issues. A product support case captures information about the customer, the product, and the reported issue.|

## Playbook plugins

The Playbooks for Customer Service Management plugin \(sn\_csm\_playbook\) is available from the ServiceNow Store. This plugin requires the following plugins:

-   Customer Service \(com.sn\_customerservice\)
-   Dynamic Related Records \(com.snc.uib.sn\_dyn\_rel\_rec\)
-   Playbook Experience \(com.playbook\_experience\)

The following playbook applications are available for use with Customer Service Management and are available from the ServiceNow Store:

-   Case Playbook for Onboarding
-   Case Playbook for Complaints
-   Case Playbook for Product Support

These playbooks require the following plugins:

-   Playbooks for Customer Service Management \(com.sn\_csm\_playbook\)
-   Customer Service Case Types \(com.snc.csm\_case\_types\)

## Request apps from the ServiceNow Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Related topics**  


[Interact with Playbook](https://www.servicenow.com/docs/access?context=playbook-ui&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

[Configure Playbooks for Customer Service Management](csm-playbooks-configuring.md)

[Using Playbooks for Customer Service Management](csm-playbooks-using.md)

