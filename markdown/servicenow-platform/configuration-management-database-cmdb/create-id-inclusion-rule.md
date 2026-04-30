---
title: Create an identification inclusion rule
description: Narrow the scope of CIs that are included in the identification process by creating an identification inclusion rule.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Identification rules, Configure, CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create an identification inclusion rule

Narrow the scope of CIs that are included in the identification process by creating an identification inclusion rule.

## Before you begin

Role required: itil has read access, itil\_admin \(on top of itil\) has full access.

## About this task

During duplication detection of independent CIs, the identification and reconciliation engine \(IRE\) processes only the CIs that satisfy the identification inclusion rules. For example, you can set a filter to include only CIs whose state is operational. When no identification inclusion rules exist, all CIs are included in the identification process and in the CMDB Health duplicate metric calculations. In the base system, there are no predefined identification inclusion rules. Identification inclusion rules are defined at the class level.

Identification inclusion rules also indirectly impact what appears in CMDB health dashboards for duplicate CIs, in addition to any [health inclusion rules](create-health-inclusion-rule.md).

**Note:** Identification inclusion rules impact any script that calls IRE, therefore create them carefully. Identification inclusion rules can prevent the identification of certain types of CIs, affecting some features of Discovery and Service Mapping.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

2.  Select **Hierarchy** to display the CI Classes list.

3.  Select the class for which to create an identification inclusion rule.

4.  In the class navigation bar, expand **Class Info** and then select **Identification**.

5.  Create or edit a rule and specify its criteria.

    1.  In the Inclusion Rule \(Advanced\) section, select **Add** to create a rule or select **Edit** to edit an existing rule.

    2.  In the Create Inclusion Rules dialog box, specify a criteria in the **Active record condition** field.

        CIs must meet this criteria to be included in the identification process and in the duplicate CMDB Health metric.

6.  Select **Save**.


## What to do next

Navigate to **All** &gt; **Configuration** &gt; **Identification/Reconciliation** &gt; **Identification Inclusion Rules** &gt; **** to see the list of all identification inclusion rules.

**Parent Topic:**[Identification rules](../concept/c_IdentificationRules.md)

**Related topics**  


[Create a CI identification rule](t_CreateCIIdentificationRule.md)

[General guidelines for using CMDB Identification](../concept/best-practices-id-reconcile.md)

[Create health inclusion rule](create-health-inclusion-rule.md)

