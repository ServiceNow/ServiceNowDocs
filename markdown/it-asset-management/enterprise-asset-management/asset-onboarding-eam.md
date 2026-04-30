---
title: Playbooks for Enterprise Asset Management
description: Playbooks provide a step-by-step guidance for setting up your assets with important information.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Explore, Enterprise Asset Management, IT Asset Management]
---

# Playbooks for Enterprise Asset Management

Playbooks provide a step-by-step guidance for setting up your assets with important information.

## Playbook overview

A playbook takes a workflow and breaks it into multiple lanes. The workflow for a playbook is generally created using the [Exploring playbooks](https://www.servicenow.com/docs/access?context=process-automation-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US). Each lane in a playbook includes:

-   A list of activities that you review.
-   Status indicators that display the current state of each activity.
-   Check marks that indicate where you are in the workflow.

As you mark an activity complete in a lane, you move to the next activity. You can save an activity at any time and return to the playbook later. After you complete all the activities in a lane, you move to the next lane. As you keep completing activities and lanes, the status keeps getting reflected in the left-hand panel. An Activity log, on the right-hand side of the playbook shows all the data that you’ve entered for each activity.

## Playbook layout

The playbook is divided into the following parts:

-   lanes on the left-hand side.
-   work area in the center.

## Available playbooks for Enterprise Asset Management

Use the following playbooks to complete various Enterprise Asset Management workflows:

-   Asset onboarding playbook: Allows you to onboard a single asset.
-   Multi-asset onboarding playbook: Allows you to onboard multiple assets at one go.
-   Calibration event playbook: Allows you to track and manage the asset calibrations that you are performing as part of your work orders.

## Asset onboarding playbook

The asset onboarding playbook provides context at each step of the process and helps you enter critical information for your assets.

Each asset can have only one onboarding process and for each onboarding process, there's an onboarding task to track the process.

The Asset Onboarding Task \[sn\_itam\_common\_asset\_onboarding\_task\] table tracks the asset onboarding process.

![Playbook for asset onboarding](../image/eam-playbook-layout.png)

## Multi-asset onboarding playbook

The multi-asset onboarding playbook enables you to onboard multiple assets for a single model at one go.

As an enterprise asset technician, you can perform any of the following tasks to onboard multiple assets:

-   [Create a catalog request](../task/create-asset-onboard-catalog-req.md).
-   [Create an Onboarding order in the Enterprise Asset Workspace](../task/onboard-eam-assets-workspace.md).

After the catalog request or the Onboarding order is submitted, an Onboard Asset Task is created. The enterprise asset manager can complete the Onboard Asset task by using the playbook associated with the task. After the onboarding task is completed, the catalog request and the requested item's state changes to **Closed Complete**.

The Multi-asset onboarding playbook has a series of activities that can be either skipped or marked as complete. The Deployment activity in the playbook enables the enterprise asset manager to specify the following details and create a deploy task:

-   The person for whom the asset is assigned
-   Location where the asset should be deployed

**Note:** You can work on the Deployment activity only after you have reviewed all the preceding activities in the Multi-asset onboarding playbook.

The deploy task for multi-asset onboarding can be either created as an Enterprise asset deployment task or a Work order task by configuring the **com.sn\_eam.default\_deployment\_task** asset property using the enterprise\_admin role. By default, the **Value** field of this asset property is set to **sn\_eam\_deploy\_asset\_task** and an Enterprise asset deployment task is created. However, you can create a work order task by setting the **Value** field to **wm\_task**.

For details on using the multi-asset playbook, see [Create a multi-asset onboarding process](../task/create-multi-asset-onboarding.md).

![Multi-asset playbook](../image/multi-asset-onboard.png)

## Calibration event playbook

The Calibration event playbook enables you to track and manage the asset calibrations that you are performing as part of your work orders. This playbook is available in any work order task that has a Work type of Calibration.

For more details on using the Calibration event playbook on your ServiceNow instance, see [Complete and close a work order for an enterprise asset](../task/complete-eam-work-order.md). For more details on using the Calibration event playbook in the ServiceNow® Mobile Agent® application, see [Take action on an enterprise asset using the Mobile Agent application](../task/complete-work-order-mobile-agent.md).

![Calibration event playbook on a ServiceNow instance.](../image/eam-calibration-playbook.png)

