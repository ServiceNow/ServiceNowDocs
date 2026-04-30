---
title: Automation Center properties
description: You can access system properties for Automation Center by navigating to All Automation Center Administration Automation Properties .
locale: en-US
release: yokohama
product: Automation Center
classification: automation-center
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Automation Center reference, Automation Center, Data and Automation]
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

Defines the number of days to purge automation execution data and automation insights information.-   Type: **integer**
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
</table>**Parent Topic:**[Automation Center reference](../concept/automation-center-reference.md)

