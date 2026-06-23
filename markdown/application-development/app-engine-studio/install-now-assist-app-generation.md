---
title: Install Now Assist for app generation to use with AES
description: 
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-development/app-engine-studio/install-now-assist-app-generation.html
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring app generation in AES, Now Assist for app generation in AES, Create your app, Building apps in App Engine Studio, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Install Now Assist for app generation to use with AES

## Before you begin

Review the [Now Assist for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application listing in the ServiceNow Store to learn about dependencies, licensing, and subscription requirements, and release compatibility. Now Assist for Creator installs the Now Assist for app generation application.

**Note:** If you using a Xanadu Store Release 2 instance, Now Assist for app generation works with ServiceNow Studio \(not App Engine Studio\). For detailed information, see [Now Assist for app generation in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/servicenow-studio-classic/sns-now-assist-app-gen-landing.md).

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

        \[Omitted image "install-now-assist-app-skill.png"\] Alt text: App Generation Card that displays the app generation skill in the Now Assist Admin console.

    For more information about using the Now Assist Admin console to access information about setting up, configuring, and monitoring Now Assist applications, see [Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/intelligent-experiences/enable-ai-experiences/configuring-now-assist.md).


## What to do next

Grant the admin and now.assist.creator roles to each user that you want to create and edit applications using app generation.

To begin generating applications, see [Generate apps with Now Assist for Creator for use with AES](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/app-engine-studio/generate-apps-from-prompts.md).

**Parent Topic:**[Configuring app generation in AES](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/app-engine-studio/configuring-now-assist-app.md)

**Related topics**  


[Install Now Assist for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/build-workflows/now-assist-for-creator/install-now-assist-for-creator.md)

