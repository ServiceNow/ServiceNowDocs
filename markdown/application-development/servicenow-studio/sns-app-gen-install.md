---
title: Install Now Assist for app generation in ServiceNow Studio
description: Install the Now Assist for Creator application so that you can get started with creating an application for your organization.
locale: en-US
release: yokohama
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [agentic ai, app gen, app generation, now assist, application generation, app creation, application creation, servicenow studio, generative ai]
breadcrumb: [Configuring Now Assist for app generation in ServiceNow Studio, Now Assist for app generation in ServiceNow Studio, Using ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# Install Now Assist for app generation in ServiceNow Studio

Install the Now Assist for Creator application so that you can get started with creating an application for your organization.

## Before you begin

Role required: admin

## Procedure

1.  Go to the [Now Assist for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application listing in the ServiceNow Store.

2.  Review the listing to learn about dependencies, licensing, subscription requirements, and release compatibility.

    In the listing, see that Now Assist for Creator includes Now Assist application generation.

    ![Now Assist for Creator listing in the ServiceNow Store with application generation skill highlighted.](../images/app-generation-install-na-creator.png)

3.  On the Now Assist for Creator application page, select **Buy**.

4.  After your request is approved, open your instance and navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

5.  Find and select the Now Assist for Creator application \(sn\_now\_creator\) by using the filter criteria and search bar.

6.  Select **Install**.

7.  Verify that Now Assist for Creator is installed.

    1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Experiences**.

    2.  In the workflow list, select **Creator**.

    3.  On the App Generation card, verify that the app generation skill is active.

        ![App Generation Card that displays the app generation skill on the Now Assist Admin skills tab.](../images/install-now-assist-app-skill-ys2.png)

        If app generation is not active, select **Turn on**.

        ![App generation skill card with turn on button highlighted.](../images/app-generation-install-turn-on-button-ys2.png)

    For more information about setting up, configuring, and monitoring Now Assist, see [Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

8.  Activate the Now Assist panel.

    1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Experiences**.

    2.  In **Summary**, select **Turn on**.

        ![Now Assist experience tab with summary and turn on button highlighted.](../images/app-generation-nap-activate1.png)

    3.  In the confirmation, select **Turn on**.

    4.  Close the success message by selecting the **X**.

    5.  In **Summary**, select the **CI Admin console** link.

        ![Now Assist panel page with summary and CI Admin console link highlighted.](../images/app-generation-nap-activate2.png)

    6.  If the **Status** of **Now Assist Panel - Platform \(default\)** is **Off**, select the actions icon, and then select **Turn on/off**.

        ![Now Assist assistants page with Now Assist Panel - Platform (default) option and action icon highlighted.](../images/app-generation-nap-activate3.png)


## What to do next

Grant the now.assist.creator role, the now\_assist\_panel\_user role, and either the admin or sn\_g\_app\_creator.app\_creator role to each user that you want to create and edit applications using app generation.

Users that only need to edit \(not create\) applications using app generation can be granted the delegated\_developer, now\_assist\_panel\_user, and now.assist.creator roles. For more information, see [Delegated development and deployment](../../applications/concept/c_DelegatedDevelopment.md).

To begin generating applications, see [Generate apps with Now Assist for app generation within ServiceNow Studio](sns-app-gen-using-landing.md).

**Parent Topic:**[Configuring Now Assist for app generation in ServiceNow Studio](../concept/sns-app-gen-config-landing.md)

**Related topics**  


[Install Now Assist for Creator](https://www.servicenow.com/docs/access?context=install-now-assist-for-creator&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)

