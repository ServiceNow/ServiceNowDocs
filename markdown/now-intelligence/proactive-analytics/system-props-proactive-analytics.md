---
title: System properties for Proactive analytics
description: Several system properties that affect the generation of insights cards are available.
locale: en-US
release: xanadu
product: Proactive Analytics
classification: proactive-analytics
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Proactive analytics insights on dashboards, Dashboards in Platform Analytics, Platform Analytics experience, Platform Analytics]
---

# System properties for Proactive analytics

Several system properties that affect the generation of insights cards are available.

These properties either exist or can be created on the System Properties \[sys\_properties\] table. The admin role is necessary to set system properties.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_kmz_5xq_hzb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.snc.pa.insights.query\_limit

</td><td>

Limit the number of rows when querying the par\_computed\_insight table in the GET response to the Insights API.

 -   Type: Integer
-   Default value: 1000
-   Location: The System Properties \[sys\_properties\] table

</td></tr><tr><td>

com.snc.pa.insight.max\_days\_in\_past

</td><td>

By default, retrieve insights created within the number of days in the past that this property specifies.

-   Type: Integer
-   Default value: 14
-   Location: To change the value, create this property in the System Properties table.
-   More information: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)

</td></tr><tr><td>

com.snc.pa.correlation.enable\_insights

</td><td>

Enables the generation of key contributor insight cards.

-   Type: true/false \(Boolean\)
-   Default value: true
-   Location: To change the value, create this property in the System Properties table.
-   More information: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)

</td></tr><tr><td>

com.sys\_par\_insights\_enabled

</td><td>

Enables the Proactive Analytics feature.

-   Type: true/false \(Boolean\)
-   Default value: true
-   Location: To change the value, create this property in the System Properties table.
-   More information: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)

</td></tr><tr><td>

com.snc.pa.xmr.processes.limit

</td><td>

The maximum number of KPI Signals Configurations \(pa\_xmr\_processes\) that can be evaluated by the KPI Signals Insight Job. After this number of processes have been evaluated, the remaining processes are ignored. -   Type: Integer
-   Default: 1000
-   Maximum: 10,000

</td></tr></tbody>
</table>