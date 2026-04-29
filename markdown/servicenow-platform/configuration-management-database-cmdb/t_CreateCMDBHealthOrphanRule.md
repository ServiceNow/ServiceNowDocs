---
title: Create a CMDB Health orphan rule
description: Create an orphan rule to determine the percentage of orphan CIs in the CMDB. This sum is then aggregated into the correctness CMDB Health KPI. Orphan rules are defined per class, and only a single orphan rule can be defined per class.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, CMDB Health, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a CMDB Health orphan rule

Create an orphan rule to determine the percentage of orphan CIs in the CMDB. This sum is then aggregated into the correctness CMDB Health KPI. Orphan rules are defined per class, and only a single orphan rule can be defined per class.

## Before you begin

Role required: sn\_cmdb\_editor and itil have read access, sn\_cmdb\_admin and itil\_admin \(on top\) have full access

## About this task

Specify the conditions that CIs must meet to be considered an orphan CI. Specify attributes that a CI must have, relationships that a CI should not have, or both. In the relationship conditions, you can either specify that the CI has no relationships, or a set of specific relationships that the CI doesn't have.

**Note:** If there is a [health inclusion rule](create-health-inclusion-rule.md) for the orphan metric, then the conditions in the health inclusion rule and the conditions in the health orphan rule, shouldn't be identical.

A health orphan rule can for example, identify a CI of the cmdb\_ci\_computer class as an orphan CI if the CI is not set with an owner or an asset. Or, for example, you can create an orphan rule for a CI in the Disk \[cmdb\_ci\_disk\] class. If that CI doesn't have a Contains::Contained by or Contained by::Contains relationship with a Computer CI, then it is an orphan CI.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

2.  Select **Hierarchy** to show the CI Classes list and then select the class for which to create an orphan rule.

3.  In the class navigation bar, expand **Health**, select **Correctness**, and then select the Orphan Rule tab.

4.  Select a rule to edit, if one exists, or select **New**, and then fill out the form.

<table id="table_ncm_kfw_m5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Class

</td><td>

The class for which the orphan rule applies.

</td></tr><tr><td>

Attributes

</td><td>

Attribute conditions that a CI must satisfy to be considered an orphan CI. For example, the filter conditions in which both the **Assigned to** and the **Owned by** fields are empty, will identify the matching CIs as orphans.

</td></tr><tr><td>

Condition

</td><td>

And/Or operation between the **Attributes** conditions and the **Relationship** conditions.

</td></tr><tr><td>

Relationship

</td><td>

The relationship conditions that a CI must fail,based on records in the CI Relationship \[cmdb\_rel\_ci\] table, in order to be considered an orphan CI.

 To specify that a CI must have no relationships, choose **Any Relation** and **Any Class** respectively.

</td></tr></tbody>
</table>5.  Select **Submit** or **Update** to save the rule.


**Related topics**  


[CMDB Health Dashboard for Helsinki \| Overview](https://youtu.be/CvMRT3NExIo)

