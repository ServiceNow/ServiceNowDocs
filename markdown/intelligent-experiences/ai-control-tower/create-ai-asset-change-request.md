---
title: Create change request for AI assets
description: Create change request to modify a relationship between a deployed AI asset and one of its related assets.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2025-11-05"
reading_time_minutes: 2
breadcrumb: [Creating requests for AI assets, Using AI Control Tower, AI Control Tower, Enable AI experiences]
---

# Create change request for AI assets

Create change request to modify a relationship between a deployed AI asset and one of its related assets.

## Before you begin

Role required:

-   AI steward \[sn\_ai\_governance\_ai\_steward\]
-   AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]

## About this task

Change requests can be created for AI systems and AI models and need to be approved by the AI steward role. Once a change request is approved, a new AI asset record is created that automatically starts the onboarding process.

## Procedure

1.  Navigate to **Workspaces** &gt; **AI Control Tower**.

2.  From AI Control Tower workspace home view, select **Create request** &gt; **Create change request**

    You can also navigate to **Create change request** from the following two paths:

    -   Go to AI assets view and select **Requests** &gt; **Change requests** and then select **Create change request**.
    -   Open a deployed AI system or AI model and select **Create request** &gt; **Create change request**. In this scenario, the asset details are already pre-populated.

        **Note:** The **Create request** option appears only when both the life cycle phase and life cycle status are set to **Deployed**.

    The New change request page opens.

3.  Enter the new version number of the asset in the **Version** field.

4.  Enter the due date by which the change should be made by in the **Due date** field.

5.  Enter a justification for creating the change request in the **Justification** field.

6.  Enter the other required fields, which differ depending on whether the change request is for an AI system or an AI model.

    AI systems doesn't support sub AI systems and inputs and outputs. So if the change request is for an AI system, the New change request page shows fields for AI models, AI prompts, and Evaluation dataset. If the change request is for an AI model, the page shows fields for Base model, training dataset, and Evaluation dataset.

7.  Select **Submit for review**.

    All the fields on the New change request page become read only and the status of the asset record changes to **Requested** and the state changes to **Open**. An Impacted assets list appears that shows all AI assets that will be impacted by this change request. If an AI system or an AI model isn’t being used by other AI systems or AI models, then the Impacted asset list is empty.

8.  Log in as the AI steward role to approve the request.

9.  In the **Assigned to** field, assign it to yourself or to any other AI steward role.

    All the other fields in the page continue to be read only.

10. Approve or reject the request.

    -   If you select Approve, the status of the request changes to **Approved** and the state changes to**In progress**. A Change tasks list appears that shows change tasks for each impacted asset. Additionally, if the AI steward role wants further clarifications on this request or has any concerns, the AI steward role can create a change task and assign it to an AI asset owner. The assigned AI asset owner needs to log in and complete all the change task. The new AI asset shows up in the **Updated AI asset** field of the change request.
    -   If you select **Reject**, The status of the request changes to **Rejected**, no new AI asset is created, and the state changes to**Completed**
    Once all the change tasks have been completed by the AI asset owner, the state of the request changes to **Completed**.


**Parent Topic:**[Creating requests for AI assets](../concept/creating-ai-asset-requests.md)

