---
title: Using the item generation process to generate controls and risks
description: The ServiceNow GRC suite of applications can automatically generate controls and risks for your organization with the enhanced item generation process. The enhanced item generation process \(v2\) in version 13.x.x fixes the stalling and performance issues from the item generation process \(v1\) in version 12.x.x and earlier releases.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Common GRC features, Governance, Risk, and Compliance]
---

# Using the item generation process to generate controls and risks

The ServiceNow® GRC suite of applications can automatically generate controls and risks for your organization with the enhanced item generation process. The enhanced item generation process \(v2\) in version 13.x.x fixes the stalling and performance issues from the item generation process \(v1\) in version 12.x.x and earlier releases.

## Overview of the item generation process

By using the Governance, Risk, and Compliance application, you can use the item generation process to generate controls and risks for your organization.

A control is the actual control activity that an organization performs. For example, a control can be related to authoritative source content \(legal articles, regulations, or public records\), policies, and risks. A control is automatically generated when you associate a policy with an entity type \(grouping of the entities that match a set of filter conditions\) or an entity type with a control objective. For more information on controls, see [Manage controls](../../grc-policy-and-compliance/concept/c_GRCControls.md).

A risk is any threat or vulnerability that could adversely affect an organization’s business objectives. For example, a risk can be related to any item, policy, control, or remediation task. A risk is automatically generated when you make associations between risk frameworks or risk statements and entity types.

**Note:** Risk statements are general statements about potential risks or threats that could occur in an organization. A risk framework consists of a risk assessment, response, and accountability for the risk and mitigation activities around it.

For more information on risks, see [Using Risk Management](../../grc-risk/concept/using-risk-mgmt.md).

The item generation process \(v1\) in version 12.x.x and earlier releases generated out-of-sync updates due to the stalled actions in the action queue. The enhanced item generation process \(v2\) eliminates the stalling issues and improves the processing time of the controls and risks significantly. For example, the legacy item generation process \(v1\) generated 10,000 risks in approximately 13.7 minutes where the new item generation process \(v2\) can generate 10,000 risks in approximately 5.27 minutes.

## Flow of the item generation process

The item generation process inserts an action in the action queue and executes the actions one by one in a sequence. A scheduled job runs periodically to check the action queue. If an action is running in the queue, the scheduled job skips it. When the current running action is completed and no other action is in process, the scheduled job picks up the next action in the Ready state in the queue as shown in the following example.

![Item generation process flow.](../image/item-gen-process-flow.png "Item generation process flow")

## Benefits of the item generation process

The new item generation process provides the following key benefits:

-   Processes the controls and risks quickly by using the item generation action event queue.
-   Eliminates the stalled actions and race conditions​ in the queue that generated the non-consistent updates.
-   Logs the history and status of the item generation actions.
-   Provides more information about an error in the item generation action event queue. It helps you to track and troubleshoot the issues quickly and efficiently.
-   Helps the compliance and risk managers to manage the controls and risks in an auto-pilot mode without much maintenance.

## Applications that are used in the item generation process

The following GRC applications are used in the item generation process:

-   GRC: Policy and Compliance Management
-   GRC: Risk Management
-   GRC: Profiles

The GRC: Profiles application is automatically installed when either the GRC: Policy and Compliance Management or GRC: Risk Management application is activated.

## Upgrade scenarios and their impact on the existing implementations

You must upgrade both Policy and Compliance Management and Risk Management applications to version 13.x.x. When you upgrade the Policy and Compliance Management and Risk Management applications to version 13.x.x, the new item generation process \(v2\) replaces the legacy item generation process \(v1\).

**Note:** Upgrading the Policy and Compliance Management and Risk Management applications to version 13.x.x automatically upgrades the GRC: Profiles application to version 13.x.x​.

Ensure that you have the required versions of the Policy and Compliance Management and Risk Management applications installed in your instance. If you have one of the following scenarios for the installed applications, you receive an error message on the screen:

-   You have both the Policy and Compliance Management and Risk Management applications previously installed in your instance and you upgrade only one of them to version 13.x.x.
-   You have only one of the Policy and Compliance Management or Risk Management applications installed in your instance and you upgrade the GRC: Profiles application to version 13.x.x.
-   You have both Policy and Compliance Management or Risk Management applications installed in your instance and you upgrade the GRC: Profiles application to version 13.x.x.

The error message states that you must upgrade both Policy and Compliance Management and Risk Management applications to version 13.x.x as shown in the following example.

![Message for upgrading the applications.](../image/item-gen-upgrade-message.png "Message for upgrading the applications")

When you upgrade, you don't see any visible impact to your existing implementations of the item generation process.

**Note:** If you haven’t upgraded to version 13.x.x, the legacy item generation process is still supported.

## Components that are used by the item generation process

The item generation process uses several types of reference components such as tables, scheduled jobs, and action handlers. For more information on the components that are used with the item generation process, see [Components installed with the item generation process](../reference/components-item-gen-process.md).

## Using the scheduled job and action event queue

The item generation process uses the **Item generation action queue processor** scheduled job and an action event queue in the background. As a user with the sn\_grc.admin role, you can configure the frequency of the scheduled job as shown in the following example.

![Configure the frequency of the scheduled job.](../image/action_queue_processor.png "Configure the frequency of the scheduled job")

When you initiate an action that results in generating, updating, or deleting a control or risk, the scheduled job inserts a record for each action in the sn\_grc\_item\_generation\_action\_event\_queue.list table. The item generation action event queue is shown in the following example.

![Item generation action event queue.](../image/activate-document-in-the-queue.png "Item generation action event queue")

When an action is generated by using the item generation process, a message that the item generation process has been initiated is displayed. For example, when you add a risk statement to a control objective, you see the message that is shown in the following example.

![Initiation of the item generation process.](../image/relationshop-bet-risks-controls.png "Initiation of the item generation process")

If an error occurs while processing an action in the queue, the item generation process displays more information about the error. For example, you might see an error trace with the object ID as shown in the following example.

![Error trace.](../image/item-gen-error-msg.png "Error trace")

You can use the error trace and other details in the queue to track and troubleshoot the issue.

## Script includes action handlers

The item generation process uses the script includes action handlers that process the actions for the Policy and Compliance Management and Risk Management applications.

You can view the list of the supported action handlers by navigating to **Script Includes** in the application navigator as shown in the following example.

![Script includes action handlers.](../image/script-includes-menu.png "Script includes action handlers")

All script includes action handlers contain the base version and the extended version. The item generation process uses the base version for handling the actions. As a user with the sn\_grc.manager role, you can review the base functions that are listed in the action handler as shown in the following example.

![Base functions.](../image/base-functions.png "Base functions")

As a user with the script\_include\_admin role, you can revise the action strategy for a control or risk by overriding the base functions as shown in the following example.

![Override the base functions.](../image/override_base_class_functions.png "Override the base functions")

-   **[Components installed with the item generation process](../reference/components-item-gen-process.md)**  
Several types of components are installed with the item generation process, including tables, scheduled jobs, and action handlers.
-   **[Operational changes in item generation of common controls](../reference/item-gen-action-types.md)**  
Operational changes are made in item generation mainly because item generation either creates a control or activates an existing standard control. When it comes to associating a control to an entity, then associating a reliant entity to a common control takes precedence over creating a control for that entity.

**Parent Topic:**[Common Governance, Risk, and Compliance features](common-grc-features.md)

