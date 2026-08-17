---
title: Exploring LEAP
description: LEAP categorizes similar incidents into groups and uses AI to generate resolution steps, problem records, AI-enhanced knowledge base articles, and playbooks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/exploring-aiops-leap.html
release: zurich
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Learning Enhanced Automation Platform \(LEAP\), ServiceNow Otto for ITOM, IT Operations Management]
---

# Exploring LEAP

LEAP categorizes similar incidents into groups and uses AI to generate resolution steps, problem records, AI-enhanced knowledge base articles, and playbooks.

## LEAP overview

LEAP helps you manage incidents and operational tasks efficiently. It uses AI to gather information from existing incidents and generates resolutions that can be automated. The LEAP automation provides tools to manage incidents early, speed up resolution, use prebuilt automation, and follow clear steps to handle issues. These tools help support smooth operations.

**Note:**

-   The plugin name has been updated from AIOps Learning Enhanced Automation Playbook to Learning Enhanced Automation Platform \(LEAP\) to reflect its expanded capabilities and strategic direction.
-   Now Assist is renamed to ServiceNow Otto.

\[Omitted image "aiops-leap-landing-page.png"\] Alt text: LEAP landing page

The landing page displays the number of records analyzed in the Automation opportunities section. The tooltip provides details about the duration considered for record analysis. [https://player.vimeo.com/video/1203972930?h=a3a7ebd490&amp;badge=0&amp;autopause=0&amp;player\_id=0&amp;app\_id=58479%22](https://player.vimeo.com/video/1203972930?h=a3a7ebd490&badge=0&autopause=0&player_id=0&app_id=58479%22)

When the LEAP homepage loads, it displays a banner that you can use to connect Ansible Automation Platform. The banner makes the Ansible automation integration discoverable so that you can connect the automation tool and map playbooks to resolution steps. Select **Connect** to open the LEAP settings page and configure the connection. To dismiss the banner, select **Remind me later**. The banner reappears when you refresh the homepage until a connection is configured. After you connect Ansible, the banner no longer appears on the homepage.

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

## What to explore next

To learn more about configuring and using LEAP, see:

-   [Configuring LEAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/configuring-aiops-leap.md)
-   [Using LEAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/using-aiops-leap.md)
-   [LEAP reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/references-aiops-leap.md)

