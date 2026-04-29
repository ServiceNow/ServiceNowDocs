---
title: Map a skill to a dashboard
description: Map a Now Assist skill to a dashboard to view skill performance indicators and skill details.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Now Assist, map, skill, dashboard, performance indicator, sn\_na\_analytics\_admin, sn\_na\_analytics\_configuration, genAI, Generative AI]
breadcrumb: [Configuring Now Assist Analytics, Analyzing Now Assist performance, Exploring Now Assist Admin, Now Assist, Enable AI experiences]
---

# Map a skill to a dashboard

Map a Now Assist skill to a dashboard to view skill performance indicators and skill details.

## Before you begin

Be sure to map a dashboard with a skill in the same domain.

**Note:** You can only map a skill to a dashboard. Mapping a feature \(that consists of multiple skills\) is currently not supported.

If you're mapping a skill to a custom dashboard, be sure to share appropriate access to the dashboard. See [Share a Platform Analytics dashboard](https://www.servicenow.com/docs/access?context=share-db-in-ac&version=australia&pubname=australia-now-intelligence&ft:locale=en-US) for more information.

Roles required: sn\_na\_analytics.admin and sn\_nowassist\_admin.nsa\_admin

## Procedure

1.  Navigate to the **All** menu and enter `sn_na_analytics_configuration.list`.

    The Now Assist Analytics Configuration \[sn\_na\_analytics\_configuration\] table appears.![Now Assist Analytics Configuration table.](../image/naa-create-skill-dashboard-mapping.png)

2.  Create a new mapping by selecting **New**

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Dashboard|The Dashboard that you want to map to a skill. Use the lookup icon \(![Lookup icon.](../../now-assist-admin/image/na-list-lookup-icon.png)\) to search for and select the dashboard.|
    |Application|The application that contains the record.|
    |Document Table|Table that contains configured skills. Use the lookup icon \(![Lookup icon.](../../now-assist-admin/image/na-list-lookup-icon.png)\) to search for and select the Now Assist Skill Config \[sn\_nowassist\_skill\_config\] table.|
    |Document Id|The Skill that you want to map to the dashboard. Use the lookup icon \(![Lookup icon.](../../now-assist-admin/image/na-list-lookup-icon.png)\) to search for and select the skill that you want to map to the dashboard.|
    |Active|Check box used to enable or disable the mapping.|
    |Order|Order to set that determines the priority of the mapping in cases where multiple skills are mapped to the same dashboard.|

4.  Select **Submit**.


## What to do next

After you've completed the mapping, go to the Skill details page and select the skill from the drop-down list to verify that the mapped dashboard is displayed.

