---
title: Map a skill to a dashboard
description: Map a Now Assist skill to a dashboard to view skill performance indicators and skill details.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-09-25"
reading_time_minutes: 1
keywords: [Now Assist, map, skill, dashboard, performance indicator, sn\_na\_analytics\_admin, sn\_na\_analytics\_configuration, genAI, Generative AI]
breadcrumb: [Configuring Now Assist Analytics, Analyzing Now Assist performance, Now Assist, Enable AI experiences]
---

# Map a skill to a dashboard

Map a Now Assist skill to a dashboard to view skill performance indicators and skill details.

## Before you begin

Role required: Now Assist Analytics Admin \[sn\_na\_analytics\_Admin\] and Now Assist Admin \[sn\_nowassist\_admin.nsa\_admin\]

Be sure to map a dashboard with a skill in the same domain.

**Note:** You can only map a skill to a dashboard. Mapping a feature \(that consists of multiple skills\) is currently not supported.

If you are mapping a skill to a custom dashboard, be sure to share appropriate access to the dashboard. See [Share a Platform Analytics dashboard](https://www.servicenow.com/docs/access?context=share-db-in-ac&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US) for more information.

## Procedure

1.  Navigate to **All** menu and enter `sn_na_analytics_configuration.list`.

    The Now Assist Analytics Configuration \[sn\_na\_analytics\_configuration\] table appears.

2.  Select **New** to create a new mapping.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Dashboard**|The dashboard you want to map to a skill. Use the search icon to search for and select the dashboard.|
    |**Application**|The application that contains the record|
    |**Document Table**|The table that contains configured skills. Use the lookup icon to search for and select Now Assist Skill Config \[sn\_nowassist\_skill\_config\] table.|
    |**Document Id**|The skill that you want to map to the dashboard. Use the lookup icon to search for and select the skill that you want to map to the dashboard.|
    |**Active**|Check box used to enable or disable the mapping.|
    |**Order**|Set the order to determine priority of the mapping in cases where multiple skills are mapped to the same dashboard.|

4.  Select **Submit**.


## What to do next

After you've completed the mapping, go to Skill details page and select the skill from the drop down to verify that the mapped dashboard is displayed.

