---
title: Automation Center properties
description: You can access system properties for Automation Center by navigating to All Automation Center Administration Automation Properties .
locale: en-US
release: australia
product: Automation Center
classification: automation-center
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Automation Center, Workflow Data Fabric]
---

# Automation Center properties

You can access system properties for Automation Center by navigating to **All** &gt; **Automation Center** &gt; **Administration** &gt; **Automation Properties**.

<table id="table_fd2_bdj_lsb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_ac.workspace.date.default\_num\_of\_days

</td><td>

Defines the default number of days that data is shown in the Automation Center workspace.-   Type: **integer**
-   Default value: **7**

</td></tr><tr><td>

sn\_ac.purge\_automation\_data\_in\_days

</td><td>

Defines the number of days the automation execution data, import error logs, action logs data, and automation insights information is retained.-   Type: **integer**
-   Default value: **14**

</td></tr><tr><td>

sn\_ac.reporting\_currency

</td><td>

Defines the currency that is used in the Automation Center dashboards and reports.-   Type: **integer**
-   Default value: **USD**

</td></tr><tr><td>

sn\_ac.savings\_averaging\_window

</td><td>

Calculates the moving average for cost and time saved per run.-   Type: **integer**
-   Default value: **4**

</td></tr></tbody>
</table><table id="table_m3d_cyx_qvb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_ac.use.spotlight.score.for.requests

</td><td>

When turned on \(by setting the value to **True**\), Spotlight feature is enabled in the Automation Center workspace.-   Type: **True/False**
-   Default value: **True**

</td></tr><tr><td>

sn\_ac.use.spotlight.group.for.requests

</td><td>

Stores the spotlight group sys\_id to let the system know which spotlight group to use. -   Type: **string**
-   Default value: **e037711dc3a11110995486d91840dd03**

</td></tr></tbody>
</table><table id="table_ayt_v3p_dwb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_ac.use\_recommended\_actions

</td><td>

When turned on \(by setting the value to **True**\), Recommended Actions application is enabled in the Automation Center workspace.-   Type: **True/False**
-   Default value: **False**

</td></tr></tbody>
</table><table id="table_ajs_lyf_q3c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_ac.max\_number\_of\_actions

</td><td>

Sets the maximum number of actions to show in all actions section in action center.-   Type: **True/False**
-   Default value: **False**

</td></tr><tr><td>

sn\_ac.max\_number\_of\_recent\_executions

</td><td>

Controls the number of action log cards we want to show in the recent section in action center.-   Type: **Integer**
-   Default value: **12**

</td></tr><tr><td>

sn\_ac.new\_action\_threshold

</td><td>

Controls the number of days the "New action" tag should appear for the newly created actions.-   Type: **Integer**
-   Default value: **12**

</td></tr></tbody>
</table><table id="table_vfq_czf_q3c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_ac.rpamigration.base.url

</td><td>

Desc-   Type: ****
-   Default value: **https://rpamigration-prod-default/**

</td></tr><tr><td>

sn\_ac.polling\_timeout\_migration\_report

</td><td>

Defines the maximum duration \(in milliseconds/seconds\) to wait while polling for the migration report status before the request times out. This ensures that long-running or stalled migration status checks do not block the process indefinitely.-   Type: **Integer**
-   Default value: **300**

</td></tr></tbody>
</table>**Parent Topic:**[Automation Center reference](../concept/automation-center-reference.md)

