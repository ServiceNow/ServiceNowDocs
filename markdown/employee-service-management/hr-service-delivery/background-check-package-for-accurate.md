---
title: Add background check packages for the Accurate service
description: Add one or more background check packages to your instance so they can be accessed when a request for a background check by Accurate is made. For example, you can add a package for a background check only and a package for both a background check and drug screening.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-06"
reading_time_minutes: 1
breadcrumb: [Integrating with the Accurate Background service, HR Integrations, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Add background check packages for the Accurate service

Add one or more background check packages to your instance so they can be accessed when a request for a background check by Accurate is made. For example, you can add a package for a background check only and a package for both a background check and drug screening.

## Before you begin

**Important:** Integrating with the Accurate Background service is being prepared for deprecation. It will be hidden and unavailable for activation from Zurich, but will continue to be supported till Brazil. If you have an active subscription, you can still activate the plugin by submitting a [plugin activation request](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/plugins/task/t_RequestAPlugin.html). For more details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

A background check package is a set of activities that are defined by the third-party system to be included in a background check. You can have a package for a background check only, a package for both a background check and drug screening, and so on. For each background check package, you must provide:

-   Package ID
-   Package name
-   Package description

Role required: sn\_hr\_integrations.admin

## Procedure

1.  Navigate to **HR Integrations** &gt; **Background Check Package**.

2.  Click **New** or open a record.

3.  Fill in the fields on the form.

    |Field|Description|
    |-----|-----------|
    |Package ID|ID of the background check package.|
    |Package name|Name of the background check package.|
    |Description|Description of the background check package.|
    |Source|Name of the third-party background check system.|

4.  Click **Submit** or **Update**.


## What to do next

.

**Parent Topic:**[Integrating with the Accurate Background service](../concept/integrate-with-accurate-service.md)

**Previous topic:**[Verify integration for the Accurate service](verify-base-integration-for-accurate.md)

**Next topic:**[Integrating with the Sterling Talent Solutions service](../concept/integrate-with-sterling-service.md)

**Related topics**  


[Provide source credentials for the Accurate service](hr-integrations-sources-accurate.md)

