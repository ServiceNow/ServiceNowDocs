---
title: Help nurture new leads agentic workflow
description: Use the Help nurture new leads agentic workflow to process the entire lead record process.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use agentic workflows, Now Assist for SFA]
---

# Help nurture new leads agentic workflow

Use the Help nurture new leads agentic workflow to process the entire lead record process.

## Help nurture new leads agentic workflow overview

You can use the Help nurture new leads agentic workflow to do the following:

-   Proactively engage with initial leads
-   Book an appointment or demo to get the lead closer to qualification
-   Identify opt-outs and disinterest for lead disqualification

To modify the Help nurture new leads agentic workflow [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements. You can activate the agentic workflow template by making triggers active and setting the display settings to include the Now Assist panel.

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

## Help nurture new leads use cases

To access the use case:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **Use cases**.
2.  Select **Help nurture new leads**.

## Help nurture new leads AI agents

The following table lists the Help nurture new leads AI agents.

**Important:** In the Define availability screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

|AI agent|AI agent role|
|--------|-------------|
|Lead outreach AI agent|Initiates the outreach and follow-up flow. This flow supports sales agents by sending the initial outreach and follow-up emails.|
|Lead disinterest AI agent|Handles disqualification of the lead and opt-out requests.|
|Inbound email AI agent|Initiates the inbound response handler flow. This flow supports sales agents by retrieving and analyzing the latest email records. Based on its analysis, it recommends necessary actions required to move forward with the lead.|
|Appointment management AI agent|Assists in managing appointments for lead records. The agent is capable of creating, updating, or canceling appointments based on the availability of the lead owner.|

## Roles required to create an agentic workflow

The roles required to activate and access the workflow are as follows.

<table id="table_cnc_nyr_dfc"><thead><tr><th>

Roles

</th><th>

Responsibilities

</th></tr></thead><tbody><tr><td>

Sales AI admin

</td><td>

-   Configure the agentic workflow.
-   Change AI settings.
-   Create and manage new workflows and AI agents.

</td></tr><tr><td>

Sales AI user

</td><td>

Interact with AI using the Now Assist panel.

</td></tr></tbody>
</table>## Activating the agentic workflow

Activating duplicated workflow

1.  Navigate to the Help nurture new leads agentic workflow and duplicate it. The workflow also duplicates any triggers associated with that agentic workflow.
2.  Navigate to the duplicated workflow and activate the trigger \(the lead record is created or updated\).

    **Note:** You can activate the triggers associated with the workflow.


Activating external triggers

1.  Navigate to **All** &gt; **System Policy** &gt; **Email** &gt; **Inbound actions**. There are 2 inbound actions that must be activated:
    -   Activate the **Trigger agentic workflow for lead** inbound action.
    -   Activate the **Trigger agentic workflow for lead task** inbound action.
2.  Navigate to the SalesAIAgentsConstants script and change the value of HELP\_NURTURE\_NEW\_LEAD\_FLOW\_ID property to the sys\_id of the duplicated agentic workflow.


Nurturing a lead

To nurture a lead, perform the following steps:

1.  Navigate to **All** &gt; **AI Agent Studio**.
2.  Review the information in the Describe and connect screen, make the necessary updates to ensure that the use case adapts to your requirements, and then select **Save and Continue**.
3.  In the Define trigger screen, activate the triggers that adapt to your requirements, or create your own triggers, and then select **Save and Continue**.
4.  In the Select display screen, perform the following steps:
    1.  Select where you want the use case output to be displayed.
    2.  Use the arrow next to it to add roles that can access the use case.

        **Note:** The sales\_agent is the default role for the use case.

    3.  Select **Save and test**.

The agent executes the testing in AI Agent Studio for the use case.

In the Now Assist panel, the agent receives a notification as soon as the interaction is generated, which enables them to follow the on-screen instructions and complete the task. For more information, see [Request the generative AI capabilities in Customer Service Management by using the Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/request-gen-ai-capabilities-csm-now-assist-panel.md).

**Parent Topic:**[Use agentic workflows in Now Assist for Sales Force Automation \(SFA\)](using-agentic-worklflows-in-lead-management.md)

