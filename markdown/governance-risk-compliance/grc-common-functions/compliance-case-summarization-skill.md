---
title: GRC case summarization skill for compliance cases
description: The GRC case summarization skill uses a large language model \(LLM\) to generate a structured, AI-powered summary of a compliance case record. The summary is generated on demand from case data and can be saved to the record for future reference.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# GRC case summarization skill for compliance cases

The GRC case summarization skill uses a large language model \(LLM\) to generate a structured, AI-powered summary of a compliance case record. The summary is generated on demand from case data and can be saved to the record for future reference.

## Overview of the GRC case summarization skill

Compliance cases can span multiple action tasks, stakeholders, and regulatory requirements. The GRC case summarization skill generates a concise AI summary of key case details, so case analysts and managers can quickly understand the context and take informed action.

The skill collects data from predefined fields and related lists across the case record. This data is assembled into a prompt and sent to the configured LLM service provider, which then returns a structured summary.

To summarize compliance case records, the skill must be activated from the Now Assist Admin console. Once it's activated, case analysts with the appropriate user role can trigger the skill on a compliance case.

## User roles

The user roles required to activate, configure, and use the GRC case summarization skill are:

-   sn\_nowassist\_admin.nsa\_admin: Grants an admin access to activate or edit a Now Assist skill.
-   sn\_comp\_case.compliance\_case\_analyst: Grants access to compliance case records.
-   sn\_grc\_sharegenai.grc\_case\_ai\_user: Grants users access to use the GRC case summarization skill.

    **Note:** The sn\_grc\_sharegenai.grc\_case\_ai\_user role must be explicitly assigned and isn’t inherited through the case analyst role.


## LLM service providers

An administrator must set a default LLM provider before the skill can be used. The following providers are supported:

-   Azure OpenAI
-   AWS Claude
-   Now LLM Service
-   Now LLM Service LTS
-   Google Gemini

To set a default provider for the GRC case summarization skill, see [Manage model providers](https://www.servicenow.com/docs/access?context=edit-model-providers&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Components of a compliance case summary

The summary reflects case data at the time of generation. As the case progresses, you can regenerate the summary to capture the latest information. Once generated, you can review and edit the summary before saving it to the case record.

<table id="table_gxr_dwc_k3c"><thead><tr><th>

Section

</th><th>

What it captures

</th></tr></thead><tbody><tr><td>

Case Overview

</td><td>

Core case details, such as name, description, start date, priority, and assigned analyst, captured from the **Details** tab.

</td></tr><tr><td>

Events Timeline

</td><td>

Date of occurrence, date of discovery, investigation start and end dates, and remediation start and end dates, captured from the **Schedule** section on the **Details** tab.

</td></tr><tr><td>

Scope of Impact

</td><td>

**Impact breakdown**- Summary of the areas and regulatory frameworks that are impacted by a compliance case, captured from the **Impacted Areas**, **Related Areas**, and **Regulations** tabs.-   **Impacted areas**- Number of areas, such as the entities, controls, companies, and users, impacted by the reported compliance case.
-   **Related areas**- Number of areas, such as policies, citations, control objectives, control, and risk events, related to the compliance case.
-   **Regulations/Standards**- Number of regulations that are or can be impacted by the reported compliance case.

</td></tr><tr><td>

Causes &amp; Consequences

</td><td>

Causes and consequences of the compliance case, captured from the **Causes and Consequences** tab.-   **Cause \(Confirmed\)**- Confirmed cause of the incident.
-   **Contributing Cause \(Suspected\)**- Suspected cause of the incident.
-   **Consequences**- Resulting impact or penalties arising from the incident.

</td></tr><tr><td>

Actions &amp; Outcomes

</td><td>

Summary of actions taken during the investigation, captured from the **Action Tasks** tab.-   **Investigation**- Initial investigation tasks to examine the reported incident.
-   **Assessment**- Impact, loss, breach scope, and breach assessments to evaluate the incident.
-   **Additional Actions Taken**- Supplementary actions to support a resolution.

</td></tr><tr><td>

Evidence &amp; Worknotes

</td><td>

Work notes and comments recorded during the investigation, captured from the **Activity** section on the **Details** tab.

</td></tr><tr><td>

Lessons Learned

</td><td>

AI-powered analysis of the case timeline and overall investigation effort.-   **Velocity analysis**- Time to detect, investigate, and remediate.
-   **Investigation effort level**- Effort assessment ranked as low, medium, or high, based on case complexity, activity log, and timelines.

</td></tr></tbody>
</table>**Related topics**  


[Activate the GRC case summarization skill](../../now-assist-irm/task/activate-grc-case-summarization-skill.md)

[Summarize a compliance case using the GRC case summarization skill](../../now-assist-irm/task/summarize-compliance-case.md)

