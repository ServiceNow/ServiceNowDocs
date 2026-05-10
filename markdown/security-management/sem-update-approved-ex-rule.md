---
title: Update an approved exception rule
description: Cancel an approved rule to be able to update it. For example, before you can modify any dates or add a condition to an approved rule, you must cancel it so that the remediation task finding is deleted, and the findings move to the Open state.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Configuring an exception rule, Configure rules to manage findings, Implement, Unified Security Exposure Management, Security Operations]
---

# Update an approved exception rule

Cancel an approved rule to be able to update it. For example, before you can modify any dates or add a condition to an approved rule, you must cancel it so that the remediation task finding is deleted, and the findings move to the Open state.

## Before you begin

Role required: sn\_vul.vulnerability\_admin

## About this task

Group rules are reapplied to these findings. Submit the rule after making the changes so that it goes through the approval process once again.

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select **Administration** in the navigation pane.

3.  Select **Review** on the **Exception rules** tile.

4.  Open the exception rule that you want to cancel and click **Cancel**.

5.  In the Cancel Rule dialog box, click **Cancel rule**.

    The rule moves back to the Draft state and the associated VUL is deleted. The related Findings are reopened, and group rules are applied to the individual Findings.


**Parent Topic:**[Configuring an exception rule](../concept/sem-configure-exception-rule.md)

