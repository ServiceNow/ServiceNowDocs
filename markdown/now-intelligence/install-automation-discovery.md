---
title: Install Automation Discovery
description: You can install the Automation Discovery application \(sn\_auto\_discovery\) using the admin role. The application activates related plugins if they are not already activated.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automation Discovery, Platform Analytics]
---

# Install Automation Discovery

You can install the Automation Discovery application \(sn\_auto\_discovery\) using the admin role. The application activates related plugins if they are not already activated.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Role required: admin

## About this task

**Important:** Starting with the Zurich release, Automation Discovery is deprecated. It will be hidden and no longer installed on new instances but will continue to be supported in Australia. Support will be withdrawn in a future release. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

The following items are installed with Automation Discovery: plugins, roles, and tables.

For more information, see [Components installed with Automation Discovery](../reference/installed-with-automation-discovery.md#).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Automation Discovery application \(sn\_auto\_discovery\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can't find the application, you might have to request it from the [ServiceNow Store](https://store.servicenow.com/$appstore.do#!/store/home).

3.  In the Application installation dialog box, review the listed application dependencies.

    Automation Discovery is dependent on the Predictive Intelligence \(com.glide.platform\_ml\) and NLU Workbench \(com.glide.nlu\) plugins. These plugins are activated when Automation Discovery is installed, if they are not already activated.

4.  Select **Install**.


## What to do next

Confirm that the activation of Predictive Intelligence has successfully installed a sharedservice.worker user with the following roles.

-   platform\_ml\_create
-   platform\_ml\_read
-   platform\_ml\_write

For more information see [Install Predictive Intelligence](https://www.servicenow.com/docs/access?context=install-predictive-intelligence&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) or article [KB1641602](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1641602) on the Now Support Knowledge Base.

