---
title: IT Service Management AI agent collection Triage and categorize ITSM incidents agentic workflow
description: Use the Triage and categorize ITSM incidents AI agent team to assign incident categories, subcategories, configuration items \(CI\), major incidents, and known problems autonomously.
locale: en-US
release: xanadu
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2025-02-07"
reading_time_minutes: 4
keywords: [Now Assist, Agentic AI]
breadcrumb: [Use agentic workflows in ITSM, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# IT Service Management AI agent collection Triage and categorize ITSM incidents agentic workflow

Use the Triage and categorize ITSM incidents AI agent team to assign incident categories, subcategories, configuration items \(CI\), major incidents, and known problems autonomously.

## Triage and categorize ITSM incidents agentic workflow overview

Using the Triage and categorize ITSM incidents agentic workflow, autonomously assign incident categories by assigning a category, subcategory, and a configuration item \(CI\) to incidents based on the incident short description. After categorizing the incident, automatically link incidents to major incidents or known problems.

To modify the Triage and categorize ITSM incidents agentic workflow, [duplicate it](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US), and adjust the settings according to your requirements.

**Note:** You must enable the semantic indexing for the Problem table when you duplicate the agentic workflow. For more information, see [Semantic Index Field form](https://www.servicenow.com/docs/access?context=semantic-index-field-form&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

**Important:** When you modify an agentic workflow, AI agent, or a tool, make sure that you update all instructions accordingly.

**Important:** To search for related major incidents, you must activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\). For more information, see [Activate Incident Management - Major Incident Management](../../incident-management/task/activate-major-incident-management-plugin.md).

## Triage and categorize ITSM incidents agentic workflow

This workflow does the following:

1.  Automatically categorizes the incidents.
2.  Then, searches for related major incidents and if found, links them to the incident.
3.  If no major incidents are found, then it searches for related problems, and if found, links them to the incident.

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
</table>## AI agents used in the Triage and categorize ITSM incidents agentic workflow

The Triage and categorize ITSM incidents agentic workflow uses a team of AI agents to identify the category, subcategory, and configuration item for an incident automatically, and link associated major incidents or known problems.

**Important:** In the Define availability screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

<table id="table_abj_5lk_j2c"><thead><tr><th>

AI agent

</th><th>

AI agent role

</th></tr></thead><tbody><tr><td>

Categorize incident AI agent

</td><td>

Automatically assigns service, service offerings, and configuration items \(CI\) to the incidents.

</td></tr><tr><td>

Link major incident AI agent

</td><td>

**Important:** To search for related major incidents, you must activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\). For more information, see [Activate Incident Management - Major Incident Management](../../incident-management/task/activate-major-incident-management-plugin.md).

If this AI agent identifies a related, most similar major incident, it automatically links it to the current incident and ends the workflow.

</td></tr><tr><td>

Link incident to problem AI agent

</td><td>

If the Major incident linker AI agent doesn't find a related major incident, then the Incident problem linker AI agent takes over. If it identifies any ongoing problem that best matches the incident, then it automatically links it to the incident.

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


**Example of Triage and categorize ITSM incidents agentic workflow output in the ServiceNow AI Agent Studio**![Triage and categorize ITSM incidents agentic workflow output .](../image/now-assist-itsm-aiagents-incident-triager-nap.png)

In the AI Agent Studio, the human agent gets notified as soon as the category recommendation is generated so that they can follow the on-screen instructions and complete the task. For more information, see [Request the generative AI capabilities in ITSM by using the Now Assist panel](../task/request-gen-ai-capabilities-itsm-now-assist-panel.md).

**Parent Topic:**[Using agentic workflows in Now Assist for ITSM](now-assist-itsm-ai-agents-use-cases.md)

