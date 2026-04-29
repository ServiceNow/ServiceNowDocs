---
title: Exploring Agentic Playbooks
description: Integrate AI agents into your workflows, and enable automation, adaptability, and transparency across your business processes.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Agentic Playbooks, Workflow Studio, Build workflows]
---

# Exploring Agentic Playbooks

Integrate AI agents into your workflows, and enable automation, adaptability, and transparency across your business processes.

## Agentic Playbooks overview

An agentic playbook consists of the same components as a regular \(deterministic\) playbook, except that AI agents are configured to perform certain activities of the playbook. For example, consider an incident management playbook that includes three activities: Finding related incidents, conducting root cause analysis, and identifying remedial actions for an incident. In a traditional setup, the service desk personnel must gather all the necessary information to complete these activities. However, when AI agents are enabled and configured for the playbook, they can perform each activity on behalf of the service desk personnel. The service desk personnel can review, approve, or edit the AI-generated responses to complete the playbook.Alternatively, you can configure AI agents to complete activities without any human intervention.

## Agentic Playbooks benefits

Agentic Playbooks bring the following benefits:

-   Makes the processes efficient
-   Automates the tedious manual tasks
-   Provides compliant outcomes across workflows
-   Uses context-aware interactions via Now Assist

## AI agents and their skills

Agentic Playbooks are powered by the **Playbook Activity Assist** agentic workflow \(See: [Now Assist agentic workflows](https://www.servicenow.com/docs/access?context=sn-aia-use-cases-list&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)\). The workflow contains a range of AI agents designed to enhance user experience and productivity. These agents are categorized based on their functionality and the tasks they perform.

-   **Playbook data gathering agent**

    The Playbook Data Gathering Agent handles user objectives that require fetching or searching for data. It intelligently determines the appropriate method for data retrieval based on the input.

<table id="table_j21_lwx_ygc"><thead><tr><th>

Script name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Knowledge Graph TextToResult API Crawler

</td><td>

Gathers data by using ServiceNow Knowledge Graph.You can also use a custom knowledge graph schema for the agent. To know more about knowledge graphs, see [Exploring Knowledge Graph](https://www.servicenow.com/docs/access?context=exploring-knowledge-graph&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

</td></tr><tr><td>

Knowledge articles retriever tool

</td><td>

Retrieves knowledge articles using AI-search capabilities.

</td></tr><tr><td>

AI Search Data Retriever

</td><td>

Uses AI Search to deliver relevant results by identifying and searching the most relevant tables related to the objective.

</td></tr><tr><td>

Retrieve attachments of a Glide record

</td><td>

Returns a list of attachments for a Glide record, including file names and sys\_ids.

</td></tr><tr><td>

Summarize attachments

</td><td>

Summarizes image attachments or image attachments on a record upon user request.This script is best suited for objectives that involve retrieving information from files such as PDFs and images,

</td></tr><tr><td>

Use web search

</td><td>

Uses web search tools to assist users in resolving issues by analyzing problems and generating resolution steps. It is designed for troubleshooting and resolving both technical and non-technical issues. You can leverage Google search or Bing search by using this agent.

</td></tr></tbody>
</table>-   **Playbook activity context agent**

    The Playbook activity context agent assists users in completing ServiceNow forms by:

    1.  Fetching relevant form fields
    2.  Automatically populating fields with available data
    3.  Prompting users for required information that is missing
    This agent also maintains a summary of its activities.

    |Script name|Description|
    |-----------|-----------|
    |Playbook slot filling script|Fetches the relevant schema required to understand and execute the playbook based on the playbook activity context ID and saves the agent response back to the activity context using the activity context ID. It also consolidates activity form fields and UI visible fields under the schema.|


For more information about Now Assist AI agents and their capabilities, refer to [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## User personas

If you're a playbook author and want to configure activities to be performed by AI agents, see [Configuring Agentic Playbooks](../task/configure-agentic-playbooks.md).

If you're an agent running a playbook, see [Using Agentic Playbooks](../task/running-agentic-activities.md).

