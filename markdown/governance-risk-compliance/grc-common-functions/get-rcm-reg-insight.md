---
title: Analyze and enrich regulatory alerts
description: Analyze and enrich regulatory alerts by using the get regulatory analysis agentic workflow in the Now Assist panel. This agentic workflow uses web search to enhance alert context and recommends potential impacts on citations, policies, and control objectives to support faster and more accurate compliance decisions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/get-rcm-reg-insight.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Now Assist, generative AI]
breadcrumb: [Agentic workflows in Risk &amp; Sustainability, Use agentic AI, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Analyze and enrich regulatory alerts

Analyze and enrich regulatory alerts by using the get regulatory analysis agentic workflow in the Now Assist panel. This agentic workflow uses web search to enhance alert context and recommends potential impacts on citations, policies, and control objectives to support faster and more accurate compliance decisions.

## Before you begin

**Important:** This agentic workflow is turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

Role required: sn\_grc\_comp\_genai.reg\_change\_ai\_agent\_user

The recommendations for regulatory alert skills are required for recommending impact areas. For more information, see [AI-generated recommendations for a regulatory alert skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/recommendations-for-a-regulatory-alert.md).

Agentic workflows and their AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aw.md).

## About this task

The get regulatory analysis agentic workflow helps regulatory change management professionals quickly understand and act on regulatory alerts in the New or In Progress state by enriching them with external context and identifying impacted areas. Using web search, the workflow adds **Enriched Insights** to the alert containing additional information such as summaries, fines, due dates, and source references. It then analyzes the enriched alert to generate recommended impacted areas including citations, policies, controls, and control objectives that appear in the **Recommendations** tab. When you accept these recommendations, they’re automatically added to the impacted areas list.

**Note:**

When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly. To modify this workflow, duplicate it and adjust the settings according to your requirements. You can activate the workflow template by making the triggers active and setting the display settings to include the Now Assist panel. For more information, see [Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md).

## Procedure

1.  Navigate to one of the following locations:

    -   **Workspaces** &gt; **Compliance Workspace**, select the list icon \[Omitted image "ws-list-icon.png"\] Alt text: and then navigate to **Regulatory alerts**.
    -   **Workspaces** &gt; **Compliance Workspace**, select the Regulatory Change Management dashboard icon \[Omitted image "reg-change-icon.png"\] Alt text: and then in the Activity overview, Tracking, or Trends section, select any segment or value in an Alerts related widget to open the list of regulatory alerts with that state.
2.  Select any regulatory alert in the New or In Progress state.

3.  To initiate the get regulatory analysis agentic workflow, select one of the following:

    -   Open the Now Assist panel by selecting the Now Assist icon \[Omitted image "nap-icon.png"\] Alt text: and then select **Get Regulatory Analysis**.
    -   Select **Ask NowAssist** and then **Get analysis**.
    The Now Assist panel icon is available to select anywhere in the Compliance Workspace and the **Ask NowAssist** action menu is available when you're on a regulatory alert page.

    Here is an example of how this workflow appears when you initiate it.

    \[Omitted image "get-regulatory-analysis.png"\] Alt text: Details of initiating the get regulatory alerts workflow in the Now Assist panel.

4.  Analyze and enrich regulatory alerts by adding enriched insights or generating recommended impacted areas.

<table id="choicetable_hf2_xq3_zgc"><thead><tr><th align="left" id="d395016e255">

Option

</th><th align="left" id="d395016e258">

Description

</th></tr></thead><tbody><tr><td id="d395016e264">

**Add enriched insights**

</td><td>

In the Now Assist panel, ask the agent to enrich a regulatory alert with web sources to get a comprehensive overview by entering `1`.\[Omitted image "get-regulatory-analysis-2.png"\] Alt text: Details of agent enriching a regulatory alert in the Now Assist panel.

**Note:**

-   If you aren’t making this request from a regulatory alert page using the action menu, be prepared to provide the regulatory alert number \(sys\_id\) so that the workflow has the context it needs to fulfill your request. The workflow generates a summary including information on any fines, penalties, important dates, taxonomy, as well as a list of sources for the information.
-   You can save the overview to the Enriched Insights field on the details page of the regulatory alert.
-   You can discard the overview and create your own summary manually.


</td></tr><tr><td id="d395016e302">

**Recommend impacted areas**

</td><td>

In the Now Assist panel, ask the agent to check for recommended impacted areas for a regulatory alert by entering `2`.\[Omitted image "get-regulatory-analysis-3.png"\] Alt text: Details of agent recommending impacted areas in the Now Assist panel.

**Note:**

-   If you aren’t making this request from a regulatory alert page using the action menu, be prepared to provide the regulatory alert number \(sys\_id\) so that the workflow has the context it needs to fulfill your request. The workflow analyzes the alert and generates a categorized list for each type of impacted area such as citation, control objective, controls, or policies.
-   You can review all potential impacted areas and add them to the regulatory alert by navigating to the **Recommendations** tab. For more information on acting on recommendations and adding impacted areas, see [Accept or dismiss recommendations for regulatory alert impacted citations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/manage-recommendation-reg-alert.md), [Accept or dismiss recommendations for regulatory alert impacted control objectives](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/manage-recommend-co-reg-alert.md), [Accept or dismiss recommendations for regulatory alert impacted controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/manage-recos-for-controls.md), [Accept or dismiss recommendations for regulatory alert impacted policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/manage-recos-for-policies.md), and [Add impacted areas manually to a regulatory alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/add-impacted-area-reg-alert.md).


</td></tr></tbody>
</table>    In the Now Assist panel, the agent receives a notification when the interaction is generated, enabling your users to follow the on-screen instructions and complete the task.

    **Important:** Be sure to check AI-generated summaries and recommendations for accuracy. If no information is available, the generated recommendations display "No recommendations available," "None," "No records to display," and so on.


**Related topics**  


[Using agentic workflows in IRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/using-agentic-ai-workflows.md)

[Activate the get regulatory analysis agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/activate-rcm-agent-workflow.md)

[Accept or dismiss recommendations for regulatory alert impacted citations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/manage-recommendation-reg-alert.md)

[Accept or dismiss recommendations for regulatory alert impacted control objectives](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/manage-recommend-co-reg-alert.md)

[Accept or dismiss recommendations for regulatory alert impacted controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/manage-recos-for-controls.md)

[Add impacted areas manually to a regulatory alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/add-impacted-area-reg-alert.md)

