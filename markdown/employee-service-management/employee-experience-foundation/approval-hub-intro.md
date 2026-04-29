---
title: Approvals hub
description: Enable the approver with the in-context information for informed and prioritized approval decisions.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setup task management, Configuring Employee Center Pro, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Approvals hub

Enable the approver with the in-context information for informed and prioritized approval decisions.

Use the approval templates with common info, primary info, tabs, and action groups to make informed decisions. You can configure individual approval types to display the request-specific information, while still having a consistent layout that is similar to other approval types.

Improve productivity with a unified approvals inbox. You can manage requests from internal and external applications from one location. Approvers can approve or send back Concur expenses to the requester right from Employee Center Pro with a configurable omni-channel experience.

## Configurable experience

Enhance employee and approver experience by configuring the information and actions for each approval type.

## Unified approvals inbox

Manage all your approvals from a unified location across business applications such as SAP Concur and Workday without switching the tools.​

## Omni-channel approvals

Meet employees where they are for approval management from all channels such as NowMobile, Outlook, and MS Teams.

## Approvals user and roles

|User roles|Required role|
|----------|-------------|
|Approvals admin|sn\_hr\_sp.esc\_admin|
|ESM framework admin|sn\_hr\_integr\_fw.admin|
|Workday admin|sn\_hr\_workday.admin|
|Flow designer admin|flow\_designer|

**Note:**

-   The approver\_user or the business\_stakeholder role is required to be able to approve or reject items on the Employee Center Pro portal.
-   The sn\_request\_read and sn\_request\_approver\_read are read-only roles.

For more information, see [Approvals hub integration with SAP Concur](x-concur-sa-integration.md) and [Approvals hub integration with Workday](wd-ec-integration.md).

## How external integration works

Approvals hub integration enables you to share data between the two platforms, automate processes, and improve efficiency. Here are the steps involved in integrating ServiceNow and external applications such as SAP Concur and Workday.

Here is what an administrator can do.

-   **As an administrator**
    -   Use prebuilt integrations and the ability to build custom integrations.
    -   Pull external data and transform it for display on Employee Center Pro.
    -   Use the default to-dos configuration and task configuration to customize the approval flows.
    -   Enable quick actions to process the request.
    -   Sync data and status between the applications.

Here is what an approver can do.

-   **As an approver**
    -   View and manage open and assigned requests from ServiceNow and external applications from a unified location.
    -   Make approval decisions based on the contextual information as configured in the to-dos configuration and task configuration.
    -   Perform quick actions to process the request.

Here is what an employee can do.

-   **As an employee**
    -   Submit your approval requests from any internal and external applications.
    -   View progress or status of the request.

For more information, see [Approvals experience reference](../reference/approval-hub-ootb.md) and [Use approval experience](../task/ec-to-dos-use-approval-hub.md).

