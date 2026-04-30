---
title: Property settings for Now Assist for CMDB
description: List of system properties for the agents used by Now Assist for CMDB agents.
locale: en-US
release: yokohama
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: reference
last_updated: "2025-11-08"
reading_time_minutes: 1
breadcrumb: [Reference, Now Assist for Configuration Management Database \(CMDB\), CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Property settings for Now Assist for CMDB

List of system properties for the agents used by Now Assist for CMDB agents.

## Property settings

**Note:** All properties are in the System Property \[sys\_properties\] table. To open the sys\_properties table, enter `sys_properties.list` in the navigation filter.

<table id="table_m2p_xvj_q2c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_cmdb\_gen\_ai.principal\_class\_suggestion\_period

</td><td>

The CMDB data governance manager agentic workflow collects and aggregates Change Management, Incident Management, and Problem Management data for the specified CI class. If the workflow collects too much data, the process might fail. This property limits the duration in days \(integer starting at zero\) for the query.

 For instances with little data, set the property to a high value like 36000 \(10 years\). For instances with a large store of data, experiment to determine a practical value.

 -   Type: integer
-   Default value: `90` \(Query all tasks that were updated in the last 90 days.\)

</td></tr><tr><td>

sn\_cmdb\_gen\_ai.suggested\_principal\_classes\_limit

</td><td>

Specifies the maximum number of principal classes that are suggested to the user.

 Type: integer

</td></tr><tr><td>

sn\_cmdb\_gen\_ai.health\_ownership\_evaluation\_period

</td><td>

If the CMDB data governance manager agentic workflow collects too much health data, the process might fail. This property limits the duration in days \(integer starting at zero\) for the query.

 -   Type: integer
-   Default value: `90` \(Query all tasks that were updated in the last 90 days.\)

</td></tr><tr><td>

sn\_cmdb\_gen\_ai.ownership\_evaluation\_health\_score\_thresholds

</td><td>

The CMDB data governance agentic workflow determines the percentage of CIs in the specified class that have values for the **Managed by group** attribute. The process returns health scores of `Poor`, `Average`, or `Healthy`.

 The default setting of `40,60,80` returns a score of `Poor` for less than 40%, `Average` for 60%-79%, and `Healthy` for 80% and above.

 Default: 40,60,80

</td></tr><tr><td>

sn\_nowassist\_sgc.ai\_search\_kb\_score\_threshold

</td><td>

Enter the relevancy score threshold for AI Search, used when retrieving knowledge articles with Now Assist for SGC.-   Type: integer
-   Default value: `5`

</td></tr><tr><td>

sn\_nowassist\_sgc.kb\_filtering\_strategy

</td><td>

Set the knowledge article filtering strategy for retrieving articles with Now Assist for SGC. -   Type: choice list
-   Default value: `strict`

Choices:

-   **strict**

Retrieves knowledge articles from the selected connector category only.

-   **non-strict**

Retrieves knowledge articles from other connector categories, in addition to the selected connector category.


</td></tr></tbody>
</table>**Parent Topic:**[Now Assist for CMDB reference](../../configuration-management/concept/now-assist-cmdb-reference.md)

