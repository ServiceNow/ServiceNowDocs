---
title: Receive certificate notifications on Slack
description: In Version 1.2.0 of Certificate Inventory and Management, set up Slack notifications to stay informed about expiring and expired certificates. Receive detailed alerts with convenient URL links for additional information.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Certificate integrations and notifications, Configuring Certificate Inventory and Management, Certificate Inventory and Management, Discovery, ITOM Visibility, IT Operations Management]
---

# Receive certificate notifications on Slack

In Version 1.2.0 of Certificate Inventory and Management, set up Slack notifications to stay informed about expiring and expired certificates. Receive detailed alerts with convenient URL links for additional information.

## Before you begin

Role required: admin

## About this task

A scheduled job in Certificate Inventory and Management regularly checks the expiry dates of certificates stored in the valid\_to field of the cmdb\_ci\_certificate table. When certificates are either expired or nearing expiration, the job initiates the subflow Process Slack Message, which subsequently sends notifications to the designated Slack channel.

## Procedure

1.  [Set up Slack spoke](https://www.servicenow.com/docs/access?context=set-up-slack&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

2.  Create a [Slack bot](https://api.slack.com/bot-users) and add it to a Slack channel.

3.  [Configure default Slack credentials](https://www.servicenow.com/docs/access?context=set-up-slack&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

4.  [Configure custom Slack credentials](https://www.servicenow.com/docs/access?context=set-up-slack&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

    If your Slack spoke version is 1.2.0, you can bypass the next step concerning the retrieval of the Channel ID.

5.  Get the ID for your Slack channel.

    1.  Go to **Slack**.

    2.  Right-click the Channel.

    3.  Select **Additional options** &gt; **Copy link**.

    4.  From the provided link, copy the string following &lt;archive/&gt;.

6.  Configure the Slack Channel ID property.

    1.  Navigate to **Discovery** &gt; **Properties**.

    2.  Enter value in the Slack Channel ID property **glide.discovery.certs.slack\_channel\_id**.

7.  Select **Save**.


## Result

Notifications are directed to the Slack channel specified in Discovery properties. If a certificate is assigned to a user, and their configured email matches the Slack email, the user is tagged in the Slack message. The Slack scheduled job runs weekly, and you can adjust its frequency by modifying the Certificate Notification scheduled job settings.

**Parent Topic:**[Certificate integrations and notifications](../concept/cert-inventory-mgmt-workflow.md)

