---
title: Generate OT KB articles agentic workflow
description: Use the Generate OT KB articles agentic workflow to generate a KB article when an Operational Technology \(OT\) incident is resolved.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use agentic AI for OTSM, Now Assist for OTSM, Operational Technology]
---

# Generate OT KB articles agentic workflow

Use the Generate OT KB articles agentic workflow to generate a KB article when an Operational Technology \(OT\) incident is resolved.

## Generate OT KB articles overview

With the Generate OT KB articles agentic workflow, you can automatically generate a KB article for an OT incident when the state of the incident is set to **Resolved**. The article contains the following information.

-   **Site**

    Site where the incident occurred.

-   **OT Device**

    Affected OT device at the site.

-   **Equipment model entity**

    Affected equipment model entity at the site.

-   **Summarization**

    The AI-generated summary, which includes the issue, key actions taken, and OT incident tasks if applicable.

-   **Resolution notes**

    AI-generated resolution notes from the OT Resolution Notes generation skill.

-   **KB Base**

    The Knowledge Base where the generated KB article is stored. The KB Base for the OTSM agentic workflow is the AI Agent OT Knowledge Base.

-   **Author**

    The author that publishes the generated KB article. The author for the OT agentic workflow is the OTSM Knowledge Generator AI Agent.


The article is then automatically published and appears in the Attached Knowledge related list of the OT incident record in the Industrial Workspace. The KB Article Generation process isn't triggered if there's an article already attached to current OT incident.

If you want to change this agentic workflow, you can [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md), adjust the settings to suit your specific needs, and activate the duplicated version of the agentic workflow instead.

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure you update all instructions accordingly.

The minimum role needed to duplicate an agentic workflow is the **sn\_aia.admin** role. By default, the OTSM agentic workflow is inactive. If you want to use the OOB agentic workflow, you can activate the OOB trigger. But if you want to customize the agentic workflow, you must duplicate it.

## AI agents used in the Generate OT KB articles agentic workflow

The OT knowledge generator AI agent is used to generate a KB article related for a resolved OT incident.

**Important:** This agent is turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

