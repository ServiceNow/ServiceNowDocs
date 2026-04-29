---
title: Evaluate Nacha operating guidelines
description: Evaluate the Nacha \(National Automated Clearing House Association\) operating guidelines to ensure that the ACH dispute qualifies for potential reimbursement.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Processing an ACH dispute, Resolving ACH disputes, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Evaluate Nacha operating guidelines

Evaluate the Nacha \(National Automated Clearing House Association\) operating guidelines to ensure that the ACH dispute qualifies for potential reimbursement.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## About this task

Nacha governs the ACH network, which processes electronic payments like payroll, bill payments, and direct deposits in the United States of America. The Nacha Operating Rules and Guidelines establish compliance requirements for all disputed ACH transactions.

This task is dependent on the Dispute Rules Content Pack for Nacha plugin.

The Dispute Rules Content Pack for Nacha includes a Knowledge Base article that contains a table of reason codes and the corresponding eligibility rules.

To access the knowledge base article:

1.  Navigate to **All** &gt; **Knowledge Center**.
2.  Navigate to the knowledge base Dispute Compliance Documents.
3.  Open the knowledge base article Nacha Operating Guidelines for Return Codes.

Dispute agents may use the KB article to manually evaluate whether an ACH transaction is eligible for chargeback.

**Note:** When the ACH disputes resolution agentic workflow in Now Assist for FSO is enabled, the Nacha operating guidelines check AI Agent is available to assist you at this step. See [Evaluate Nacha operating guidelines with AI agent](../../fso-now-assist/task/nacha-guidelines-ai.md) for more information.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  In the **Processing** tab, select the transaction ID.

7.  In **Open Tasks**, select **Evaluate NACHA operation guidelines**.

8.  In **Nacha eligibility action**, indicate the final action.

    -   **Eligible**: This dispute is considered eligible under Nacha guidelines.
    -   **Ineligible**: This dispute is considered ineligible under Nacha guidelines.
9.  Enter a resolution reason.

10. Close the task.


**Parent Topic:**[Processing an ACH dispute](../concept/process-dispute-ach.md)

