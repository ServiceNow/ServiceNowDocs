---
title: Configure the CI form contextual help skill
description: Configure the CI form contextual help skill.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-skill-form-sense-config.html
release: zurich
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-04"
reading_time_minutes: 1
breadcrumb: [Configure, Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure the CI form contextual help skill

Configure the CI form contextual help skill.

## Before you begin

Role required: admin

## About this task

To enable Now Assist to provide a detailed description, you must activate the External Content Connectors plugin, install the ‘ServiceNow Product Documentation’ connector, and then crawl the product documentation.

## Procedure

1.  Navigate to **All** &gt; **Application Manger** and then search for `external content connectors` on the **Available for you** or **Updates** tab.

2.  Install the ServiceNow product documentation external content connector as described in .

3.  Configure the crawl settings as described in .

    On the **Settings** tab, select **Extend Now Platform Capabilities** and then select **Save**.

    **Note:** You can select additional settings, but, to enable the skill, you must at least select **Extend Now Platform Capabilities**.

4.  On the **Crawl schedules** tab, select **Crawl content** and then follow the instructions in  to configure the crawl process.


**Parent Topic:**[Configuring Now Assist for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-configuring.md)

