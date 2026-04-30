---
title: Configure notifications for ERP Semantic Mining tasks
description: Enable notifications to find out when ERP Semantic Mining succeeds or fails in a mining job for the ERP \(Enterprise Resource Planning\) system of record.
locale: en-US
release: zurich
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, ERP Semantic Mining overview, Workflow Data Fabric]
---

# Configure notifications for ERP Semantic Mining tasks

Enable notifications to find out when ERP Semantic Mining succeeds or fails in a mining job for the ERP \(Enterprise Resource Planning\) system of record.

## Before you begin

**Important:** Starting with the Zurich release, ERP Semantic Mining is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

Before you can set up notifications for yourself, your admin must add you to the ERP Semantic Mining Notification group.

Role required: sn\_erp\_mining.erp\_admin, sn\_erp\_mining.erp\_user

## About this task

For general information on preferences, see [System and custom notification and delivery channel preferences in Next Experience](https://www.servicenow.com/docs/access?context=advanced-notification-prefrences&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Procedure

1.  From your user profile, navigate to **Preferences**.

2.  Select the **Notifications** card.

3.  Enable the toggle for **Custom Notifications** in **General Settings**.

4.  Select the open in new tab icon for **Custom Notifications**.

5.  Select the **Create notification** button.

6.  Enter the basic details for the notification in the **Select notification** section of the **Create Notification** modal.

<table id="table_scg_x5p_cbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Personal notification name

</td><td>

Descriptive name for the notification you're setting up. For example, `Ann's ERP failure email notification`.

</td></tr><tr><td>

Notification

</td><td>

Select the notification that you want. The options are:-   **ERP Extraction Completion Notification**
-   **ERP Extraction Failure Notification**


</td></tr></tbody>
</table>7.  Select the **Next** button.

8.  Select the delivery channel.

    1.  Expand the method for how you want to be notified, such as **Email**.

    2.  Enable the toggle for the email address that you want to receive the notification.

        Email addresses must already be associated with your ServiceNow AI Platform user account.

    3.  Select the **Next** button.

9.  Select the **Schedule** for your notification.

10. Finish setting up the notification by selecting the **Save** button.


## Result

The notification email that you receive contains a link that takes you to the record for the job. You can view the progress of its tasks by selecting the **Show training progress** Related Link. The tasks there also appear in the Connection tasks overview lists on the **Overview** tab of the Connection status page. You could then select to **Show matching** on a day's **Task period** value in the Connection tasks overview list to see the status of all tasks for that day.

**Parent Topic:**[Configuring ERP Semantic Mining](../concept/configuring-ecm.md)

