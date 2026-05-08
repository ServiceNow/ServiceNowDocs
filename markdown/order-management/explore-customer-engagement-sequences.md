---
title: Customer Engagement Sequences
description: Customer Engagement Sequences is a playbook that consists of a series of automated and manual activities that can be set up to engage with leads and customers at every stage of their relationship with your business​ through various channels.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Lead and opportunity management, Explore, Sales Customer Relationship Management]
---

# Customer Engagement Sequences

Customer Engagement Sequences is a playbook that consists of a series of automated and manual activities that can be set up to engage with leads and customers at every stage of their relationship with your business​ through various channels.

## Customer Engagement Sequences overview

Use ServiceNow® Customer Engagement Sequences to provide structured plans to sales representatives for prospects, which helps ensure consistent messaging and effective objection-handling. Standardizing repetitive tasks means representatives can focus on high-value actions.

## Customer Engagement Sequences users

<table id="table_yjd_pgj_wfc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sequence admin, sequence writer

 \(For example, Sales admin, Sales Development Manager \(SDM\)\)

</td><td>

Creates multi-step sequences using Workflow Studio and defines triggers \(start conditions\), activities \(for example, call attempts\), and exit conditions.

</td></tr><tr><td>

Sequence executor

 \(For example, Sales Development Representative \(SDR\), account executive, customer success manager, telesales representative\)

</td><td>

Views sequence tasks that are assigned to them and executes targeted outreach strategies, often using a combination of emails, phone calls, and social media, to engage prospects and move them through the initial stages of the sales funnel using the predefined sequence steps.

</td></tr><tr><td>

Business stakeholder

 \(For example, sales operations manager\)

</td><td>

Views sequences in Workflow Studio to identify and share high-performing workflows across territories, driving process optimization, consistency, and improved sales performance.

</td></tr></tbody>
</table>## Customer Engagement Sequences workflow

The following illustration describes the tasks involved in configuring and using Customer Engagement Sequences.

![Infographic showing how to create sequences and complete outreach using Customer Engagement Sequences. For details, refer to the list of tasks that follows.](../image/customer-engagement-sequences-workflow-landing.svg "Creating and using Customer Engagement Sequences")

1.  As a sequence writer, create a customer engagement sequence such as a lead-nurturing sequence from the CSM Configurable Workspace.
2.  Define the sequence parameters:
    -   Single or multi-trigger conditions \(for example, when a new lead is created\)
    -   Sequence steps \(for example, call, follow-up, email\)
    -   Delay between steps \(for example, wait three days between two call attempts\)
    -   Exit conditions \(for example, lead conversion or disqualification\)
3.  Test and activate the sequence.
4.  Every record that meets the trigger condition is added to the sequence, and a sequence task associated with the record is created. For example, when a new lead record is created in the system, the sequence is run, and it generates a sequence task.
5.  As a sequence executor, view the assigned sequence task and complete the series of predefined activities that are part of it. For example:
    -   Day 1: Call the prospect
    -   Day 4: Make a follow-up call and use a questionnaire to gather more information
6.  The sequence task moves to closed state when all sequence steps have been completed or the predefined exit condition is met.
7.  Business stakeholders with sequence reader role can view the sequences in Workflow Studio to suggest process improvements to the SDMs and share high-performing sequences with other sales teams situated in different territories.

## Customer Engagement Sequences benefits

<table id="table_scx_yvl_zfc"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

-   Configure sequences using Workflow Studio to reduce dependency on developers.
-   Provide a structured, multi-step plan to sales representatives for each prospect so they know exactly when to call, email, or send a social media message.
-   Personalize outreach by inserting a prospect’s name, company, and other details.
-   Ensure consistent messaging and effective objection handling by providing teams with clearly defined steps that dynamically adapt to customer responses.

</td><td>

[No-code interface to build customer engagement sequences](../task/create-customer-engagement-sequence.md)

</td><td>

Sequence admin, sequence writer

</td></tr><tr><td>

Reduce duplicating sequence workflows by specifying multiple record-based triggers on various entities that can initiate a sequence.

</td><td>

[Define trigger conditions](../task/define-trigger-conditions.md)

</td><td>

Sequence admin, sequence writer

</td></tr><tr><td>

Design telesales-oriented sequences using the schedule call activity, and enable outbound click-to-call capability by integrating with platforms such as Amazon Connect.

</td><td>

[Add a schedule call activity to a telesales workflow sequence](../task/add-schedule-call-activity.md)

</td><td>

Sequence admin, sequence writer

</td></tr><tr><td>

-   Boost productivity by minimizing repetitive tasks so sales representatives can focus on high-value activities.
-   Reduce the chance of missing a follow-up, ensure consistency in outreach, and minimize manual effort by following predefined steps.
-   Accelerate onboarding by enabling new sales representatives to adopt proven outreach strategies from existing sequences.

</td><td>

[Predefined activities that align with business goals and outreach strategy](../task/execute-sequence-steps.md)

</td><td>

Sequence executor

</td></tr><tr><td>

Use the click-to-call capability to connect with prospective customers from the sequence task without needing to leave your workspace.

</td><td>

[Fulfill a telesales sequence](../task/complete-telesales-sequences.md)

</td><td>

Sequence executor

</td></tr></tbody>
</table>## Related links

The following topics provide more information about configuring and using Customer Engagement Sequences:

-   [Configuring Customer Engagement Sequences](configuring-customer-engagement-sequences.md)
-   [Using Customer Engagement Sequences](using-customer-engagement-sequences.md)
-   [Components installed with Customer Engagement Sequences](../reference/components-installed-customer-engagement-sequences.md)
-   Exploring Workflow Studio

