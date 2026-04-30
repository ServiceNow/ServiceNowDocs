---
title: Getting notifications for ERP Customization Mining connection updates
description: ERP Customization Mining \(ERP-CM\) can email you about the success and failures of ERP \(Enterprise Resource Planning\) system connections.
locale: en-US
release: xanadu
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring ERP Customization Mining, ERP Customization Mining \(ERP-CM\), Building low-code applications, Developing your application, Building applications]
---

# Getting notifications for ERP Customization Mining connection updates

ERP Customization Mining \(ERP-CM\) can email you about the success and failures of ERP \(Enterprise Resource Planning\) system connections.

## Notifications for success and failure

ERP-CM customization mining jobs run to find candidates for replatforming. With notifications, you can get an email when a customization mining task succeeds or fails.

-   Success notifications indicate that all the customization mining tasks have finished running with no errors.
-   Failure notifications indicate that one or more of the customization mining tasks are in error status.

The notification email you receive contains a link that takes you to the record for the customization mining job. You can view the progress of its tasks by selecting the **Show training progress** Related Link. The tasks there also appear in the Connection tasks overview list on the **Overview** tab of the Connection status page. You could then select to **Show matching** on a day's **Task period** value in the Connection tasks overview list to see the status of all tasks for that day.

## Selecting your email notifications

Notification emails aren’t enabled by default, and you must configure them for yourself in your ServiceNow AI Platform preferences. For details on configuring notifications, see [Configure notifications for ERP-CM tasks](../task/erpcm-enable-notifications.md).

Before you can set up notifications for yourself, your admin must add you to the ERP Customization Mining Notification group. For more information, see [Add a user to a group](https://www.servicenow.com/docs/access?context=t_AddAUserToAGroup&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Notifications also appear in the Notifications table

Notifications appear in the Notifications table, which you can access by navigating to **All** &gt; **System Notification** &gt; **Notifications**.

## Flow that runs notifications

The ECM Statistical Data Extractor flow in Workflow Studio runs automatically to power notifications. You don't need to do anything to activate the flow, but you can customize it in Workflow Studio. For more information, see [Edit a flow](https://www.servicenow.com/docs/access?context=flow-edit&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

**Parent Topic:**[Configuring ERP Customization Mining](configuring-ecm.md)

