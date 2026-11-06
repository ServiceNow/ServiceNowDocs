---
title: Customer Service Management AI agent collection triage cases agentic workflow
description: Use CSM AI agents agentic workflow to process all routine cases coming in through email and other offline channels and increase agent productivity through faster resolution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/now-assist-for-csm/case-resolving-use-case.html
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 10
keywords: [Generative AI, generative AI for Customer Service Management, generative AI for customer service agents, AI agents for Customer Service Management Triage cases agentic workflow]
breadcrumb: [Use agentic AI in CSM, ServiceNow Otto for CSM, Customer Service Management]
---

# Customer Service Management AI agent collection triage cases agentic workflow

Use CSM AI agents agentic workflow to process all routine cases coming in through email and other offline channels and increase agent productivity through faster resolution.

## Triage cases overview

Using the Triage cases agentic workflow, handle end-to-end validation, creation, verification, and escalation of cases or case types. Get the correct information from the case or interaction to answer customer questions directly and reduce the number of cases that must be created.

Refer to the information provided here on agents, tools, and triggers that are related to the Triage cases agentic workflow in AI agents for Customer Service Management.

To modify the Triage cases agentic workflow [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements. You can activate the agentic workflow template by making triggers active and setting the display settings to include the ServiceNow Otto panel.

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

## Triage cases agentic workflow

Triage and provide faster resolution for all the routine cases coming in through email and other offline channels.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage.**
2.  Select **Triage cases**.

## Triggers for Triage cases agentic workflow

In the Define trigger screen, the agentic workflow begins executing when the trigger meets the following conditions:

1.  Case
    -   Set the Target table field to sn\_customerservice\_case.
    -   Set the **Run as** field value to **Assigned to**.
    -   Set the following conditions:
        -   **\[State\]** changes to **\[Open\]** and
        -   **\[Assigned to\]** is **\[not empty\]** and
        -   **\[Priority\]** in **\[3-Moderate, 4 Low\]**
2.  Interaction
    -   Set the Target table to Interaction.
    -   Set the **Run as** field value to **Assigned to**.
    -   Set the following conditions for a contact:

        -   **\[State\]** changes to **\[Work in Progress\]** and
        -   **\[Assigned to\]** is **\[not empty\]** and
        -   **\[Account\]** is **\[not empty\]** and
        -   **\[Contact\]** is **\[not empty\]**
        And set the following conditions for a consumer:

        -   **\[State \]** changes to **\[Work in Progress\]** and
        -   **\[Assigned to\]** is **\[not empty\]** and
        -   **\[Consumer\]** is **\[not empty\]**
        -   **\[Type\]** is **\[Email\]**

**Important:** In the Edit trigger form, make sure that the **Active** button is turned on to trigger the AI agent autonomously.

## Access control lists \(ACLs\)

Access Control Lists \(ACLs\) are preconfigured to support the Triage use case, including AI agents and their associated flows and actions, such as the Document Verification Agent. By default, ACLs are configured for the sn\_esm\_agent role. Customers can modify these ACLs to align with their specific business requirements and security policies. For more information, [Configure security controls for a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/nask-access-control.md).

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

## Tools mapped to Case context gatherer

|Tool type|Execution mode|Name|Description|
|---------|--------------|----|-----------|
|Flow actions|Supervised|Create Case or Case Type from Source Record|Creates a case or case type and returns the sys\_id and the URL of the newly created record.|
|Flow actions|Autonomous|Determine Case Type|Returns the case type that has been identified from the given content.|
|Flow actions|Autonomous|Close Interaction|Closes the interaction by using the record sys\_id.|
|Flow actions|Autonomous|Update Work Notes|Updates the work notes of the record by using the record's summary as the work note content.|
|Flow actions|Autonomous|Create and link interaction to case|Creates and links interactions to cases. Uses the new record sys\_id as the target sys\_id, the case type as the target table, and the record sys\_id as the interaction sys\_id.|
|Flow actions|Autonomous|Get Record Details|Gathers the record details for the interaction, cases, and email's reply.|
|Scripts|Autonomous|Summarize a record|Returns the record's summary.|
|Scripts|Autonomous|Create consolidated context summary|Creates the consolidated context summary by using the output of the fields and the document's verification process.|

## Tools mapped to the Information email responder

|Tool type|Execution mode|Name|Description|
|---------|--------------|----|-----------|
|Flow actions|Autonomous|Get Record Details|Gathers the record details for interactions, cases, and email replies.|
|AI skills|Supervised|Email Response|Generates an email response based on the inputs provided.|
|Scripts|Autonomous|Draft Email|Creates an email draft.|
|Scripts|Autonomous|Send Email|Sends an email from the email draft.|

## Tools mapped to the Customer escalation handler

|Tool type|Execution mode|Name|Description|
|---------|--------------|----|-----------|
|Flow actions|Autonomous|Get Record Details|Fetches the details of the records by using the record table and either the record sys\_id or record number.|
|Flow actions|Autonomous|Get Intents|Returns the intent that has been identified in the source record's content.|
|Scripts|Autonomous|Look up and verify the record|Looks up and verifies the record to identify if the record is valid to continue the process.|
|Scripts|Autonomous|Get email reply content|Gets the email reply content by using the question, answer, and the consolidated context summary.|
|Search retrievals|Autonomous|Get relevant knowledge articles|Fetches knowledge articles that contain similar and relevant information to the search query.|

## Tools mapped to the Customer information verifier

|Tool type|Execution mode|Name|Description|
|---------|--------------|----|-----------|
|Flow actions|Autonomous|Get all fields|Returns all fields.|
|Flow actions|Autonomous|Check for missing fields|Returns an array of final verified fields.|
|Flow actions|Autonomous|Slot fill|Returns the fields that have been identified in the content.|
|Scripts|Autonomous|Get custom fields|Returns the array of custom fields that are specified by the customer.|

## Tools mapped to the Customer document verifier

|Tool type|Execution mode|Name|Description|
|---------|--------------|----|-----------|
|Scripts|Autonomous|Status report|Returns the status.|
|Scripts|Autonomous|Documents Checklist|Gets the list of documents based on a Case Type.|
|Subflows|Autonomous|Initiate Document Verification|Returns the response after initiating the verification.|
|Subflows|Autonomous|Verify the documents|Gets the output after verifying the documents.|

## Tools mapped to the Troubleshooting steps identification AI agent

|Tool type|Execution mode|Name|Description|
|---------|--------------|----|-----------|
|Flow action|Autonomous|Get case details|Gets and displays troubleshooting steps performed by the user from case work notes.|
|RAG Tool|Autonomous|Get similar cases, relevant knowledge articles and documents|Gets relevant KB articles, resolved cases, and documents attached to knowledge articles based on the case short description using either RAG tool or AI search.|
|Script|Autonomous|Get documents list|Fetches the list of documents \(.pdf, .docx, .xlsx, and so on\) attached to records fetched from AI search.|
|Script|Autonomous|Initiate troubleshooting steps extraction|Asks user to choose from documents fetched for the most relevant troubleshooting steps then initiates the extraction process by creating a DocIntel task.|
|Script|Autonomous|Get troubleshooting steps from document|Uses a DocIntel task to extract the actual troubleshooting steps from the document.|
|Script|Autonomous|Update the case with work notes|Asks the human agent to update the consolidated list of suggested troubleshooting steps.|

## Role masking

Required role: B2B agents \(sn\_customerservice\_agent\) and B2C agents \(sn\_customerservice.consumer\_agent\)

**Important:** To access data in the agentic workflow, the admin role must include the specified roles under **Contains roles**.

Agentic workflows and their AI agents use role masking to determine which users can access them. Ones installed with your applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aw.md).

In the data access settings, you must also add the necessary roles to access the cases that need triaging. For example, you can add the csm role to the agentic workflow's list of approved roles so that it can access case records.

## Triaging the case

In the triaging the case agentic workflow, perform the following steps:

1.  In **Define key requirements** the workflow’s purpose is clearly described and its steps with specific actions and criteria for each is outlined.
2.  In the **Define security controls** screen, you can set the access at user and data level.

    1.  **Define user access**: Specify which users can access and interact with the agentic workflow. Once you save your selections, the system automatically generates an Access Control List \(ACL\).
    2.  **Define data access**: Choose the user identity under which the Provide customer 360 insights agentic workflow will run. This determines the roles and associated data access permissions.

        **Note:** Choose the user identity this agentic workflow should run as to determine the roles and the data access permissions derived from them. Remember, when agentic workflows can access data, they can also share that data with the human user who interacts with them. Agent level role mask are: B2B agents \(sn\_customerservice\_agent\) and B2C agents \(sn\_customerservice.consumer\_agent\).

    1.  In **Add triggers** you can set up optional triggers to launch the agentic workflow automatically without a user request. Triggers can be based on conditions or schedules you define and initiate agentic AI experiences.
    2.  In **Select channels and status**, you can choose the channels where this agentic workflow will be available to engage with users who initiate interactions. Toggle the display for **Engage via the ServiceNow Otto panel** to see the agentic flow in ServiceNow Otto panel.

        **Note:** To turn off the agentic workflow, toggle off **Engage via the ServiceNow Otto panel**.

    3.  Select **Save and test**.
    The agent executes the **testing** in AI Agent Studio for the agentic workflow.


\[Omitted image "case-resolving-use-case-output-in-ai-agent-studio.png"\] Alt text: AI Agent Studio showing the testing output for Triage cases agentic workflow.

In the Now Assist panel, the agent receives a notification as soon as the interaction is generated, which enables them to follow the on-screen instructions and complete the task. For more information, see [Request the generative AI capabilities in Customer Service Management by using the ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/now-assist-for-csm/request-gen-ai-capabilities-csm-now-assist-panel.md).

