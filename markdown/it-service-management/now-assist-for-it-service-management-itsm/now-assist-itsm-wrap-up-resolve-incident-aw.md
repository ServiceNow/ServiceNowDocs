---
title: ITSM Wrap-up and resolve incident agentic workflow
description: Use the Wrap-up and resolve incident agentic workflow to generate resolution notes and select resolution code to resolve an incident. Attach the Knowledge Base \(KB\) article or create a draft Knowledge article. Attach a Known Error \(KE\) article to the incident record when the resolution code is selected as Known Error. Update duplicate incident information when the resolution code is Duplicate.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-wrap-up-resolve-incident-aw.html
release: zurich
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Now Assist, agentic AI, generative AI, Gen AI]
breadcrumb: [Agentic AI in the Incident Management application, Use agentic AI in IT Service Management, ServiceNow Otto for IT Service Management \(ITSM\), IT Service Management]
---

# ITSM Wrap-up and resolve incident agentic workflow

Use the Wrap-up and resolve incident agentic workflow to generate resolution notes and select resolution code to resolve an incident. Attach the Knowledge Base \(KB\) article or create a draft Knowledge article. Attach a Known Error \(KE\) article to the incident record when the resolution code is selected as Known Error. Update duplicate incident information when the resolution code is Duplicate.

## Wrap-up and resolve incident agentic workflow overview

Using the Wrap-up and resolve incident agentic workflow:

1.  Generate resolution notes \(root cause and resolution steps\) based on the work notes and comments in the activity stream of the incident record and select a resolution code.
2.  Update duplicate incident information to the incident record when the resolution code is Duplicate.
3.  Check for relevant available KE articles and attach any of them to the incident record when the resolution code is Known Error.
4.  Check for relevant available KB articles and attach any of them to the incident record.
5.  Create a draft KB and attach it to the incident record if necessary.

To modify the Wrap-up and resolve incident agentic workflow, [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements.

**Important:** When you modify an agentic workflow, AI agent, or a tool, make sure that you update all instructions accordingly.

## Resolve incidents and link a KB or KE article

When you make a query or a request in the  ServiceNow Otto panel,  resolution notes are generated based on the work notes and the comments from the activity stream of the incident record. You can select any resolution code from the available resolution codes. You can update the duplicate incident information to the incident record if the resolution code is selected as Duplicate.

You can also attach any of the KE articles from the similar KE article recommendations to the incident record if the resolution code is selected as Known Error and then resolve the incident. After the incident is resolved, you can attach any of the KB articles from the similar recommended KB articles to the incident record. You can also select to create a draft KB article.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Wrap up and resolve incident**.

## AI agents used in the Wrap-up and resolve incident agentic workflow

In the Wrap-up and resolve  incident agentic workflow, specific AI agents are used for each type of resolution to generate the desired recommendations and output.

**Important:** In the Define availability screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

<table id="table_bh5_mbv_jgc"><thead><tr><th>

AI Agent

</th><th>

AI Agent role

</th></tr></thead><tbody><tr><td>

Incident resolution details AI agent

</td><td>

1.  Generates and recommends resolution notes based on the work notes and comments in the activity stream. After you approve, the resolution notes are added to the incident record.
2.  Provides the available resolution codes to select. After selection, the codes are added to the incident record.
3.  Updates duplicate incident information to the incident record if the selected resolution code is Duplicate.

</td></tr><tr><td>

Incident knowledge article AI agent

</td><td>

1.  Resolves the incident and then searches and recommends similar KB articles. You can select any of the recommended KB articles or enter any KB article irrespective of any similar KB articles found which are then attached to the incident record.
2.  If no similar KB articles are available or you don’t want to select from the available similar KB articles, you can still choose to create a draft KB article anyway. You can provide the input as Draft in the ServiceNow Otto panel. In such a case, the AI agent drafts and recommends a KB article that you can link to the incident record.

</td></tr><tr><td>

Incident known error article AI agent

</td><td>

Searches for and recommends similar KE articles if the resolution code is Known Error. You can select any of the recommended KE articles that are then attached to the incident record and the incident is resolved. If no relevant KE articles are available, you can enter any KE article, which is then attached to the incident record.

</td></tr></tbody>
</table>## Set up the Wrap-up and resolve incident agentic workflow

To use the Wrap-up and resolve incident agentic workflow, you must confirm or perform the following:

1.  The ServiceNow Otto for IT Service Management \(ITSM\) plugin \(sn\_itsm\_gen\_ai\) plugin is installed and configured.
2.  Navigate to **All** &gt; **AI Admin Hub** &gt; **AI Skills** and enable the following skills and options:

    1.  On the **AI Skills** tab, select **ITSM** and then activate the Resolution notes generation and KB generation skill. For more information, see [Skill inputs and triggers for ServiceNow Otto for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-skills.md).
    2.  On the **AI Experience** tab, enable the ServiceNow Otto panel for users.
    3.  Select the **CI Admin console** link, and then enable the ServiceNow Otto panel.
    For more information, see [Configure ServiceNow Otto for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/now-assist-for-it-service-management-itsm/configure-now-assist-for-itsm.md).


## Use the Wrap-up and resolve incident agentic workflow

In the agentic workflow record:

1.  Review the information in the Define key requirements screen \(workflow description and list of steps field\) and in the Add a preferred trigger screen, make any necessary updates, and then select  **Save and Continue**.

    **Note:** You can only edit the information in this record in the IT Service Management AI agent collection application scope.

2.  In the Select a UI display screen:

    1.  Select **ServiceNow Otto panel** where you want the agentic workflow output to be displayed.

        **Note:** When selected, the ServiceNow Otto panel icon can be accessed from the menu bar.

    2.  Use the arrow next to it to add roles that can access the agentic workflow.

        **Note:** The itil role is added by default. Any role that you add in this field can use the Wrap-up and resolve incident agentic workflow. For example, from the ServiceNow Otto panel.

    3.  Select  **Save and test**.
    The agent executes the request for the agentic workflow.

    **Example of the Wrap-up and resolve incident agentic workflow output in the ServiceNow AI Agent Studio**\[Omitted image "now-assist-itsm-wrap-up-resolve-incident-agent-studio.png"\] Alt text: Wrap-up and resolve incident agentic workflow output in AI Agent Studio.

3.  Access and use the Wrap-up and resolve incident agentic workflow from the ServiceNow Otto panel.

    You can query in the ServiceNow Otto panel to use the agentic workflow. For the query instruction, follow the steps specified in the **List of steps** field of the Define key requirements screen in the agentic workflow record.

    **Example of the Wrap-up and resolve incident output in the ServiceNow Otto Panel**

    \[Omitted image "now-assist-itsm-wrap-up-resolve-incident-nap.png"\] Alt text: Wrap-up and resolve incident agentic workflow resolution notes generation output in the ServiceNow Otto panel.\[Omitted image "now-assist-itsm-wrap-up-resolve-incident-nap-rc.png"\] Alt text: Wrap-up and resolve incident agentic workflow resolution code selection output in ServiceNow Otto panel.


Based on the query, the different AI agents work on the incident record. Depending on the various workflow stages and the resolution codes selected for an incident, the AI agents can either operate individually in sequence or collaborate simultaneously to deliver the desired outcome.

For example, when generating resolution notes, adding resolution notes and codes or updating duplicate incident information to the incident record, the Incident resolution details AI agent is used. For more information on how to query using the ServiceNow Otto panel, see [Request the generative AI capabilities in ITSM by using the ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/now-assist-for-it-service-management-itsm/request-gen-ai-capabilities-itsm-now-assist-panel.md).

**Parent Topic:**[Agentic AI ServiceNow Otto for Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/now-assist-for-it-service-management-itsm/using-agentic-ai-workflow-im.md)

