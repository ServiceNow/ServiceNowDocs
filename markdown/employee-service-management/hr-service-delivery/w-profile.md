---
title: Synchronize worker profiles
description: Pull worker profile data from Workday into ServiceNow. View worker profile details from Workday in ServiceNow HR Service Delivery.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring HR Service Delivery Integration with Workday, HR Service Delivery Integration with Workday, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Synchronize worker profiles

Pull worker profile data from Workday into ServiceNow. View worker profile details from Workday in ServiceNow HR Service Delivery.

The following sections explain how to set up the application, configure worker profile settings, activate and run the schedule flow to synchronise worker profiles.

## Application setup

First, you must activate the HR Service Delivery Integration with Workday application from ServiceNow Store. This automatically activates the Workday HR Spoke. Next, you must set up [Workday HR Spoke](https://www.servicenow.com/docs/access?context=workday-hr-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

## Worker profile settings

Store one-time configuration parameters for synchronizing data between Workday and ServiceNow. For more information, see [Configure worker profile settings](../task/config-w-sync.md).

**Note:** Even if you are not using Worker profile synchronization, ensure that you have configured the **Workday tenant time zone** field in the Workday Worker Profile Sync Configurations form. This field handles the time zones between the two systems, ServiceNow and Workday.

## Schedule flow activation

Activate and run the schedule flow that pulls Worker profile information into ServiceNow. For more information, see [Activating schedule flows](../task/activate-w-schedule-flow.md).

