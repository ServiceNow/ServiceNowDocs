---
title: Create or edit Configuration Compliance remediation task rules
description: You can create rules to automatically group test results based on filter conditions. These rules automatically group test results as they are imported. Use the filter to limit the test results grouped by this rule, such as selecting all test results with exploits.
locale: en-US
release: australia
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Create or edit Configuration Compliance remediation task rules

You can create rules to automatically group test results based on filter conditions. These rules automatically group test results as they are imported. Use the filter to limit the test results grouped by this rule, such as selecting all test results with exploits.

## Before you begin

Role required: sn\_vulc.admin

## About this task

The base system ships with one remediation task rule, **Assignment group, Test**, which groups test results by assignment group \(pre-populated from **Assignment Rules**\) and the test result **Test** field. This rule can be modified using filter conditions and group keys. Group keys are columns in the test results table. Select up to six keys to indicate what values should be used to group the test results.

Starting with version 14.7 of Configuration Compliance, the **Assignment group, Test** remediation task rule is deactivated for new implementations.

**Note:** New or updated rules are automatically evaluated on the next import or manually using the **Reapply** button on the Remediation Task Rule form.

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Administration** &gt; **Remediation Task Rules**.

2.  Open the **Assignment group, Test** rule or click **New**.

    ![New Remediation Task rule example](../image/TRGRExample.png)

3.  If **New**, fill in the fields on the form, as appropriate.

<table id="table_vks_thr_ns"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the remediation task rule.

</td></tr><tr><td>

Active

</td><td>

Indicates whether the remediation task rule is active.

</td></tr><tr><td>

Description

</td><td>

Text description of this remediation task rule.

</td></tr><tr><td>

Case sensitive

</td><td>

Determines whether the rule matching is case sensitive or not.**Note:** The default value is case insensitive.

</td></tr><tr><td>

Conditions

</td><td>

Conditions that must be met.By default, \(**Case sensitive** check box disabled\), the search text you enter in the condition builder on remediation task rules records and forms is not case-sensitive. You have the option to enable case-sensitive searches on group records and forms.

</td></tr><tr><td class="sub-head" colspan="2">

**Group By**

</td></tr><tr><td>

Group test results from

</td><td>

Automate the creation of groups based on this rule. Choose one of the options available.-   Test Result \| Using field
-   Test Result-&gt;Configuration Item \| Table \| Using field

If an extended **Table** field is selected, test results that don't use the corresponding extended table are grouped in a separate remediation task.

</td></tr><tr><td class="sub-head" colspan="2">

**Assignment**

</td></tr><tr><td>

Assign test result groups by

</td><td>

Automate the assignment of groups created based on this rule. Choose one of the options available.

-   Group key

When selected, a Key value field appears, available fields are listed in a drop-down menu.

-   User group

When selected, a User group lookup field appears.

</td></tr></tbody>
</table>4.  Click **Submit**.

    **Note:** **The Clear Group By Keys** related link removes the group keys from the Group By tab on the form.


