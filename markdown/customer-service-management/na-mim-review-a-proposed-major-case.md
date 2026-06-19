---
title: Review a proposed major case
description: When the AI workflow proposes a new major case, review the suggestion and approve or reject it to determine whether a major issue lifecycle is initiated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/na-mim-review-a-proposed-major-case.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2026-06-03"
reading_time_minutes: 1
breadcrumb: [Now Assist for CSM Major Issue Management, Manage cases, Use, Customer Service Management]
---

# Review a proposed major case

When the AI workflow proposes a new major case, review the suggestion and approve or reject it to determine whether a major issue lifecycle is initiated.

## Before you begin

Role required: sn\_customerservice\_manager, sn\_majorissue\_mgt.major\_issue\_manager

The AI detection workflow must have identified a new major case candidate. The case `major_case_state` is set to **Proposed** and the Major Issue Management lifecycle has been triggered, placing the case in your queue.

## About this task

When a case is proposed, the workflow has already linked all similar cases to it using the `suggested_major_case` field and updated their worknotes and business impact. You can decide whether those associations are set to active under a major issue lifecycle or are dismissed.

## Procedure

1.  Open the proposed major case from your Major Case Manager queue.

2.  Review the worknotes added by the workflow to understand why the case was proposed.

    The worknotes summarize the similarity pattern the AI detected and list the related cases that triggered the proposal.

3.  Review the business impact statement updated by the workflow.

4.  Review the related cases linked by the `suggested_major_case` field to assess the scope of the potential major issue.

5.  Select **Approve** or **Reject**.

    |Action|Result|
    |------|------|
    |**__Approve__**|The proposed case is promoted to an active major case. Related cases remain linked under the major issue lifecycle.|
    |**__Reject__**|The proposal is dismissed. Related cases are not grouped under a major issue.|


