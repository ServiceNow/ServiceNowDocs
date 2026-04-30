---
title: Initiate background verification in First Advantage from ServiceNow using invite
description: Initiate background verification of the required candidate by sending a request to complete an application through an invite email.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [First Advantage Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Initiate background verification in First Advantage from ServiceNow using invite

Initiate background verification of the required candidate by sending a request to complete an application through an invite email.

## Before you begin

-   [Create a case in First Advantage from ServiceNow](create-fadv-case.md)

    **Note:** Ensure that the **Send Invite link** option is selected and the **Use "Order As"** option isn't selected.

-   Role required: First Advantage admin or First Advantage user

## Procedure

1.  Navigate to **All** &gt; **First Advantage Spoke** &gt; **First Advantage Cases**.

2.  Search for the required task.

3.  Ensure that the **Send Invite link** option is selected and the **Use "Order As"** option isn't selected.

4.  Change the **State** of the task from **Draft** to **Ready**.

    -   The First Advantage - Candidate Background Verification using Invite flow is triggered.
    -   **State** is changed to **In Progress**.
    -   In the **Employee Tasks** tab, a record is created and its details such as **Number**, **Invite ID** and so on, are populated. Open the record to access details such as **Invite URL**, **Candidate ID**, and so on. Also, real-time updates are displayed here.

        **Note:** The **Employee Tasks** tab displays all the invite records created for the user.

    -   In the **Order History** tab, a record is created and its details such as **Number**, **Short Description** and so on, are populated.

        **Note:** The **Order History** tab displays all the order records created for the user.

    -   Real-time updates and System Administrator events are displayed in the **Order Details** tab.

        **Note:** **Order ID** is populated only after the invite is executed successfully. For example, **Order ID** isn't populated if the candidate has declined to complete the application form.

    -   An invite email is sent to the candidate.

## Result

After accessing the invite email, candidate can either complete the application form or decline. If candidate fills and submits the application form,First Advantage approves, cancels, or rejects the task after performing the background verification.

-   The status and all other details can be accessed in real-time by navigating to **First Advantage Spoke** &gt; **Employee Tasks**.
-   Guest events are displayed in the respective First Advantage Employee Task record.

**Note:**

-   You must set up the webhooks to receive the guest event updates. See [Set up First Advantage webhooks](setup-first-adv.md#) for information on setting up the webhooks.
-   If the candidate has declined the request for background verification, the Order record isn't created for the task.

