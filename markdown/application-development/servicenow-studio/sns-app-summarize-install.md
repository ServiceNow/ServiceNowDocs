---
title: Install Now Assist for app summary generation
description: Install the Now Assist for Creator application so that you can use app summary generation for your organization.
locale: en-US
release: zurich
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Now Assist, generative AI]
breadcrumb: [Configuring, Now Assist for app summary generation in ServiceNow Studio, Working with Now Assist tools and AI files, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Install Now Assist for app summary generation

Install the Now Assist for Creator application so that you can use app summary generation for your organization.

## Before you begin

Review the [Now Assist for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application listing in the ServiceNow Store to learn about dependencies, licensing, and subscription requirements, and release compatibility. Now Assist for Creator installs the Now Assist for app summary generation skill.

**Note:** The Now Assist table summary generation skill must also be active to use the app summary generation skill.

Role required: admin

## Procedure

1.  Search for and open the [Now Assist for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application.

2.  On the Now Assist for Creator application page, select **Get**.

3.  After your request is approved, navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

4.  Find and select the Now Assist for Creator application \(sn\_now\_creator\) by using the filter criteria and search bar.

5.  Select **Install**.

6.  Verify that Now Assist for Creator is installed.

    1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Features**.

    2.  In the workflow list, select **Creator**.

    3.  Verify that the app summary generation skill and the table summary generation skill are active by selecting **View details** on the **App** card.

    For more information about using the Now Assist Admin console to access information about setting up, configuring, and monitoring Now Assist applications, see [Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).


## What to do next

Assign the admin, sn\_app\_summary.app\_summary\_user, or sn\_g\_app\_creator.app\_creator roles to users who want to generate app summaries.

To summarize an app, see [Summarize the contents of an app in ServiceNow Studio](../../servicenow-studio/task/summarize-an-app-in-servicenow-studio.md).

**Parent Topic:**[Configuring Now Assist for app summary generation](../concept/sns-config-now-assis-app-summarize.md)

