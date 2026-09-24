---
title: Install Automation Discovery
description: You can install the Automation Discovery application \(sn\_auto\_discovery\) using the admin role. The application activates related plugins if they are not already activated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/install-automation-discovery.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Automation Discovery, Platform Analytics]
---

# Install Automation Discovery

You can install the Automation Discovery application \(sn\_auto\_discovery\) using the admin role. The application activates related plugins if they are not already activated.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Role required: admin

## About this task

**Important:** The deprecation of Automation Discovery was announced in the Zurich release. From the Brazil release, Automation Discovery is no longer deployed, enhanced, or supported. You can continue to use existing deployments but can't initiate new ones. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

The following items are installed with Automation Discovery: plugins, roles, and tables.

For more information, see [Components installed with Automation Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/installed-with-automation-discovery.md).

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

For more information see [Install Predictive Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/install-predictive-intelligence.md) or article [KB1641602](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1641602) on the Now Support Knowledge Base.

