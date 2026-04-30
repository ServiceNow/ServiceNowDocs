---
title: Configure the self-registration feature on the Patient Portal
description: Enable or disable the self-registration feature on the Patient Portal by setting the value of the Enables self registration on Healthcare patient Portal property \(sn\_hcls.enable\_self\_registration\).
locale: en-US
release: xanadu
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring the Patient Portal, Configuring Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configure the self-registration feature on the Patient Portal

Enable or disable the self-registration feature on the Patient Portal by setting the value of the **Enables self registration on Healthcare patient Portal** property \(**sn\_hcls.enable\_self\_registration**\).

## Before you begin

Set the application scope to Healthcare and Life Sciences using the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

Role required: admin

## Procedure

1.  Enter `sys_properties.list` in the navigation filter, and then open the **sn\_hcls.enable\_self\_registration** property.

2.  In the **Value** field, enter the required value.

    -   Enter `true` to enable the self-registration feature in the Patient Portal.
    -   Enter `false` to disable the self-registration feature in the Patient Portal.
3.  Click **Update**.


