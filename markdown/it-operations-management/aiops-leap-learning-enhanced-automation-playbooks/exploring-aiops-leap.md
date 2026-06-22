---
title: Exploring LEAP
description: LEAP categorizes similar incidents into groups and uses AI to generate resolution steps, problem records, AI-enhanced knowledge base articles, and playbooks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/exploring-aiops-leap.html
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Learning Enhanced Automation Platform \(LEAP\), Now Assist for ITOM, IT Operations Management]
---

# Exploring LEAP

LEAP categorizes similar incidents into groups and uses AI to generate resolution steps, problem records, AI-enhanced knowledge base articles, and playbooks.

## LEAP overview

LEAP helps you manage incidents and operational tasks efficiently. It uses AI to gather information from existing incidents and generates resolutions that can be automated. The LEAP automation provides tools to manage incidents early, speed up resolution, use prebuilt automation, and follow clear steps to handle issues. These tools help support smooth operations.

**Note:** The plugin name has been updated from AIOps Learning Enhanced Automation Playbook to Learning Enhanced Automation Platform \(LEAP\) to reflect its expanded capabilities and strategic direction.

\[Omitted image "aiops-leap-landing-page.png"\] Alt text: LEAP landing page

The landing page displays the number of records analyzed on the right-hand side of Automation opportunities section. The tool tip provides details about the duration considered for record analysis.

## Grouping of automation opportunities in LEAP

GAF \(Group Action Framework\) is the clustering engine that LEAP uses to group incidents into Automation Opportunities \(AOs\). GAF analyzes incident records using the short description field and applies ML-powered clustering to group incidents that share similar problem patterns. LEAP surfaces recurring issue types as discrete automation opportunities \(AOs\) rather than treating every incident in isolation.

GAF runs on a scheduled job, by default monthly. The schedule is configured during LEAP skill activation through the installer. On the first run, GAF processes up to six months of historical incident data using the filter set in the installer.

Before clustering begins, GAF selects the top N incidents from the eligible incident pool, where N is configurable and can be set to a maximum of 50. This selection confirms that clustering focuses on the most relevant and recent incidents within the defined scope. You can configure the fields GAF considers during analysis such as tables and columns in the LEAP settings. You can also modify the schedule run frequency in the LEAP settings.

## LEAP users

<table id="table_pny_2gg_42c"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

LEAP admin

</td><td>

You have full control over LEAP capabilities, including the following:

-   Turn features on and off
-   Execute scheduled jobs
-   Manage LEAP tables and the LEAP Workspace
-   Generate and update resolution steps
-   Generate AI-enhanced knowledge base articles, problem records, and playbooks from automation opportunities \(AO\)

</td></tr><tr><td>

LEAP viewer

</td><td>

You can access and view data related to LEAP, including tables, the workspace, and problems originating from AOs.

</td></tr><tr><td>

LEAP agent

</td><td>

You can access the LEAP menu from the Service Operations Workspace \(SOW\) and trigger LEAP executions directly from within SOW.

</td></tr></tbody>
</table>These roles work together to create a streamlined and secure approach for managing automation, resolving incidents, and sharing knowledge across teams.

## Personas in LEAP

LEAP supports different personas who can have different roles assigned to enhance IT Operations Management.

<table id="table_nj3_glg_42c"><thead><tr><th>

Persona

</th><th>

Description

</th><th>

Responsibility

</th></tr></thead><tbody><tr><td>

Automation architect

</td><td>

An automation architect is a senior technical expert who designs and develops automation solutions, scaling them when required. They're a bridge between IT operations, business needs, and automation strategy. The automation architect streamlines manual, repetitive, and error-prone tasks.

</td><td>

-   Identifies high-impact areas for automation
-   Develops automation scripts, integrate AI-driven insights, and maintain scalable automation frameworks
-   Extracts patterns from historical ticket data to optimize future resolutions
-   Refines automation solutions based on feedback and evolving business needs.
-   Collaborates with different business units to align automation with enterprise objectives.

</td></tr><tr><td>

IT operator

</td><td>

An IT operator includes all L1 and L2 incident handlers who support day-to-day IT operations.

</td><td>

-   Uses AI-generated playbooks to resolve incidents
-   Accesses the Knowledge Base

</td></tr><tr><td>

Buyer, Business goal owner

</td><td>

A buyer or a business goal owner gains strategic and operational advantages using LEAP.

</td><td>

-   Uses LEAP to improve IT operations
-   Optimizes resource allocation
-   Automates recurring issue resolution

</td></tr></tbody>
</table>An automation architect can use LEAP to gather feedback and refine solutions. In a similar manner, IT operators will use LEAP to detect recurring issues and LEAP displays suggestions for preventive automation. This enables faster resolution and operators can resolve more incidents independently leading to improved efficiency and service quality.

## LEAP benefits

|Benefit|Feature|
|-------|-------|
|Promotes automation culture|Interpret data and automate records|
|Drives incident resolution|Measure and enhance performance|
|Targets Outcomes for L1 Operators|Interpret data and automate records|
|Improves MTTR|Measure and enhance performance|
|Optimize Resource Allocation|Identify and prioritize high impact areas|
|Provides cost predictability|Fixed pricing model for incident analysis operations|

## LEAP AI agent

The LEAP AI agent uses automation opportunities created by LEAP analysis to generate artifacts — problem records, knowledge base articles, or playbooks — based on user requests.

|AI agent|AI agent role|
|--------|-------------|
|LEAP AI agent|Uses the automation opportunities created by LEAP analysis, and creates artifacts — problem records, AI-enhanced knowledge base articles, or playbooks — based on user requests.|

**Important:** This agent is turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

## What to explore next

To learn more about configuring and using LEAP, see:

-   [Configuring LEAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/configuring-aiops-leap.md)
-   [Using LEAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/using-aiops-leap.md)
-   [LEAP reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/references-aiops-leap.md)

