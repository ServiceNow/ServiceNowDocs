---
title: IT Service Management AI agent collection Generate post incident reviews agentic workflow
description: Use the Post-incident review AI agent to generate a review report after a major incident is resolved. You can review and revise this report if necessary.
locale: en-US
release: zurich
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Agentic AI in the ITSM application, Use agentic AI in IT Service Management, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# IT Service Management AI agent collection Generate post incident reviews agentic workflow

Use the Post-incident review AI agent to generate a review report after a major incident is resolved. You can review and revise this report if necessary.

## Generate post incident reviews agentic workflow overview

Using the Generate post incident reviews agentic workflow, generate reports after an incident is resolved. The report includes the following sections:

-   Executive Summary
-   Customer/Service Impact
-   Detailed Technical Summary
-   Action Items &amp; Prevention

The time taken to create the report after the incident is resolved may be reduced, and the business impact may be minimized when responses to major incidents are both effective and efficient. For information on how major incidents are created, see [Major Incident Management process](../../incident-management/concept/major-incident-management-process.md).

To modify the Generate post incident reviews agentic workflow, [duplicate it](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US), and adjust the settings according to your requirements.

**Important:** When you modify a use case, AI agent, or tool, make sure that you update all instructions accordingly.

## Generate post incident reviews agentic workflow

Autonomously generate a report for the fulfiller once a major incident has been closed.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Post-incident reviews**.

**Important:** In the Edit trigger form, make sure that the **Active** button is turned on to enable the AI agent to trigger autonomously.

**Important:** To enable the display of the Generate post incident reviews agentic workflow, you must activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\). For more information, see [Activate Incident Management - Major Incident Management](../../incident-management/task/activate-major-incident-management-plugin.md).

## AI agents used in the Generate post incident reviews agentic workflow

The Post-incident review AI agent is used to fetch incident details, related records, and the post incident summary.

**Important:** In the Define availability screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

## Generating the report

In the agentic workflow record:

1.  Review the information in the Describe and connect screen and in the Define trigger screen, make the necessary updates, and then select **Save and Continue**.
2.  In the Select display screen:

    1.  Choose where you want the agentic workflow output to be displayed.
    2.  Use the arrow next to it to add roles that can access the agentic workflow.

        **Note:** The itil role is added by default.

    3.  Select **Save and test**.

        The agent executes the request for the agentic workflow.

    **Example of a Generate post incident reviews agentic workflow report in the ServiceNow AI Agent Studio** ![Generate post incident reviews agentic workflow output.](../image/now-assist-itsm-aiagents-mim-nap.png)


In the AI Agent Studio, the fulfiller receives a notification as soon as the report is generated, enabling them to follow the on-screen instructions and complete the task. For more information, see [Request the generative AI capabilities in ITSM by using the Now Assist panel](../task/request-gen-ai-capabilities-itsm-now-assist-panel.md).

## Generating the Post Incident Reviews workflow in the Now Assist panel

As a user, do the following in the Now Assist panel:

**Note:** When the **Assigned to** field is populated and the major incident is moved to the resolved state, then the workflow gets triggered through the Now Assist panel.

1.  To trigger the workflow manually, open the Now Assist panel and enter the major incident number for which you want to generate the post incident review.

    The Post-incident review AI agent validates that the incident is a major incident and that it is in resolved state. If the validation fails, the workflow requests a valid major incident number.

2.  The Post-incident review AI agent retrieves the following information from the incident:
    -   Short description and detailed description
    -   Assignment group and assigned to user
    -   Category and subcategory
    -   Service and configuration item
    -   Resolution notes and business impact
    -   Activity logs and work notes
3.  The AI agent collects the following related records:
    -   Child incident details
    -   Associated problems
    -   Change requests and caused-by change requests
    -   Incident tasks
4.  The AI agent generates the Post Incident review report that includes the following four sections:
    -   **Executive Summary:** This includes the non-technical overview such as the nature of the incident, duration, affected users, and the key highlights.
    -   **Customer / Service Impact:** This includes the scope of the impact, affected regions and services, and impact to the service availability.
    -   **Detailed Technical Summary:** This includes the technical description of failures, environmental context, root cause analysis, and the timeline of events.
    -   **Action Items &amp; Prevention:** This includes the completed and outstanding action items, root cause explanation, remediation steps, preventive measures.
5.  The AI agent displays the complete Post Incident Review report to the user and request feedback.
6.  The user provides the feedback by either approving the report or asking for revisions such as requesting for more concise, more detailed information or requests specific modifications.

<table id="table_zd4_fzg_m3c"><thead><tr><th>

If

</th><th>

Then, the AI agent

</th></tr></thead><tbody><tr><td>

The user approves the request

</td><td>

1.  Verifies that the report has write access permissions.
2.  Updates **Post Incident Report** field in the major incident record. This information is updated in the major incident record in the Core UI and also in Service Operations Workspace.
3.  When the user confirms that there is no additional feedback, the AI agent concludes the workflow.


</td></tr><tr><td>

If the user requests changes to the report

</td><td>

1.  Revises the report based on the feedback.
2.  Displays the updated report.
3.  Requests feedback again.
4.  Repeats the process until the user approves it.


</td></tr></tbody>
</table>
Post Incident Review report in Core UI ![Post Incident Workflow in Now Assist panel for Core UI](../image/now-assist-itsm-post-incident-flow-ui16.png)

Post Incident review report in Service Operations Workspace![Post Incident Workflow in Now Assist panel in Service Operations Workspace](../image/now-assist-itsm-post-incident-flow-sow.png)

