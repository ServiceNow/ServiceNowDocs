---
title: GRC case summarization skill for privacy cases
description: The GRC case summarization skill uses a large language model \(LLM\) to generate a structured summary of a privacy case record. The summary is generated on demand from case data and can be saved to the record for future reference.
locale: en-US
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Now Assist for Privacy Management, Privacy Management, Governance, Risk, and Compliance]
---

# GRC case summarization skill for privacy cases

The GRC case summarization skill uses a large language model \(LLM\) to generate a structured summary of a privacy case record. The summary is generated on demand from case data and can be saved to the record for future reference.

## Overview of the GRC case summarization skill

Privacy cases can involve multiple coordinators, complex activity logs, and breach assessments. The GRC case summarization skill generates a concise AI summary of key case details, so assignees and approvers can quickly understand the context and support efficient decision-making.

The GRC case summarization skill collects data from predefined fields and related lists across the case record. This data is assembled into a prompt and sent to the configured LLM service provider, which then returns a structured summary.

To summarize privacy case records, the skill must be activated from the Now Assist Admin console. Once it's activated, case analysts with the appropriate user role can trigger the skill on a privacy case.

## User roles

Important user roles to activate and use this skill are:

-   sn\_nowassist\_admin.nsa\_admin: Grants an admin access to activate or edit a Now Assist skill.
-   sn\_privacy\_case.privacy\_case\_analyst: Grants access to privacy case records.
-   sn\_prm\_gen\_ai.user: Grants access to the Now Assist for Privacy Management skills.

    **Note:** Users with the sn\_prm\_gen\_ai.user role automatically have the sn\_grc\_sharegenai.grc\_case\_ai\_user role, which is the minimum role required to use the GRC case summarization skill.


All members of the **Assignment group** on a case record can view any summary that has been saved to that record.

## LLM service providers

An administrator must set a default LLM provider before the skill can be used. The following providers are supported:

-   Azure OpenAI
-   AWS Claude
-   Now LLM Service
-   Now LLM Service LTS
-   Google Gemini

To set a default provider for the GRC case summarization skill, see [Manage model providers](https://www.servicenow.com/docs/access?context=edit-model-providers&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Components of a privacy case summary

The summary reflects case data at the time of generation. As the case progresses, you can regenerate the summary to capture the latest information. Once generated, you can review and edit the summary before saving it to the privacy case record. The saved summary appears in the **Overview** tab and in the **Activity** stream of the **Details** tab.

<table id="privacy_summary_structure"><thead><tr><th>

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

**Blast Radius Breakdown**- Summary of the areas and regulatory frameworks impacted by the privacy case, captured from the **Impacted Areas**, **Related Areas**, and **Regulations** tabs.-   **Impacted areas**- Number of areas, such as control, entity, location, company, and users, impacted by the reported privacy case.
-   **Related areas**- Number of areas, such as policies, citations, control objectives, and risk events, related to the privacy case.
-   **Regulations/Standards**- Number of regulations that are or can be impacted by the reported privacy case.

</td></tr><tr><td>

Data Impacted

</td><td>

Types of personal data exposed or compromised during the incident, captured from the **\[PI\] Information Objects** tab.

</td></tr><tr><td>

Evidence &amp; Worknotes

</td><td>

Work notes and comments recorded during the investigation, captured from the **Activity** section on the **Details** tab.

</td></tr><tr><td>

Causes &amp; Consequences

</td><td>

Causes and consequences of the privacy case, captured from the **Causes and Consequences** tab.-   **Cause \(Confirmed\)**- Confirmed cause of the incident.
-   **Contributing Cause \(Suspected\)**- Suspected cause of the incident.
-   **Consequences**- Resulting impact or penalties arising from the incident.

</td></tr><tr><td>

Actions &amp; Outcomes

</td><td>

Summary of actions taken during the investigation, captured from the **Action Tasks** and **Breach assessment** tabs.-   **Investigation**- Initial investigation tasks to examine the reported incident.
-   **Assessment**- Breach assessment to evaluate the risk and extent of compromised data.
-   **Additional Actions Taken**- Supplementary actions to support a resolution.

</td></tr><tr><td>

Lessons Learned

</td><td>

AI-powered analysis of the case timeline and overall investigation effort.-   **Velocity analysis**- Time to detect, investigate, and remediate.
-   **Investigation effort level**- Effort assessment ranked as low, medium, or high, based on case complexity, activity log, and timelines.

</td></tr></tbody>
</table>**Related topics**  


[Activate the GRC case summarization skill](../../now-assist-irm/task/activate-grc-case-summarization-skill.md)

[Summarize a privacy case using the GRC case summarization skill](../task/summarize-privacy-case.md)

