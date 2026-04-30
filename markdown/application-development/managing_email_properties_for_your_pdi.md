---
title: Managing email properties for your PDI
description: Configure properties within your PDI to start sending and receiving emails.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Personal developer instance guide, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Managing email properties for your PDI

Configure properties within your PDI to start sending and receiving emails.

## Before you begin

Role required: none

## About this task

ServiceNow® instances can send and receive email. Configuring email is typically the responsibility of a system administrator, not an application developer. In order to send and receive email with your PDI, email sending and receiving needs to be configured.

Unfortunately, personal developer instances \(PDI\) have been used both accidentally and maliciously to send email spam. In order to prevent spamming but still allow notifications on PDIs, we have restricted our email servers to sending to a single domain, [guerrillamail.com](https://guerrillamail.com/). PDIs can receive email from any domain except guerrillamail.com.

## Procedure

1.  To enable email sending and receiving from the Developer Site:

    1.  Open the **Account** menu to access the **My Instance** section.

    2.  Click the **Manage Email Properties** instance action.

    3.  In the **Your instance actions** dialog, activate the **Enable email sending and receiving** toggle.

        ![Manage email properties for an instance](../image/manage-email-properties-pdi.png)

    4.  Click the **Save** button.

2.  To disable email sending and receiving, deactivate the **Enable email sending and receiving** toggle.


**Parent Topic:**[Personal developer instance guide](../concept/personal_developer_instance_guide.md)

