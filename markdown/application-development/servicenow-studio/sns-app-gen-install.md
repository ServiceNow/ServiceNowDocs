---
title: Install Now Assist for app generation in ServiceNow Studio
description: 
locale: en-US
release: xanadu
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2024-10-16"
reading_time_minutes: 1
keywords: [app gen, app generation, now assist, application generation, app creation, application creation, servicenow studio, generative ai]
breadcrumb: [Configuring app generation in ServiceNow Studio, Now Assist for app generation in ServiceNow Studio, Using ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# Install Now Assist for app generation in ServiceNow Studio

## Before you begin

Review the [Now Assist for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application listing in the ServiceNow Store to learn about dependencies, licensing, and subscription requirements, and release compatibility. Now Assist for Creator installs the Now Assist for app generation application.

Role required: admin

## Procedure

1.  Navigate to the [Now Assist for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application on the ServiceNow Store.

2.  On the Now Assist for Creator application page, select **Request App**.

3.  After your request is approved, navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

4.  Find the Now Assist for Creator application \(sn\_now\_creator\) by using the filter criteria and search bar.

5.  Select **Install**.

6.  Verify that Now Assist for Creator is installed.

    1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Features**.

    2.  In the workflow list, select **Creator**.

    3.  On the App Generation card, verify that the app generation skill is active.

        ![App Generation Card that displays the app generation skill in the Now Assist Admin console.](../../app-engine-studio/image/install-now-assist-app-skill.png)

    For more information about using the Now Assist Admin console to access information about setting up, configuring, and monitoring Now Assist applications, see [Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).


## What to do next

Grant the admin and now.assist.creator roles to each user that you want to create and edit applications using app generation.

As of Xanadu Store Release 2, users that only need to edit \(not create\) applications using app generation can be granted the delegated\_developer, now\_assist\_panel\_user, and now.assist.creator roles. For more information, see [Delegated development and deployment](../../applications/concept/c_DelegatedDevelopment.md).

To begin generating applications, see [Generate apps with Now Assist for Creator for ServiceNow Studio](sns-app-gen-using-landing.md).

**Parent Topic:**[Configuring app generation in ServiceNow Studio](../concept/sns-app-gen-config-landing.md)

**Related topics**  


[Install Now Assist for Creator](https://www.servicenow.com/docs/access?context=install-now-assist-for-creator&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)

