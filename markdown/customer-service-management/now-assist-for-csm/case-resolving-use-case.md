---
title: Customer Service Management AI agent collection triage cases agentic workflow
description: Use CSM AI agents agentic workflow to process all routine cases coming in through email and other offline channels and increase agent productivity through faster resolution.
locale: en-US
release: xanadu
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2025-02-21"
reading_time_minutes: 4
keywords: [Generative AI, generative AI for Customer Service Management, generative AI for customer service agents, AI agents for Customer Service Management Triage cases agentic workflow]
breadcrumb: [Using agentic workflows in CSM, Now Assist for Customer Service Management \(CSM\), Customer Service Management]
---

# Customer Service Management AI agent collection triage cases agentic workflow

Use CSM AI agents agentic workflow to process all routine cases coming in through email and other offline channels and increase agent productivity through faster resolution.

## Triage cases overview

Using the Triage cases agentic workflow, handle end-to-end validation, creation, verification, and escalation of cases or case types. Get the correct information from the case or interaction to answer customer questions directly and reduce the number of cases that must be created.

Refer to the information provided here on agents, tools, and triggers that are related to the Triage cases agentic workflow in AI agents for Customer Service Management.

To modify the Triage cases agentic workflow [duplicate it](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US), and adjust the settings according to your requirements. You can activate the agentic workflow template by making triggers active and setting the display settings to include the Now Assist panel.

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

## Triage cases agentic workflow

Triage and provide faster resolution for all the routine cases coming in through email and other offline channels.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage.**
2.  Select **Triage cases**.

## Access control lists \(ACLs\)

Access Control Lists \(ACLs\) are preconfigured to support the Triage use case, including AI agents and their associated flows and actions, such as the Document Verification Agent. By default, ACLs are configured for the sn\_esm\_agent role. Customers can modify these ACLs to align with their specific business requirements and security policies. For more information, see [Access Control List Rules](https://www.servicenow.com/docs/access?context=access-control-rules&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

When updating the agent role for the Triage Cases Agentic Workflow, it’s important to also update the corresponding Access Control Lists \(ACLs\) to ensure proper permissions. To manually update ACLs for custom roles:

1.  Go to the **sys\_security\_acl** table.
2.  Use filters to locate ACLs related to your use case, AI agent, and internal flows or actions.
3.  Add your custom role to each relevant ACL record.

## Triage cases AI agents

The following tables list the agents that are used in the Triage cases agentic workflow.

**Important:** In the **Define availability** screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

|AI agent|AI agent role|
|--------|-------------|
|Triage cases planner|Coordinates the verification of records, extracts essential information, and analyzes the intent and sentiment to determine the next steps in the process.|
|Context validator and analyzer|Validates the incoming record and analyzes the sentiment and intents from the input record.|
|Duplicate identification|Verifies duplicate cases or interactions are spotted early to avoid creating redundant records. If a similar record exists, the system links the new entry to the existing one rather than generating a duplicate.|
|Informational queries|Automatically responds to informational queries by supplying relevant content from the knowledge base.|
|Transactional queries|Handles transactional requests, such as field updates and responds to the customer.|
|Case creation|Assesses a record to determine if it meets all the requirements for creation and then validates the record to identify if it needs user communication for additional information or conversion into a specific case or case type.|
|Entity extraction|Extracts key pre-defined fields from the email body or documents according to configurable instructions.|
|Document verification|Validates the required documents attached to the record and extracts relevant information from the documents.|
|Email response|Consolidates and displays email responses, facilitates draft creation, and supports email sending according to the intent and query.|

## Triaging the case

In the triaging the case agentic workflow, perform the following steps:

1.  Review the information in the Describe and connect screen, make the necessary updates to verify the agentic workflow adapts to your requirements, and then select **Save and Continue**.
2.  In the Define trigger screen, activate the triggers that adapt to your requirements, or create your own triggers, and then select **Save and Continue**.
3.  In the Select display screen, perform the following steps:
    1.  Select where you want the agentic workflow output to be displayed.
    2.  Use the arrow next to it to add roles that can access the agentic workflow.

        **Note:** sn\_esm\_agent is the default role for the agentic workflow.

    3.  Select **Save and test**.

The agent executes the **testing** in AI Agent Studio for the agentic workflow.

![AI Agent Studio showing the testing output for Triage cases agentic workflow.](../image/case-resolving-use-case-output-in-ai-agent-studio.png "Example of a Triage cases agentic workflow testing in AI Agent Studio")

In the Now Assist panel, the agent receives a notification as soon as the interaction is generated, which enables them to follow the on-screen instructions and complete the task. For more information, see [Request the generative AI capabilities in Customer Service Management by using the Now Assist panel](../task/request-gen-ai-capabilities-csm-now-assist-panel.md).

