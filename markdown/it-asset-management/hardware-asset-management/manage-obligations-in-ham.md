---
title: Manage obligations in the Hardware Asset Workspace
description: Obligation Management in the Hardware Asset Workspace enables you to create obligation records to define specific instructions and obligation task types required to fulfill a contract obligation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/manage-obligations-in-ham.html
release: brazil
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Asset lifecycle and disposal, Use, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Manage obligations in the Hardware Asset Workspace

Obligation Management in the Hardware Asset Workspace enables you to create obligation records to define specific instructions and obligation task types required to fulfill a contract obligation.

Hardware contracts such as leases, warranties, maintenance agreements, and purchase agreements each include specific commitments. Without proper tracking, organizations risk:

-   Missing renewal deadlines
-   Failing to verify vendor service level performance
-   Paying for repairs covered under warranty
-   Incurring penalties from missed purchase obligations

With Obligation Management in the Hardware Asset Workspace, contract managers can create, assign, and complete contractual obligations from a single workspace. For details, see [Hardware Asset Management integration with Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/ham-cm-pro-integration.md).

**Note:** You can also use the Manage contract repository agentic workflow to extract obligations from signed contracts and create obligation records automatically. For more details, see [Initiate metadata and obligation extraction from a signed contract in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/initiate-metadata-extraction-ham.md) and [Review AI-extracted obligations in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/review-extracted-obligation-ham.md).

## Obligation task types

-   **Ad hoc obligation task**

    An obligation task that is required only once or at irregular intervals to fulfill the contract obligations.

-   **Recurring obligation task**

    An obligation task that is required at regular intervals to fulfill contract obligations. Recurring obligation tasks are created automatically based on the defined schedule. When you select this task type, the **Frequency** and **Lead time** fields appear on the obligation task record. The lead time determines how many days before the due date each task is created.


## Roles

The following roles support Obligation Management in the Hardware Asset Workspace.

|Role|Description|
|----|-----------|
|sn\_cm\_obligation.obligation\_admin|Provides administrative access to Obligation Management and underlying data.|
|sn\_cm\_obligation.obligation\_fulfiller|Creates obligations and approves, rejects, or cancels obligation tasks within the Hardware Asset Workspace.|
|sn\_cm\_obligation.obligation\_user|Acts on the assigned obligation task and submits the task within Hardware Asset Workspace.|

## Obligation Management workflow

The following workflow describes how users create and manage obligations for hardware contracts.

1.  A user with the sn\_cm\_obligation.obligation\_fulfiller role creates an obligation record on a hardware contract, specifying the obligation name, category, assignee, dates, instructions, and task type.
2.  The user with the sn\_cm\_obligation.obligation\_fulfiller role also creates one or more obligation tasks. Each task inherits fields from the parent obligation record and requires a due date that falls within the obligation start and end dates.
3.  When an obligation task is saved, the system sends an email notification to the assigned user with the sn\_cm\_obligation.obligation\_user role.
4.  The assigned user reviews and submits the obligation task in the Employee Center. The obligation task moves to the **Awaiting Approval** state. For more information, see [Create obligations manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/cncore-work-on-ob-tasks.md).
5.  The approver with the sn\_cm\_obligation.obligation\_fulfiller role reviews and approves the task. For more information, see [Approve or reject obligation tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/cncore-manage-ob-tasks.md).
6.  After approval, the obligation task moves to the **Closed Complete** state.

-   **[Create an obligation record in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/create-obligation-records-ham.md)**  
Create an obligation record for signed contracts in the Hardware Asset Workspace to fulfill the responsibilities specified in the contract through obligation tasks.

**Parent Topic:**[Asset lifecycle and disposal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/asset-lifecycle-disposal-ham.md)

**Related topics**  


[Request a Hardware Asset Refresh]()

[Manage refresh of assets using Zero Touch Refresh]()

[Manage your expiring contracts for leased hardware assets]()

[Reclaim hardware assets]()

[Create a disposal order]()

[Donate assets to charity organizations]()

[Manage asset bundles from your inventory]()

[Manage contract repository agentic workflow in the Hardware Asset Workspace]()

