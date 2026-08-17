---
title: Activate the Document screening Al skill in ServiceNow Otto for PSDS
description: Activate the Document screening AI skill to use ServiceNow Otto for PSDS gen-AI to screen documents in the Social Benefits Playbook. The skill classifies document types, validates them against case requirements, and flags issues with clear explanations. Agents receive AI-composed messages to send to constituents with resubmission instructions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-ai-skills-doc-screening-activate.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Activate ServiceNow Otto skills, Configure, ServiceNow Otto for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Activate the Document screening Al skill in ServiceNow Otto for PSDS

Activate the Document screening AI skill to use ServiceNow Otto for PSDS gen-AI to screen documents in the Social Benefits Playbook. The skill classifies document types, validates them against case requirements, and flags issues with clear explanations. Agents receive AI-composed messages to send to constituents with resubmission instructions.

## Before you begin

**Important:** Some generative AI skills, agents, and agentic workflows are turned on by default. The default behavior works as follows:

-   **New customers**

    When you install an AI product, designated generative AI skills, AI agents, or agentic workflows are turned on automatically.

-   **Existing customers who are upgrading \(starting with Zurich Patch 4\)**

    There is no change to skills, agents, or agentic workflows that are currently enabled and customized.

    An AI asset is turned on if:

    -   The AI plugin is installed, but the asset was never turned on.
    -   An admin has never adjusted roles for the skill.
    An AI asset is not turned on if:

    -   The asset was previously turned on, and then turned off again.
    -   An admin has adjusted roles for the asset.

For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

-   Confirm that the following applications and plugins are installed:

    -   ServiceNow Otto in Document Intelligence \(sn\_docintel\_gen\_ai\)
    -   Document Processor \(sn\_doc\_processor\)
    -   Service Applicant Information \(sn\_svc\_appl\_info\)
    -   ServiceNow Otto for Public Sector Digital Services \(PSDS\)
    -   Social Benefits Playbook, Grants Management, **or** License and Permit Playbook
    For more information on configuring ServiceNow Otto in Document Intelligence, see [Configuring Now Assist in Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/docintel-configuring-now-assist.md).

-   Perform this task in your ServiceNow instance, ensuring the ServiceNow Otto for Public Sector Digital Services \(PSDS\) Application scope is selected.
-   Role required: admin

**Note:** AI Admin Hub \(sn\_nowassist\_admin\) and ServiceNow Otto for Platform \(sn\_genai\_platform\) plugins must be installed.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **ServiceNow Otto Skills**.

2.  In the workflow list, select **Customer** &gt; **PSDS**.

3.  On the card for the Document screening Al skill, select **Turn on**.

    \[Omitted image "psds-activate-doc-screening-skill-otto.png"\] Alt text: Document screening Al skill card that displays the skill to be turned on.

4.  Configure user access on the pop-up modal to specify who can use this skill.

    Access control lists \(ACLs\) are implemented to identify the users permitted to access this skill, and are generated automatically\).

5.  Select **Turn on**.

6.  In the dialog box, select **Back to skills**.

7.  Verify that the skill is activated on the Document Screening Al skill card.

    \[Omitted image "psds-doc-screening-skill-activated-otto.png"\] Alt text: Document screening Al skill is active.


