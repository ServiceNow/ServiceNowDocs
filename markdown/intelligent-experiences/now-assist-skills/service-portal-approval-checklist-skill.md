---
title: Requester Approval Checklist
description: The Requester Approval Checklist skill in the ServiceNow AI Platform generates a structured checklist by mapping real-time request data against your organization’s knowledge articles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/now-assist-skills/service-portal-approval-checklist-skill.html
release: zurich
product: Now Assist Skills
classification: now-assist-skills
topic_type: concept
last_updated: "2026-01-14"
reading_time_minutes: 1
breadcrumb: [Skills in the Platform workflow, Skills, AI assets, Enable AI experiences]
---

# Requester Approval Checklist

The Requester Approval Checklist skill in the ServiceNow AI Platform® generates a structured checklist by mapping real-time request data against your organization’s knowledge articles.

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

This skill is available within AI Agents for Requester v3.1 and provides instant, data-backed decision support across in-product, agentic, and workflow experiences.

The skill uses information from the following sources to promote accuracy:

-   **Knowledge articles**

    Defines the evaluation criteria based on your company policy.

-   **System data**

    Fetches requester profiles and historical data from ServiceNow.

-   **Approval request**

    Analyze the details submitted in a live request.


## Requester Approval Checklist structure

The output is presented in a two-step format: Criteria \(what is required\) and Reason \(why it passed, failed, or has missing information\). Each item has one of the following statuses: Met, Not met, or Unknown.

**Note:** All referenced knowledge base articles are provided as links at the end of the checklist for easy verification.

## Key skill considerations

-   **Integration**

    The skill is built for workflows and agentic experiences, but doesn't support follow-up questions and answers.

-   **Decision support**

    The skill provides information only. It doesn't perform actions like Approve, Reject, or Comment.

-   **Flexibility and control**

    The Requester Approval Checklist respects the approval configuration to provide flexibility and control.


For more information, see [Platform Approval assistance AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/platform-approval-aia.md) and [Configure Service Portal Approval Configuration record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/configure-approval-assistance-ai-agent.md).

**Parent Topic:**[Generative AI skills in the Platform workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skills/now-assist-on-now-platform.md)

