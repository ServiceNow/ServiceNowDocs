---
title: Getting notifications for ERP Semantic Mining connection updates
description: ERP Semantic Mining can email you about the success and failures of ERP \(Enterprise Resource Planning\) system connections.
locale: en-US
release: australia
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, ERP Semantic Mining overview, Workflow Data Fabric]
---

# Getting notifications for ERP Semantic Mining connection updates

ERP Semantic Mining can email you about the success and failures of ERP \(Enterprise Resource Planning\) system connections.

**Important:** Starting with the Zurich release, ERP Semantic Mining is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

## Notifications for success and failure

ERP Semantic Mining jobs run to find candidates for replatforming. With notifications, you can get an email when a mining task succeeds or fails.

-   Success notifications indicate that all the mining tasks have finished running with no errors.
-   Failure notifications indicate that one or more of the mining tasks are in error status.

The notification email that you receive contains a link that takes you to the record for the job. You can view the progress of its tasks by selecting the **Show training progress** Related Link. The tasks there also appear in the Connection tasks overview lists on the **Overview** tab of the Connection status page. You could then select to **Show matching** on a day's **Task period** value in the Connection tasks overview list to see the status of all tasks for that day.

## Selecting your email notifications

Notification emails aren’t enabled by default, and you must configure them for yourself in your ServiceNow AI Platform preferences. For details on configuring notifications, see [Configure notifications for ERP Semantic Mining tasks](../task/erpcm-enable-notifications.md).

Before you can set up notifications for yourself, your admin must add you to the ERP Semantic Mining Notification group. For more information, see [Add a user to a group](https://www.servicenow.com/docs/access?context=t_AddAUserToAGroup&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Notifications also appear in the Notifications table

Notifications appear in the Notifications table, which you can access by navigating to **All** &gt; **System Notification** &gt; **Notifications**.

## Flow that runs notifications

The ECM Statistical Data Extractor flow in Workflow Studio runs automatically to power notifications. You can customize the flow in Workflow Studio. For more information, see [Edit a flow](https://www.servicenow.com/docs/access?context=flow-edit&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

**Parent Topic:**[Configuring ERP Semantic Mining](configuring-ecm.md)

