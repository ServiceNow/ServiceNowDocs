---
title: IT Service Management AI agent collection Triage and categorize ITSM incidents agentic workflow
description: Use the Triage and categorize ITSM incidents AI agent team to assign incident categories and subcategories. Then, assign the service, service offering, and the configuration items \(CI\), and also link major incidents, and known problems autonomously.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [ITSM, Use agentic AI in IT Service Management, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# IT Service Management AI agent collection Triage and categorize ITSM incidents agentic workflow

Use the Triage and categorize ITSM incidents AI agent team to assign incident categories and subcategories. Then, assign the service, service offering, and the configuration items \(CI\), and also link major incidents, and known problems autonomously.

## Triage and categorize ITSM incidents agentic workflow overview

Using the Triage and categorize ITSM incidents agentic workflow, autonomously assign incident categories by assigning a category and a subcategory to incidents based on the incident short description. After categorizing the incident, assign the service, service offering, and configuration item \(CI\) related to the incident. Then, automatically link incidents to major incidents or known problems.

To modify the Triage and categorize ITSM incidents agentic workflow, [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements.

**Note:** You must enable the semantic indexing for the Problem table when you duplicate the agentic workflow. For more information, see [Semantic Index Field form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/semantic-index-field-form.md).

**Important:** When you modify an agentic workflow, AI agent, or a tool, make sure that you update all instructions accordingly.

**Important:** To search for related major incidents, you must activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\). For more information, see [Activate Incident Management - Major Incident Management](../../incident-management/task/activate-major-incident-management-plugin.md).

## Triage and categorize ITSM incidents agentic workflow

This workflow does the following:

1.  Automatically categorizes the incidents.
2.  Then, assigns the related service, service offering, and configuration item \(CI\).
3.  Then, searches for related major incidents and if found, links them to the incident.
4.  If no major incidents are found, then it searches for related problems, and if found, links them to the incident.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Triage and categorize ITSM incidents**.

**Important:** In the Edit trigger form, make sure that the **Active** button is turned on to enable the AI agent to trigger autonomously. You must enter the sys\_id of the user with the itil role when the trigger is activated.

## Setting automatic or manual triggers for the agentic workflow

Based on the incident assignment, state, and priority, the Triage and categorize ITSM incidents agentic workflow is triggered either automatically or manually.

<table id="table_w5k_4tt_1fc"><thead><tr><th>

Type of trigger

</th><th>

Field values

</th></tr></thead><tbody><tr><td rowspan="2">

Automatic

</td><td>

-   **State** is **New**
-   **Assigned to** is **empty**
-   **Priority** is **3, 4, or 5**

</td></tr><tr><td>

-   **State** is updated to **In progress**
-   **Assigned to** is empty
-   **Priority** is **3, 4 and 5**

</td></tr><tr><td>

Manual

</td><td>

-   **State** is **In progress**
-   **Assigned to** isn’t empty

</td></tr></tbody>
</table>## Setting the AI user as the Run as user

The ITSM Worker AI Agent user record is of identity type **AI agent** and is available by default. You can create users of this type and assign roles to the users based on your needs.

Add the AI agent user as the Run as user:

1.  Navigate to the **Define key requirements** screen.
2.  Go to the **Select the entity this agentic workflow will run as** section.
3.  In the **Run as** field, select **AI user**.
4.  In the **AI user** field, select the desired AI agent user.

## AI agents used in the Triage and categorize ITSM incidents agentic workflow

The Triage and categorize ITSM incidents agentic workflow uses a team of AI agents to automatically categorize incidents, then assign the service, service offering, and configuration item \(CI\) related to the incident and then links associated major incidents or known problems.

**Important:** In the Define availability screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

<table id="table_abj_5lk_j2c"><thead><tr><th>

AI agent

</th><th>

AI agent role

</th></tr></thead><tbody><tr><td>

Categorize ITSM incident AI agent

</td><td>

Automatically assigns incidents to categories, and subcategories, based on the incident's short description.

</td></tr><tr><td>

Classify service and CI AI agent

</td><td>

Automatically assigns service, service offerings, and configuration items \(CI\) to the incidents.

</td></tr><tr><td>

Link major incident or problem AI agent

</td><td>

**Important:** To search for related major incidents, you must activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\). For more information, see [Activate Incident Management - Major Incident Management](../../incident-management/task/activate-major-incident-management-plugin.md).

 -   If this AI agent identifies a related, most similar major incident, it automatically links it to the current incident and ends the workflow.
-   If the Major incident linker AI agent doesn't find a related major incident, then the Incident problem linker AI agent takes over. If it identifies any ongoing problem that best matches the incident, then it automatically links it to the incident.

</td></tr></tbody>
</table>## Assigning incident categories

In the agentic workflow record:

1.  Review the information in the Describe and connect screen and in the Define trigger screen. Make the necessary updates, and then select **Save and Continue**.
2.  In the Select display screen:
    1.  Choose where you want the agentic workflow output to be displayed.
    2.  Use the arrow next to the display option to add roles that can access the agentic workflow.

        **Note:** The itil role is added by default.

    3.  Select **Save and test**.

        The agent executes the request for the agentic workflow.


**Example of Triage and categorize ITSM incidents agentic workflow output in the ServiceNow AI Agent Studio**![Triage and categorize ITSM incidents agentic workflow output.](../image/now-assist-itsm-aiagents-inc-triage-classify.png)

In the AI Agent Studio, the human agent gets notified as soon as the category recommendation is generated so that they can follow the on-screen instructions and complete the task. For more information, see [Request the generative AI capabilities in ITSM by using the Now Assist panel](../task/request-gen-ai-capabilities-itsm-now-assist-panel.md).

## Automate the categorizing an incident, then automatically link them to major incidents or known problems in the Now Assist panel

When an incident is updated and the trigger conditions are met, an execution plan is created. The incident fields are updated based the execution by each AI agent.

As a user, do the following in the Now Assist panel:

1.  Enter a message in the Now Assist panel, such as, "triage incident INC0010010".

    All executions are autonomous and the AI agent does need user inputs in any of the steps during the execution.

2.  The first AI agent, which is the Categorize ITSM incident AI agent does the following:
    1.  Updates the following fields in the incident record after the execution:
        -   Category
        -   Sub-category
    2.  Updates any changes in the **Work notes** field.

        The orchestrator then moves to the next available agent.

        ![](../image/now-assist-itsm-inc-cat-nap.png)

3.  The second agent, which is the Classify Service and CI AI agent updates the following fields in the incident record after the execution:

    -   Service
    -   Service offering
    -   Configuration item
    It also updates the **Additional comments** and **Work notes** fields.

    ![Now Assist for ITSM Categorize Incidents Additional Comments](../image/now-assist-itsm-inc-cat-add-comm.png)

4.  The third agent, which is the Link major incident or problem AI agent updates the parent **incident** or **problem** field in the incident's related record. The AI agent updates the changes in the **Additional comments** field.

![Now Assist ITSM Categorize Incidents Related Records](../image/now-assist-itsm-inc-cat-related-records.png)

The image below shows the following:

-   The Categorize ITSM incident AI agent populates the **Category** and **Subcategory** fields.
-   The Classify service and CI AI agent populates the **Service**, **Service offering**, and **Configuration items** fields.
-   The Link major incident or problem AI agent populates the **Parent incident** or the **Problem** field.

![Now Assist ITSM categorize incidents workflow fields populated](../image/now-assist-itsm-inc-cat-fields.png)

