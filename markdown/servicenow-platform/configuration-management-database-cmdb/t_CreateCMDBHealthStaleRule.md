---
title: Create a CMDB Health staleness rule
description: If the staleness metric is in effect, then staleness rules are used to determine the percentage of stale CIs in the CMDB. This sum is then aggregated into the correctness KPI.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, CMDB Health, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a CMDB Health staleness rule

If the staleness metric is in effect, then staleness rules are used to determine the percentage of stale CIs in the CMDB. This sum is then aggregated into the correctness KPI.

## Before you begin

Role required: sn\_cmdb\_editor and itil have read access, sn\_cmdb\_admin and itil\_admin \(on top\) have full access

## About this task

The Discovery setting of certain types of CIs as stale takes precedence over a CMDB Health staleness rule defined for the CI. For more information about Discovery marking CIs as stale, see Discovery for VMware vCenter.

Staleness rules are defined per class. If a rule isn't defined for a class, then the parent's rule is automatically derived by the child class and applies for the child class. If later a staleness rule is defined at the child class level, it overwrites the staleness rule that was derived from the parent class.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

2.  Select **Hierarchy** to show the CI Classes list and then select the class for which to create a staleness rule.

3.  In the class navigation bar, expand **Health**, select **Correctness**, and then select the Staleness Rule tab.

4.  Select a staleness rule to edit or select **New**, and then fill out the Staleness Rule form.

<table id="table_ncm_kfw_m5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Applies to

</td><td>

The class for which the rule applies.

</td></tr><tr><td>

Effective Duration

</td><td>

The time period that is used for the staleness test.If the CI was not updated \(based on Updated **sys\_updated\_on**\) within the specified time period — the CI is determined to be stale.

 If you enter a value with a prefix that is valid and a suffix that is not, such as `15 x` — the valid portion of the value is used \('15'\). If the entire value is invalid — the value is ignored and the previous valid value is used.

</td></tr></tbody>
</table>5.  Select **Submit** or **Update** to save the rule.


**Related topics**  


[CMDB Health Dashboard for Helsinki \| Overview](https://youtu.be/CvMRT3NExIo)

