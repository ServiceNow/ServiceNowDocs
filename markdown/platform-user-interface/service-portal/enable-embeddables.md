---
title: Enable embeddables
description: Before you can use embeddables in Service Portal, you must install the required plugins and enable the feature on your portal record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-user-interface/service-portal/enable-embeddables.html
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-09-23"
reading_time_minutes: 1
keywords: [embeddables, service portal, enable, setup, prerequisites]
breadcrumb: [Embeddables in Service Portal, Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Enable embeddables

Before you can use embeddables in Service Portal, you must install the required plugins and enable the feature on your portal record.

## Before you begin

Role required: admin

Install the following plugins on your ServiceNow® instance:

-   `com.glide.ux.embeddables`
-   `app-embeddables-core`

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Portals**.

2.  Select a portal record.

3.  Select **Enable Embeddables**.

    **Note:** If **Enable Embeddables** is not available, verify that the `com.glide.ux.embeddables` plugin is installed on your instance.

4.  select components you want Service Portal to preload during the initial page load.

    1.  In the **Embeddable Macroponents** section, select **Select target record**.

    2.  Choose one or more macroponents from the list.

5.  Select **Save**.


**Parent Topic:**[Embeddables in Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-user-interface/service-portal/embeddables-service-portal.md)

