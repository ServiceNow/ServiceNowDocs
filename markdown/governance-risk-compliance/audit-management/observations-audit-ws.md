---
title: Audit observations in Audit Workspace
description: Audit observations are the results of an audit. As an important part of the audit report, audit observations represent the results of reviews, analysis, interviews, and discussions.
locale: en-US
release: xanadu
product: Audit Management
classification: audit-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Audit Workspace for the Audit supervisor, Audit Workspace, Audit Management, Governance, Risk, and Compliance]
---

# Audit observations in Audit Workspace

Audit observations are the results of an audit. As an important part of the audit report, audit observations represent the results of reviews, analysis, interviews, and discussions.

## Overview of an audit observation

Audit observations are used to bring significant issues to the attention of audit supervisors. Observations are logged in the system. For example, if a bank's operations are being audited, then the audit observations are based on evidence about how the bank's operations perform against the audit criteria. During control testing, interviews, and walkthroughs, audit observations are recorded. An audit user can create an observation from an engagement if the engagement is not in the **Follow Up** or **Closed** states. An observation can also be created from all types of audit tasks.

After the auditor completes the audit, the auditor then presents the audit observations to the audit supervisors. By using the audit observations, the auditor can present a summary of problems, discoveries, and recommendations. The audit team reviews the observations to determine if the observation is a reportable issue. The audit team can also determine if the observation can be tracked as a recommendation, an observation, or a best practice.

In its life cycle, an audit observation moves through the following states:

1.  Draft
2.  Review
3.  Respond
4.  Finalize
5.  Closed

## Status workflow of an audit observation in workspace

1.  An audit user with the role sn\_audit.user creates an observation. See [Create an observation for an engagement](../task/create-observation-audit-ws.md).
    1.  To create an observation, navigate to **All** &gt; **Audit** &gt; **Audit Workspace**.
    2.  Click the lists icon \(![List icon.](../image/ListsIcon.jpg)\).
    3.  Click **All engagements** or **My engagements** in the Execution list.
    4.  Click the link to the engagement record in the **Name** column.
    5.  Click the **Observations** tab.
    6.  Click **New**.
    7.  On the Create New Observation form, fill in the fields.
2.  The observation creator assigns respondents and peer reviewers to the observation. The respondents are the entity owners and control owners. The peer reviewers are the auditors and audit leads of the engagement.
3.  The observation creator can request a peer review of the observation. In that case, the following happens:

    1.  The peer reviewer gets a notification to perform the peer review. The peer reviewer can view the task under **My pending tasks** &gt; **All** by clicking the tasks icon \(![Tasks icon](../image/TasksIcon.jpg)\) in the workspace.

        **Note:** The peer reviewer can also navigate to **Tasks** &gt; **My tasks** &gt; **Open** in the Home page of the workspace.

    2.  The peer reviewer completes the review.
    **Note:** When a peer review is requested, the state remains as **Draft** but the substate changes to **Peer review requested**.

4.  The observation creator can also request a review. The reviewer can be an audit supervisor or the audit lead.
    1.  The reviewer gets a notification to perform the review. The reviewer can view the task by navigating to **My pending tasks** &gt; **All** &gt; **Observations**.
    2.  The reviewer can either request a revision of the observation or request a response from the respondent. The reviewer can also provide feedback in the **Results** section by selecting the appropriate option.
5.  If the reviewer requested a response from the respondent, then the respondent responds to the observation by navigating to **Audit** &gt; **Observations** &gt; **My Pending Response**.
6.  The observation moves to the **Finalize** state.
7.  The observation is closed and an issue is created.

