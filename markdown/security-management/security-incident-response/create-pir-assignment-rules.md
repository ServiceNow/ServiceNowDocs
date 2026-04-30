---
title: Create PIR assignment rules
description: In addition to manually adding users post incident review assessment list for a security incident, you can define assignment rules for automatically adding users to the list.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Manage post incident activities, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create PIR assignment rules

In addition to manually adding users post incident review assessment list for a security incident, you can define assignment rules for automatically adding users to the list.

## Before you begin

Role required: sn\_si.admin, sn\_si.manager, sn\_si.analyst

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Administration** &gt; **Post Incident Review - Assessments Setup**.

2.  Drill down to the **User Assignment Rules** section.

3.  Click **Configure**.

4.  Click **New**.

    ![Post incident review assignment rule](../image/pir-assignment-rule.png)

5.  Fill in the fields, as needed.

<table id="table_l2p_dcs_ns"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of this assignment rule.

</td></tr><tr><td>

Active

</td><td>

Select this check box to make the rule active.

</td></tr><tr><td>

Order

</td><td>

Enter a numerical value to specify where in the list of assignment rules this rule should appear. Lower numbers appear at the top of the list.**Note:** Only the first matching assignment rule is executed, and only the users defined in that rule are added to the assessment list.

</td></tr><tr><td>

Condition

</td><td>

Use the [condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) to define the conditions that must be met in the security incident for this rule to be executed. For more information, see the example below.

</td></tr><tr><td>

Assign to users

</td><td>

Click the lock icon to add users to the review list. After the field is unlocked, options are available for adding or removing multiple users, roles, or entering user email addresses.

</td></tr></tbody>
</table>6.  Click **Submit**.


## Malicious code activity

In the post incident review assignment rule shown here, when a security incident with the **Category** field set to **Malicious code activity** transitions to the **Review** state, the three users identified \(who happen to be experts in dealing with malicious code activity\) are added to the list of users who will receive the post incident review questionnaire for this security incident.

![PIR assignment rule](../image/malicious-code-activity.png "Malicious code activity")

