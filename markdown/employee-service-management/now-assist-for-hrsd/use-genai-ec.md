---
title: Configure Gen AI Virtual Agent for HRSD
description: Enable your requesters to have a streamlined, conversational experience that is based on generative AI as they submit a catalog item request in Virtual Agent. By offering this generative AI experience, your organization can increase self-service and reduce operating costs.
locale: en-US
release: xanadu
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure Now Assist for HR Service Delivery \(HRSD\), Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Configure Gen AI Virtual Agent for HRSD

Enable your requesters to have a streamlined, conversational experience that is based on generative AI as they submit a catalog item request in Virtual Agent. By offering this generative AI experience, your organization can increase self-service and reduce operating costs.

## Before you begin

Role required: admin

## About this task

The generative AI capabilities can provide a human-like, efficient catalog request experience over the Virtual Agent conversational interface. By using the generative AI capabilities with Virtual Agent, your organization can reduce the turnaround time for the request submission.

When the generative AI experience is configured for catalog item request submissions, the following experience is available for a requester:

-   Contextual question prompts that enable a more human-like conversation based on answers to previous questions.
-   Slot filling that recognizes answers to one or more questions on the requester's input. For example, inquiring about HR benefits or requesting leave of absence.
-   Ability to answer catalog item questions.
-   Ability to exit the request submission process at any point.
-   Although the following catalog item question types are supported in the conversation mode, natural language responses aren't supported:
    -   Reference
    -   Lookup select box
    -   Lookup multiple choice
    -   Requested For
    -   Attachment
    -   Multiple choice question with more than 10 choices

## Procedure

1.  Turn on the required Virtual Agent Skills: **Multi-Assist Multi-turn Catalog Ordering** and/or **Now-Assist Q&amp;A Genius Results**.

2.  Set up Now Assist in Virtual Agent.

    For complete details on how to turn on the skills and set up Gen AI Virtual Agent, see [Configuring Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

    **Note:**

    -   Configure the required conditions for the Virtual Agent Skills.
    -   HR Service Delivery Virtual Agent will be replaced with the Gen AI Virtual Agent.

**Parent Topic:**[Configure Now Assist for HR Service Delivery \(HRSD\)](configure-now-assist-hr.md)

**Related topics**  


[Skill inputs and triggers for Now Assist for HR Service Delivery \(HRSD\)](../concept/now-assist-hrsd-skill-inputs.md)

[RCA approvals for Now Assist for HR Service Delivery \(HRSD\)](run-rca-now-assist-hrsd.md)

[Restrict Now Assist capabilities for employee relations cases](restrict-now-assist-skills-er-cases.md)

[Configure the Now Assist for HRSD Virtual Agent topics](config-va-topics.md)

[Configure HCM AI agents from the HR Service Delivery AI Agent Collection](configure-hcm-agents.md)

[Configure sensitivity detection in Now Assist for HR Service Delivery \(HRSD\)](config-na-sd-filters.md)

