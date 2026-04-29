---
title: Customer Service Management AI agent collection triage cases agentic workflow
description: Use CSM AI agents agentic workflow to process all routine cases coming in through email and other offline channels and increase agent productivity through faster resolution.
locale: en-US
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Generative AI, generative AI for Customer Service Management, generative AI for customer service agents, AI agents for Customer Service Management Triage cases agentic workflow]
breadcrumb: [Use agentic AI in CSM, Now Assist for CSM, Customer Service Management]
---

# Customer Service Management AI agent collection triage cases agentic workflow

Use CSM AI agents agentic workflow to process all routine cases coming in through email and other offline channels and increase agent productivity through faster resolution.

## Triage cases overview

Using the Triage cases agentic workflow, handle end-to-end validation, creation, verification, and escalation of cases or case types. Get the correct information from the case or interaction to answer customer questions directly and reduce the number of cases that must be created.

Refer to the information provided here on agents, tools, and triggers that are related to the Triage cases agentic workflow in AI agents for Customer Service Management.

To modify the Triage cases agentic workflow [duplicate it](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US), and adjust the settings according to your requirements. You can activate the agentic workflow template by making triggers active and setting the display settings to include the Now Assist panel.

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

## Triage cases agentic workflow

Triage and provide faster resolution for all the routine cases coming in through email and other offline channels.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage.**
2.  Select **Triage cases**.

## Access control lists \(ACLs\)

Access Control Lists \(ACLs\) are preconfigured to support the Triage use case, including AI agents and their associated flows and actions, such as the Document Verification Agent. By default, ACLs are configured for the sn\_esm\_agent role. Customers can modify these ACLs to align with their specific business requirements and security policies. For more information, [Configure security controls for a skill](https://www.servicenow.com/docs/access?context=nask-access-control&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

When updating the agent role for the Triage Cases Agentic Workflow, it’s important to also update the corresponding Access Control Lists \(ACLs\) to ensure proper permissions. To manually update ACLs for custom roles:

1.  Go to the **sys\_security\_acl** table.
2.  Use filters to locate ACLs related to your use case, AI agent, and internal flows or actions.
3.  Add your custom role to each relevant ACL record.

## Triage cases AI agents

The following tables list the agents that are used in the Triage cases agentic workflow.

**Important:** In the **Define availability** screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

|AI agent|AI agent role|
|--------|-------------|
|Triage cases WrapUp|Wrap up the case triage process using the Triage Cases Wrapup AI Agent. It synthesizes the execution details and posts the summary to the work notes of the source record to ensure traceability and closure.|
|Context validator|Validate the content of a record using the Context Validator AI Agent. It analyzes sentiment and identifies a list of intents from the input record. Invoke this agent whenever record content requires validation and intent classification.|
|Informational queries|Create a summary of all answers related to informational intent using the Informational Queries AI Agent. It retrieves a list of all intents, then processes each informational intent individually before generating the final summary. Invoke this agent whenever a consolidated response to informational queries is required.|
|Case creation|Automate and manage the end-to-end process of case creation using the Case creation AI agent. Invoke this agent whenever a case needs to be created.|
|Entity extraction|Extract entities from emails and documents using the Entity Extraction AI Agent. It matches the extracted entities against a predefined allowlist of fields to ensure relevance and accuracy. Invoke this agent whenever entity-level information needs to be identified and structured from unstructured content.|
|Document verification|Verify documents on a record using the Document Verification AI Agent to determine whether they match the required list for the case type. It identifies any missing documents or verification failures. Invoke this agent whenever document validation is needed.|
|Email response|Generate and send email responses using the Email Response AI Agent. It acts as a response assistant to draft, display, and deliver email replies. Invoke this agent whenever an automated email response is required.|

## Role masking

Required role: B2B agents \(sn\_customerservice\_agent\) and B2C agents \(sn\_customerservice.consumer\_agent\)

**Important:** To access data in the agentic workflow, the admin role must include the specified roles under **Contains roles**.

Agentic workflows and their AI agents use [role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

In the data access settings, you must also add the necessary roles to access the cases that need triaging. For example, you can add the csm role to the agentic workflow's list of approved roles so that it can access case records.

## Triaging the case

In the triaging the case agentic workflow, perform the following steps:

1.  In **Define key requirements** the workflow’s purpose is clearly described and its steps with specific actions and criteria for each is outlined.
2.  In the **Define security controls** screen, you can set the access at user and data level.

    1.  **Define user access**: Specify which users can access and interact with the agentic workflow. Once you save your selections, the system automatically generates an Access Control List \(ACL\).
    2.  **Define data access**: Choose the user identity under which the Provide customer 360 insights agentic workflow will run. This determines the roles and associated data access permissions.

        **Note:** Choose the user identity this agentic workflow should run as to determine the roles and the data access permissions derived from them. Remember, when agentic workflows can access data, they can also share that data with the human user who interacts with them. Agent level role mask are: B2B agents \(sn\_customerservice\_agent\) and B2C agents \(sn\_customerservice.consumer\_agent\).

    1.  In **Add triggers** you can set up optional triggers to launch the agentic workflow automatically without a user request. Triggers can be based on conditions or schedules you define and initiate agentic AI experiences.
    2.  In **Select channels and status**, you can choose the channels where this agentic workflow will be available to engage with users who initiate interactions. Toggle the display for **Engage via the Now Assist panel** to see the agentic flow in Now Assist panel.

        **Note:** To turn off the agentic workflow, toggle off **Engage via the Now Assist panel**.

    3.  Select **Save and test**.
    The agent executes the **testing** in AI Agent Studio for the agentic workflow.


![AI Agent Studio showing the testing output for Triage cases agentic workflow.](../image/case-resolving-use-case-output-in-ai-agent-studio.png "Example of a Triage cases agentic workflow testing in AI Agent Studio")

In the Now Assist panel, the agent receives a notification as soon as the interaction is generated, which enables them to follow the on-screen instructions and complete the task. For more information, see [Request the generative AI capabilities in Customer Service Management by using the Now Assist panel](../task/request-gen-ai-capabilities-csm-now-assist-panel.md).

