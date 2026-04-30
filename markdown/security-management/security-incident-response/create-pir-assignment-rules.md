---
title: Create post incident review assignment rules
description: In addition to manually adding users to a Post Incident Review \(PIR\) assessment list for a security incident, you can define assignment rules for automatically adding users or group to the list.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage post incident activities, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create post incident review assignment rules

In addition to manually adding users to a Post Incident Review \(PIR\) assessment list for a security incident, you can define assignment rules for automatically adding users or group to the list.

## Before you begin

Role required: sn\_si.admin, sn\_si.manager, sn\_si.analyst

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Administration** &gt; **Post Incident Review - Assessments Setup**.

2.  Select the **Configure** button corresponding to the **User Assignment Rules** section.

3.  On the Post Incident Review Assignment Rules page, select **New**.

    ![Post incident review assignment rule](../image/pir-assignment-rule.png)

4.  Fill in the fields, as needed.

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

Option to activate the rule.

</td></tr><tr><td>

Order

</td><td>

Controls the display order of this assignment rule. Assignment rules with lower sequence numbers appear first. **Note:** Only the first matching assignment rule is executed, and only the users defined in that rule are added to the assessment list.

</td></tr><tr><td>

Condition

</td><td>

Option to configure the [condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) to define the conditions that must be met in the security incident for this rule to be executed. For more information, see the example below.

</td></tr><tr><td>

Assign to users

</td><td>

Field to add users to the review list. After the field is unlocked, options are available for adding or removing multiple users, roles, or entering user email addresses.

</td></tr><tr><td>

Assignment Group

</td><td>

Option to add an assignment group. All the active users of this group with the sn\_si.analyst role are added to the post incident review for a security incident.

</td></tr></tbody>
</table>5.  Select **Submit**.


## Malicious code activity

In the post incident review assignment rule shown here, when a security incident with the **Category** field set to **Malicious code activity** transitions to the **Review** state, the three users identified \(who happen to be experts in dealing with malicious code activity\) are added to the list of users who receive the post incident review questionnaire for this security incident.

![PIR assignment rule configuration](../image/malicious-code-activity.png "Malicious code activity")

