---
title: Customer Engagement Sequences
description: Customer Engagement Sequences is a playbook that consists of a series of automated and manual activities that can be set up to engage with leads and customers at every stage of their relationship with your business​ through various channels.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Exploring Sales Customer Relationship Management, Sales Customer Relationship Management]
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

 \(For example, Sales admin, Sales Development Manager \(SDR\)\)

</td><td>

Creates multi-step sequences using Workflow Studio and defines triggers \(start conditions\), activities \(for example, call attempts\), and exit conditions.

</td></tr><tr><td>

Sequence task owner

 \(For example, Sales representative, customer success manager, telesales representative\)

</td><td>

Views sequence tasks that are assigned to them and executes targeted outreach strategies, often using a combination of emails, phone calls, and social media, to engage prospects and move them through the initial stages of the sales funnel using the predefined sequence steps.

</td></tr></tbody>
</table>## Customer Engagement Sequences workflow

The following illustration describes the tasks involved in configuring and using Customer Engagement Sequences.

![Infographic showing how sales development representatives create customer engagement sequences and how sales representatives use them for interacting with prospective customers. For details, refer to the following description.](../image/customer-engagement-sequences-workflow-landing.svg "Creating and using Customer Engagement Sequences")

1.  As a sequence admin, create a customer engagement sequence such as a lead-nurturing sequence from the CSM Configurable Workspace.
2.  Define the sequence parameters:
    -   Trigger conditions \(for example, when a new lead is created\)
    -   Sequence steps \(for example, call, follow-up, email\)
    -   Step frequency \(for example, wait three days between steps\)
    -   Exit conditions \(for example, lead conversion or disqualification\)
3.  Test and activate the sequence.
4.  Every record that meets the trigger condition is added to the sequence, and a sequence task associated with the record is created. For example, when a new lead record is created in the system, the sequence is run, and it generates a sequence task.
5.  As a sequence task owner, view the assigned sequence task and complete the series of predefined activities that are part of it. For example:
    -   Day 1: Call the prospect
    -   Day 4: Make a follow-up call and use a questionnaire to gather more information
6.  The sequence task moves to closed state when all sequence steps have been completed or the predefined exit condition is met.

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

-   Boost productivity by minimizing repetitive tasks so sales representatives can focus on high-value activities.
-   Reduce the chance of missing a follow-up, ensure consistency in outreach, and minimize manual effort by following predefined steps.
-   Accelerate onboarding by enabling new sales representatives to adopt proven outreach strategies from existing sequences.

</td><td>

[Predefined activities that align with business goals and outreach strategy](../task/execute-sequence-steps.md)

</td><td>

Sequence task owner

</td></tr></tbody>
</table>## What to explore next

The following topics provide more information about configuring and using Customer Engagement Sequences:

-   [Configuring Customer Engagement Sequences](configuring-customer-engagement-sequences.md)
-   [Using Customer Engagement Sequences](using-customer-engagement-sequences.md)
-   [Components installed with Customer Engagement Sequences](../reference/components-installed-customer-engagement-sequences.md)
-   [Exploring Workflow Studio](https://www.servicenow.com/docs/access?context=exploring-workflow-studio&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)

