---
title: Post activation indexing and customization
description: After activating the report for a GRC issue AI agent, the system performs indexing to ensure optimal functionality. Users can also choose to customize the issue definition, enabling the AI agent to provide more tailored suggestions and align with organizational standards.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [issue submission AI agent, report a GRC issue, AI agent studio, indexing, customization, issue definition, post activation, generative AI, Now Assist]
breadcrumb: [Activate the Report a GRC issue AI agent, Configure, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Post activation indexing and customization

After activating the report for a GRC issue AI agent, the system performs indexing to ensure optimal functionality. Users can also choose to customize the issue definition, enabling the AI agent to provide more tailored suggestions and align with organizational standards.

## Indexing

Indexing begins automatically after activation. It prepares the system to deliver contextual recommendations during issue reporting. The system indexes the following objects:

-   Entities
-   Control objectives
-   Policies
-   Authority documents

Indexing can take a couple of minutes to several hours, depending on the volume of data. During this time, suggestions for related records don't appear, but other fields such as the problem statement and issue time remain functional. Once indexing is complete, the AI agent can suggest related records and improve clarity and context for reported issues.

## Customizing issue definition

The report a GRC issue AI agent uses a predefined issue definition provided by default in the system. If your organization’s issue definition differs, you can update it in the configuration settings.

The sn\_grc\_context\_definition table holds definitions for all GRC terms, including issues. Updating this table ensures that issue reporting aligns with organizational governance without any additional changes to the agent’s functionality.

**Related topics**  


[Activate the Report a GRC issue AI agent](activate-the-issue-submission-ai-agent.md)

[Report a GRC issue](report-a-grc-issue.md)

