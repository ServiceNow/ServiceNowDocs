---
title: Install AI Authoring for Catalog Builder
description: Install the ServiceNow Otto for Creator application from the ServiceNow Store to get AI Authoring for Catalog Builder.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/install-now-assist-catalog-generation.html
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [generative AI, AI Authoring in Catalog Builder]
breadcrumb: [AI Authoring for Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Install AI Authoring for Catalog Builder

Install the ServiceNow Otto for Creator application from the ServiceNow® Store to get AI Authoring for Catalog Builder.

## Before you begin

-   Review the [ServiceNow Otto for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility. ServiceNow Otto for Creator installs the AI Authoring for Catalog Builder application \(com.snc.text2catalog\).
-   Role required: admin

## About this task

AI Authoring for Catalog Builder is a capability within the ServiceNow Otto for Creator application and to start using this capability, you must to first install the application.

## Procedure

1.  From the ServiceNow Otto for Creator application page on the ServiceNow Store, select **Request App**.

2.  After approval has been granted, on your instance, navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

3.  Using the search bar, search for the ServiceNow Otto for Creator application \(sn\_now\_creator\).

4.  Select **Install**.

5.  Verify that ServiceNow Otto for Creator is installed:

    1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Features**.

    2.  In the workflow list, select **Creator**.

    3.  On the Service Catalog card, verify that the Catalog item generation skill is active.

        **Note:** If the skill isn’t active, select **View details**. Then on the Service Catalog page, turn on the Catalog item generation skill.

        For more information about AI Admin Hub, see [AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md).


## What to do next

Grant the catalog\_builder\_editor role to enable users to create catalog items using ServiceNow Otto.

**Parent Topic:**[AI Authoring for Catalog Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/now-assist-for-catalog-generation.md)

