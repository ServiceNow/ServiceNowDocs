---
title: Create an asset onboarding process
description: Create an asset onboarding process to walk you through the process of entering important information for assets.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create and manage enterprise assets, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Create an asset onboarding process

Create an asset onboarding process to walk you through the process of entering important information for assets.

## Before you begin

The asset onboarding process is a playbook experience that provides an interactive user interface to complete a process. The asset onboarding process is triggered after an onboarding task is created. An onboarding task can be automatically created from the asset request flow or manually created from an asset record.

Onboarding is available only for preassembled and simple assets. Also, only the parent preassembled asset can be onboarded; not the child preassembled assets.

The asset onboarding process is organized into lanes. The lanes appear in the left pane of the page. Each lane includes a few activities that you’re asked to complete. Use the following buttons to skip, save, or complete a task:

-   **Skip**: takes you to the next activity.
-   **Save**: saves the information but doesn't complete the activity.
-   **Mark as complete**: saves the information and completes the activity, and takes you to the next lane.

**Note:** You can close an onboarding task only after you’ve skipped all the activities or marked all them as complete.

While you’re performing a particular activity, a status of **In progress** appears for that activity. As you mark an activity complete, the status of that activity changes to complete. After you complete all the activities in a lane, you move to the next lane.

The **Onboard asset** button that triggers an onboarding task only appears when the asset is in any one of the following states or substates as listed in the following table.

<table id="table_l51_1zf_zwb"><thead><tr><th>

State

</th><th>

Substates

</th></tr></thead><tbody><tr><td>

-   Build
-   In use
-   In stock
-   In maintenance

</td><td>

-   Available
-   Reserved
-   Pending Install
-   Pending transfer

</td></tr></tbody>
</table>Role required: sn\_eam.enterprise\_asset\_manager

## Procedure

1.  Navigate to **Enterprise Asset Workspace** &gt; **Enterprise asset estate**.

2.  Open the asset record for which you want to create an onboarding process.

3.  Select **Onboard asset**.

    The asset onboarding task opens.

4.  Select the **Onboarding playbook** related list tab.

    The asset onboarding page opens.

5.  Review or enter details in the Asset details lane.

    **Note:** If you’re onboarding a preassembled industrial asset, the **MAC address** field is included in the Asset details. Also, the **Child assets** activity under Asset details is displayed only for preassembled industrial assets.

    If you have activated the OT Asset Management application, the Asset details activity displays the **MAC address** field for preassembled industrial assets and the hardware assets.

6.  Select **Skip**, **Save**, or **Mark as complete** to proceed to the next lane.

7.  Continue to review or enter details in the lanes until you reach the last lane.

8.  After all the lanes show a status of skipped or complete, select **Close Task** to complete the asset onboarding process.

    Your asset is successfully onboarded.


-   **[View an automatically created onboarding task](view-auto-onboard-task.md)**  
View an automatically created asset onboarding task.

**Parent Topic:**[Create and manage enterprise assets](../concept/create-manage-enterprise-assets.md)

