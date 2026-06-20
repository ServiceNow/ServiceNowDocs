---
title: Receive certificate notifications via Microsoft Teams
description: Configure certificate notifications to be delivered to a Microsoft Teams channel so that you can receive alerts and initiate certificate renewal workflows directly from Microsoft Teams.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/configure-ms-teams-cert-notifications.html
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-06-20"
reading_time_minutes: 1
keywords: [configure Microsoft Teams CIM notifications, certificate expiration Teams channel, CIM Teams spoke setup]
breadcrumb: [Certificate alerts and notifications, Configuring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Receive certificate notifications via Microsoft Teams

Configure certificate notifications to be delivered to a Microsoft Teams channel so that you can receive alerts and initiate certificate renewal workflows directly from Microsoft Teams.

## Before you begin

Verify that the Microsoft Teams spoke is installed and configured. For more information, see .

Role required: pki\_admin or admin.

## About this task

The Microsoft Teams integration uses the ServiceNow Microsoft Teams spoke to deliver notifications. A scheduled job in Certificate Inventory and Management regularly checks the expiry dates of certificates stored in the **valid\_to** field of the Certificate \[cmdb\_ci\_certificate\] table. When certificates expire or are nearing expiration, the system triggers a subflow that sends notifications to the configured Microsoft Teams channel.

## Procedure

1.  Navigate to **Workspaces** &gt; **Certificate Management**.

2.  Select **Settings** from the menu bar and then select the **MS Teams Channel** tab.

3.  Enter the details of the Microsoft Teams channel.

    |Field|Description|
    |-----|-----------|
    |Channel alias|Alias for the channel.|
    |Microsoft teams channel link|URL to the Microsoft Teams channel.|
    |Microsoft team name|Name of the team the Microsoft Teams channel is associated with.|
    |Microsoft channel name|Name of the Microsoft Teams channel.|

4.  Select **Add**.

    The Microsoft Teams channel is added to the Certificate Microsoft Teams channel \[sn\_disco\_certmgmt\_microsoft\_teams\_channel\] table.

5.  Configure the type of notifications the Microsoft Teams channel receives.

    1.  Select the **Notification** tab.

        The available notification types in the **Certificate notification policy** \[sn\_disco\_certmgmt\_notification\_policy\] table are:

        -   Auto-Renewal Failed notification
        -   Certificate Completed Failed notification
        -   Certificate Expired notification
        -   Certificate Expiring notification
        -   Certificate Renewal Task Created notification
        -   Certificate Task Creation notification
    2.  Select the Edit form icon \[Omitted image "edit-icon-workspace.png"\] Alt text: for the relevant notification type.

    3.  Enable Microsoft Teams channel notifications for the notification type by selecting the **MS Teams enabled** check box.

    4.  Select the **MS Teams channel** field and then select the relevant channel you want to notify.

    5.  Select **Update**.


## Result

Certificate notifications are sent to the relevant Microsoft Teams channel as configured for each notification type.

**Parent Topic:**[Certificate alerts and notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/cert-inventory-mgmt-workflow.md)

