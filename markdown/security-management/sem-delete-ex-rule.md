---
title: Delete an exception rule
description: Delete an exception rule that is not required anymore. For example, you can delete a rule if you don't want to defer a finding during ingestion.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Configuring an exception rule, Configure rules to manage findings, Implement, Unified Security Exposure Management, Security Operations]
---

# Delete an exception rule

Delete an exception rule that is not required anymore. For example, you can delete a rule if you don't want to defer a finding during ingestion.

## Before you begin

Role required: See [Access control lists \(ACLs\) for administration rules](../concept/sem-acls-for-admin-rules.md)

## About this task

Deleting a rule cancels the associated remediation task \(VUL\). The related findings are reopened, and group rules are applied to the individual findings.

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select **Administration** in the navigation pane.

3.  Select **Review** on the **Exception rules** tile.

4.  Open the exception rule that you want to delete and click **Delete**.

5.  In the Delete Rule dialog box, click **Delete rule** to delete the selected rule.

    The associated remediation task is also deleted. The related findings are reopened, and group rules are applied to the individual findings.


**Parent Topic:**[Configuring an exception rule](../concept/sem-configure-exception-rule.md)

