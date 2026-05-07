---
title: Create an exception rule
description: Create a rule to automatically request an exception for a specific condition for a group findings, such as a rule with a condition that is based on the vulnerability severity of these findings. With this rule, you can defer new and existing findings automatically if they match the approved rule condition.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 2
breadcrumb: [Configuring an exception rule, Configure rules to manage findings, Implement, Unified Security Exposure Management, Security Operations]
---

# Create an exception rule

Create a rule to automatically request an exception for a specific condition for a group findings, such as a rule with a condition that is based on the vulnerability severity of these findings. With this rule, you can defer new and existing findings automatically if they match the approved rule condition.

## Before you begin

Role required: See [Access control lists \(ACLs\) for administration rules](../concept/sem-acls-for-admin-rules.md)

## About this task

The rule is applied from the "Valid from" until the "Valid to" date. The remediation task \(VUL\) is created when the rule is approved. The grouping method for this VUL is known as exception rules. The VUL is created in the Deferred state. You can't close, reopen, or delete this VUL. New and reopened VIs are deferred and added to this VUL from the "Valid from" date until the group expires on the "Valid to" date.

**Note:**

Email notifications are sent at every stage of the exception rule work flow. These emails provide the status and other details of a request. For example, when an exception rule is requested, the requester receives an email that confirms that the request is submitted.

**Note:** If the rule is rejected, you can reopen it in the Draft state, update it, and then resubmit it for approval.

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select **Administration** in the navigation pane.

3.  Select **Review** on the **Exception rules** tile.

4.  On the Exception Rule new record page, click **New** to create a rule.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the exception rule.|
    |Valid from|Date from which this rule is active to defer the Findings.|
    |Valid to|Date from which the remediation task stops accepting new Findings.|
    |Reason|Reason to create this exception rule.|
    |Assignment group|Group that the remediation task that was created for tracking the deferred Findings is assigned to.|
    |Additional information|Additional information that the requester wants to provide to the approver. This information is populated in the description field of the remediation task.|
    |Condition|Filter condition for the Findings that can be defined while processing the Findings.|
    |Execute on existing data|Option that enables you to run this rule on existing data the first time that this rule is run.|
    |Workflow stage|Current approval status of the exception rule.|
    |State|State of the exception rule.|
    |Execution order|Unique order for each exception rule.|
    |Deferred until|Date until when the VULs and Findings are deferred. On this date, the created VUL is closed, all the Findings move out of the group, and group rules are reapplied.|

6.  Add the assignment group when you are creating the rule.

7.  Submit the form for approval.

    The status of the request changes to In review. Until you submit the exception rule, it remains in the Draft state.


**Parent Topic:**[Configuring an exception rule](../concept/sem-configure-exception-rule.md)

