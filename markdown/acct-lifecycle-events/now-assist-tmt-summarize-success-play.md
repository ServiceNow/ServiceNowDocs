---
title: Summarize a customer play using ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)
description: Generate a summary from a customer play record and all associated customer play tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/now-assist-tmt-summarize-success-play.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Create a customer play, Manage playbooks, Customer success, Use, Customer Success Management]
---

# Summarize a customer play using ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)

Generate a summary from a customer play record and all associated customer play tasks.

## Before you begin

Role required: `sn_acct_lc.customer_success_agent`

## About this task

The customer play summary skill provides a summary of the customer play record and associated customer play tasks. The skill is available in CRM Workspace and in Core UI:

-   In CRM Workspace, use the Customer play summary by ServiceNow Otto component, which appears above the Activities card.
-   In Core UI, select **Summarize** on the customer play record.

**Note:** The skill requires a minimum 50 words in the record to generate a summary. If the skill isn't active, summaries are generated using the out-of-box case summarization skill instead.

## Procedure

1.  Navigate to **Workspaces** &gt; **CRM Workspace** &gt; **Lists** &gt; **All Customer plays**.

2.  Open a customer play and select **Summarize**.

    Based on the inputs from Engagement, Account, and Short Description, the summary includes:

    -   **Overview:** the primary goal, engagement, account, product, progress, due date, squad, and customer contact details.
    -   **Progress updates:** current status, meetings associated with the customer play, and total/open/closed task counts.
    -   **Next steps:** all open customer play tasks, required agent actions, scheduled meetings, and tasks due in the next 7 days.
3.  After you're finished, manage the results: view more/less detail, provide helpful/not-helpful feedback, copy the summary, or view summary info using the icons on the summary card.


**Parent Topic:**[Create a customer play](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-create-success-case-playbook.md)

