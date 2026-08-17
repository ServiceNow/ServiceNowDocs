---
title: Install ServiceNow Otto for app summary generation
description: Install the ServiceNow Otto for Creator application so that you can use app summary generation for your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/sns-app-summarize-install.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, generative AI]
breadcrumb: [Configuring, App summary generation, AI tools and files, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Install ServiceNow Otto for app summary generation

Install the ServiceNow Otto for Creator application so that you can use app summary generation for your organization.

## Before you begin

Review the [ServiceNow Otto for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application listing in the ServiceNow Store to learn about dependencies, licensing, and subscription requirements, and release compatibility. ServiceNow Otto for Creator installs the ServiceNow Otto for app summary generation skill.

**Note:** The ServiceNow Otto table summary generation skill must also be active to use the app summary generation skill.

Role required: admin

## Procedure

1.  Search for and open the [ServiceNow Otto for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application.

2.  On the ServiceNow Otto for Creator application page, select **Get**.

3.  After your request is approved, navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

4.  Find and select the ServiceNow Otto for Creator application \(sn\_now\_creator\) by using the filter criteria and search bar.

5.  Select **Install**.

6.  Verify that ServiceNow Otto for Creator is installed.

    1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Features**.

    2.  In the workflow list, select **Creator**.

    3.  Verify that the app summary generation skill and the table summary generation skill are active by selecting **View details** on the **App** card.

    For more information about using the AI Admin Hub to access information about setting up, configuring, and monitoring ServiceNow Otto applications, see [Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md).


## What to do next

Grant the admin and now.assist.creator roles, or the sn\_g\_app\_creator.app\_creator and now.assist.creator roles, to each user that you want to summarize apps.

To summarize an app, see [Summarize the contents of an app in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/summarize-an-app-in-servicenow-studio.md).

**Parent Topic:**[Configuring ServiceNow Otto for app summary generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sns-config-now-assis-app-summarize.md)

