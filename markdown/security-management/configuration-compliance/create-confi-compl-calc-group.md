---
title: Create a Configuration Compliance calculator group
description: Configuration Compliance calculator groups are used to group calculators based on how you want to use them.
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Create a Configuration Compliance calculator group

Configuration Compliance calculator groups are used to group calculators based on how you want to use them.

## Before you begin

Role required: sn\_vulc.admin

## About this task

The Configuration Compliance base system includes one calculator group: **Risk Score**. As you create other calculators, you can add them to this group or create other groups and calculators. Within each group, the first calculator that matches the test result runs.

There are two calculator groups that are included with the Configuration Compliance application:

-   Risk Calculators
-   Risk Score Rollup Calculators

Risk Calculators calculate the risk score and risk rating of a Test Result.

Risk Score Rollup Calculators roll up risk scores for all Test Results and Remediation Tasks with the same Configuration Test to provide an overall risk score.

You also create new calculators directly from these groups.

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Administration** &gt; **Calculator Groups**.

2.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Administration** and select **Risk Calculators** or **Risk Score Rollup Calculators**.

3.  Click **New**.

4.  Fill in the fields on the form, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Name|The name of the calculator.|
    |Description|A description of this calculator group.|
    |Active|Enable or disable the calculator group.|

5.  Right-click **Save** in the form header or click **Submit**.

    The new calculator group is displayed on in the group list with the other calculators. Click the name of new calculator group to open the record. See [Create, edit, and reapply risk calculators for Configuration Compliance](v11reapplycalc.md) for more information about setting conditions and displayed values and reapplying calculators.

    ![Newly added risk calculator called My risk calculator highlighted](../image/v11Newcalc.png)

    The **Security Calculators** related list is displayed.

    ![Risk score calculator group](../image/CalculatorGroup.png)

6.  Click **New** to add calculators along with their conditions to the group.

    Case sensitivity for the search text you enter in the condition builder is not supported on this record or form.


