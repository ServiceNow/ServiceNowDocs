---
title: Create a connection with Microsoft Exchange Online
description: Integrate the Career Conversations ServiceNow instance and Microsoft Exchange Online account by creating a custom OAuth application in Microsoft Exchange Online to authenticate ServiceNow requests.
locale: en-US
release: australia
product: Career Conversations
classification: career-conversations
topic_type: task
last_updated: "2025-12-02"
reading_time_minutes: 1
breadcrumb: [Set up Microsoft Outlook integration in Career Conversations, Install and configure Career Conversations, Career Conversations, Growth Experiences, HR Service Delivery, Employee Service Management]
---

# Create a connection with Microsoft Exchange Online

Integrate the Career Conversations ServiceNow instance and Microsoft Exchange Online account by creating a custom OAuth application in Microsoft Exchange Online to authenticate ServiceNow requests.

## Before you begin

Role required: admin

## About this task

Set up conversations and sync them with Microsoft Outlook using a connection with the Microsoft Exchange Online spoke.

## Procedure

1.  Ensure that the Microsoft Exchange Online spoke is installed.

2.  Set up Microsoft Exchange Online spoke.

    If you are a new customer, in the **Create Connection records for the Microsoft Exchange Online spoke** procedure, perform the following actions:

    -   For **Microsoft\_Exchange\_Online** Connection and Credential alias, in the Connection related list, select **MS Graph 1** and make the changes.

        Do not change the **Name** and **Credential**. In the OAuth Entity Profile form of the **MS Graph 1** credential, ensure that the **Grant type** field is selected as **Client Credentials**.

    -   For **Microsoft\_Exchange\_Online\_clientCred** Connection and Credential alias, in the Connection related list, select **MS Graph 2** and make the changes.

        Do not change the **Name** and **Credential**. In the OAuth Entity Profile form of the **MS Graph 2** credential, ensure that the **Grant type** field is selected as **Client Credentials**.


**Parent Topic:**[Set up Microsoft Outlook integration in Career Conversations](../concept/outlook-integration-cc.md)

