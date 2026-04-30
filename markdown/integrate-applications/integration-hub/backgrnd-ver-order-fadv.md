---
title: Initiate background verification in First Advantage from ServiceNow using order
description: Initiate background verification of the required candidate by sending an email requesting for the essential information.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [First Advantage Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Initiate background verification in First Advantage from ServiceNow using order

Initiate background verification of the required candidate by sending an email requesting for the essential information.

## Before you begin

-   [Create a case in First Advantage from ServiceNow](create-fadv-case.md)

    **Note:** Ensure that the **Send Invite link** and **Use "Order As"** options aren't selected.

-   Role required: First Advantage admin or First Advantage user

## About this task

An order is initiated when First Advantage has all basic information about the candidate and requires only some essential sensitive information.

## Procedure

1.  Navigate to **All** &gt; **First Advantage Spoke** &gt; **First Advantage Cases**.

2.  Search for the required task.

3.  Ensure that the **Send Invite link** and **Use "Order As"** options aren't selected.

4.  Change the **State** of the task from **Draft** to **Ready**.

    -   The First Advantage - Candidate Background Verification using Order flow is triggered.
    -   **State** is changed to **In Progress**.
    -   In the **Order History** tab, a record is created and its details such as **Order ID**, **Number**, **Short Description** and so on, are populated.
    -   Real-time updates and System Administrator events are displayed in the **Order Details** tab.

        **Note:** The **Order History** tab displays all the order records created for the user.

    -   An order email is sent to the candidate.

## Result

A mail is sent to candidate requesting only the sensitive information. Real-time updates and guest events are displayed in the **Order Details** tab. First Advantage approves, cancels, or rejects the task after performing the background verification.

**Note:** You must set up the webhooks to receive the guest event updates. See [Set up First Advantage webhooks](setup-first-adv.md#) for information on setting up the webhooks.

