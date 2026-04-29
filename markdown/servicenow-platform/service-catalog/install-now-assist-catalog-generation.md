---
title: Install Now Assist in Catalog Builder
description: Install the Now Assist for Creator application from the ServiceNow Store to get Now Assist in Catalog Builder.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [generative AI, Now Assist in Catalog Builder]
breadcrumb: [Now Assist in Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Install Now Assist in Catalog Builder

Install the Now Assist for Creator application from the ServiceNow® Store to get Now Assist in Catalog Builder.

## Before you begin

-   Review the [Now Assist for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility. Now Assist for Creator installs the Now Assist for catalog generation application \(com.snc.text2catalog\).
-   Role required: admin

## About this task

Now Assist in Catalog Builder is a capability within the Now Assist for Creator application and to start using this capability, you must to first install the application.

## Procedure

1.  From the Now Assist for Creator application page on the ServiceNow Store, select **Request App**.

2.  After approval has been granted, on your instance, navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

3.  Using the search bar, search for the Now Assist for Creator application \(sn\_now\_creator\).

4.  Select **Install**.

5.  Verify that Now Assist for Creator is installed:

    1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Features**.

    2.  In the workflow list, select **Creator**.

    3.  On the Service Catalog card, verify that the Catalog item generation skill is active.

        ![Catalog item generation skill](../image/catalog-item-gen-skill-page.png)

        **Note:** If the skill isn’t active, select **View details**. Then on the Service Catalog page, turn on the Catalog item generation skill.

        For more information about Now Assist Admin, see [Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).


## What to do next

Grant the catalog\_builder\_editor role to enable users to create catalog items using Now Assist.

**Parent Topic:**[Now Assist in Catalog Builder](../concept/now-assist-for-catalog-generation.md)

