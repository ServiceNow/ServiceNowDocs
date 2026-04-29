---
title: Configuring an exception rule
description: You can request an exception for findings that can't be remediated or deferred immediately. By automating the finding deferral process, you can defer the matching findings based on the rule when the system identifies them.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure rules to manage findings, Implement, Unified Security Exposure Management, Security Operations]
---

# Configuring an exception rule

You can request an exception for findings that can't be remediated or deferred immediately. By automating the finding deferral process, you can defer the matching findings based on the rule when the system identifies them.

-   **[Create an exception rule](../task/sem-create-exception-rule.md)**  
Create a rule to automatically request an exception for a specific condition for a group findings, such as a rule with a condition that is based on the vulnerability severity of these findings. With this rule, you can defer new and existing findings automatically if they match the approved rule condition.
-   **[Approve an exception rule request](../task/sem-approve-ex-rule-request.md)**  
Assess exception rule requests from users so that you can approve or reject these requests.
-   **[Activating an exception rule](sem-activate-ex-rule.md)**  
A rule is activated on its "Valid from" date. After activation, it automates the exception process for findings.
-   **[Reopen an exception rule](../task/sem-reopen-ex-rule.md)**  
Reopen an exception rule that has been rejected, but you want to resubmit. Reopening the rule moves it to the Draft state.
-   **[Update an approved exception rule](../task/sem-update-approved-ex-rule.md)**  
Cancel an approved rule to be able to update it. For example, before you can modify any dates or add a condition to an approved rule, you must cancel it so that the remediation task finding is deleted, and the findings move to the Open state.
-   **[Delete an exception rule](../task/sem-delete-ex-rule.md)**  
Delete an exception rule that is not required anymore. For example, you can delete a rule if you don't want to defer a finding during ingestion.

**Parent Topic:**[Configure rules to manage findings](../task/sem-configure-rules-manage-findings.md)

**Related topics**  


[Deferring findings automatically without manual intervention using exception rules](sem-exception-rules-overview.md)

