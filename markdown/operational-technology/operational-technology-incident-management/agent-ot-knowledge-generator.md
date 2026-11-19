---
title: Generate OT KB articles agentic workflow
description: The Generate OT KB articles agentic workflow automatically generates a KB article when an Operational Technology \(OT\) incident is resolved, capturing resolution information for future reference.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/operational-technology/operational-technology-incident-management/agent-ot-knowledge-generator.html
release: zurich
product: Operational Technology Incident Management
classification: operational-technology-incident-management
topic_type: concept
last_updated: "2026-07-23"
reading_time_minutes: 1
breadcrumb: [Agentic AI for Operational Technology Service Management, Use, Operational Technology Incident Management, Operational Technology]
---

# Generate OT KB articles agentic workflow

The Generate OT KB articles agentic workflow automatically generates a KB article when an Operational Technology \(OT\) incident is resolved, capturing resolution information for future reference.

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

To change this agentic workflow, [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/clone-aia-usecase.md), adjust the settings to suit your specific needs, and activate the duplicated version of the agentic workflow instead.

**Note:** When you modify an agentic workflow, AI agent, or tool, verify that you update all instructions accordingly.

The minimum role needed to duplicate an agentic workflow is the sn\_aia.admin role. By default, the OTSM agentic workflow is inactive. To use the base system agentic workflow, activate the base system trigger. To customize the agentic workflow, duplicate it.

## AI agents used in the Generate OT KB articles agentic workflow

The OT knowledge generator AI agent is used to generate a KB article for a resolved OT incident.

**Important:** This AI agent is turned on by default. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

**Parent Topic:**[Agentic AI for Operational Technology Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/operational-technology-incident-management/now-assist-otsm-use-cases.md)

