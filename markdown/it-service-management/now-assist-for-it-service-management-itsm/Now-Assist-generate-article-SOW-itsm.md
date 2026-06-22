---
title: Generate a knowledge article from the Service Operations Workspace for ITSM and classic environment by using Now Assist
description: As an agent or knowledge writer, quickly generate knowledge articles from resolved and closed incidents within the Service Operations Workspace for ITSM application and classic environment by using the Now Assist application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/now-assist-for-it-service-management-itsm/Now-Assist-generate-article-SOW-itsm.html
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Use generative AI skills, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Generate a knowledge article from the Service Operations Workspace for ITSM and classic environment by using Now Assist

As an agent or knowledge writer, quickly generate knowledge articles from resolved and closed incidents within the Service Operations Workspace for ITSM application and classic environment by using the Now Assist application.

## Before you begin

You can generate a knowledge article in any incident state that is set by your administrator using the **com.snc.incident.create\_knowledge.multistate.enable** system property. The incident must also not have an existing knowledge article that is associated with it.

The Knowledge generation skill is turned on by default. The skill will be automatically available to appropriate role users for the application. When new customers install a Now Assist product, designated skills are turned on automatically. For existing users who upgrade, there will be no change to the skill activation. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

**Important:**

-   Install the applications and plugins listed in the tables below and update them to the corresponding store app version before configuring the Knowledge Generation skill.
-   For information on the plugin version numbers that correspond to the release you’re installing, see [https://store.servicenow.com/store/app/2c09636e1be06a50a85b16db234bcb74\#versionSummary](https://store.servicenow.com/store/app/2c09636e1be06a50a85b16db234bcb74#versionSummary)

-   For Knowledge Management, you must install and update the following store apps to the corresponding application version.

    |Store application name|Plugin ID|
    |----------------------|---------|
    |Now Assist in Knowledge Management \[app-knowledge-gen-ai\]|sn\_km\_gen\_ai|
    |Knowledge Capabilities in UI Builder \[app-knowledge-uib\]|sn\_km\_uib|

-   For ITSM Service Operations Workspace, you must install and update the following store apps to the corresponding application version.

    |Application name|Plugin ID|
    |----------------|---------|
    |Service Operations Workspace ITSM Applications|sn\_sow\_itsm\_cont|
    |Now Assist for IT Service Management \(ITSM\)|sn\_itsm\_gen\_ai|
    |Service Operations Workspace Core|sn\_sow|
    |Record Page for Service Operations Workspace|sn\_sow\_record|
    |Service Operations Workspace ITSM Common|sn\_sow\_itsm\_common|
    |Incident Management for Service Operations Workspace|sn\_sow\_inc|
    |Interaction Management for Service Operations Workspace|sn\_sow\_interaction|


To enable an agent to see the Now Assist experience on the Create Article page, configure the following knowledge base generation criteria:

-   Install the knowledge skills. For more information, see [Configure Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/configure-now-assist-for-itsm.md).
-   Make sure that the following criteria are in place in the Now Assist Admin console:
    -   Specify the table record and input fields.
    -   Specify the conditions for the skill availability from the list of attributes.
    -   Specify that the knowledge base generation feature for the In-product or Now Assist panel is displayed.
-   Configure the Create Article feature to apply the supported template, Incident-KCS article - HTML, or Standard article.

-   Currently, only the Create Article experience is available.

Role required: itil

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  Open an incident that is assigned to you.

    In the incident record, resolve and close the incident.

3.  Create the article by selecting the **Create knowledge** option from the UI action drop-down menu in the incident.

    \[Omitted image "now-assist-itsm-knowledge-option.png"\] Alt text: Now Assist in ITSM knowledge article option.

    **Note:**

    -   The **Create knowledge** UI action is only visible when an incident doesn't have an existing knowledge article that is associated with it.
    -   When the **Create knowledge** action is initiated, it gets redirected to an interceptor page. The Knowledge article interceptor page displays only when the KCS integration for incident management \(com.snc.incident.knowledge\) plugin is not installed.

        **Important:** If the KCS integration for incident management \(com.snc.incident.knowledge\) plugin is installed, then the interceptor page is skipped.

        A series of steps is then executed within the [Knowledge Management application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/knowledge-management.md).

        This includes determining if the following actions must be done:

        -   Display the write option using Now Assist.
        -   Present a list of similar records.
        -   Generate a submission record if the **glide.knowman.submission.workflow** property is enabled.
    -   If you encounter a duplicate **Create Knowledge** button, see the [Resolving duplicate Create Knowledge actions](https://www.servicenow.com/community/itsm-articles/issue-and-resolution-two-quot-create-knowledge-quot-actions-in/ta-p/3418702) community article for the resolution.
4.  In the Knowledge article interceptor page, select a knowledge base and an article template.

    |Knowledge article interceptor page|UI display|
    |----------------------------------|----------|
    |**In Service Operation Workspace**|\[Omitted image "now-assist-itsm-kb-interceptor-sow.png"\] Alt text: The knowledge article interceptor page in Service Operations Workspace|
    |**In Core UI**|\[Omitted image "now-assist-itsm-kb-interceptor-ui16.png"\] Alt text: The knowledge article interceptor page for core UI.|

5.  Select **Next**.

    **Note:** When you use the standard template, the content from the incident's **Description**, **Resolution**, and **Additional comments** fields are populated in the respective fields in the article body of the standard template.

6.  To add or update the knowledge article, follow the instructions in the table below.

<table><thead><tr><th align="left" id="d317622e525">

To add or update the knowledge article

</th><th align="left" id="d317622e528">

Do this

</th></tr></thead><tbody><tr><td id="d317622e534">

**In Service Operation Workspace**

</td><td>

-   In the main article editor, select the Now Assist icon \[Omitted image "icon-ai-sparkle.png"\] Alt text: Now Assist iconand make changes as needed.

\[Omitted image "now-assist-itsm-sow-create-new-knowledge.png"\] Alt text: Create a KCS article for an incident in SOW-Article body sections populated from fields in the corresponding incident

-   Click **Save**.


</td></tr><tr><td id="d317622e575">

**In Core UI**

</td><td>

You can update the knowledge article manually or use Generative AI to update it.\[Omitted image "now-assist-itsm-coreui-create-new-knowledge.png"\] Alt text: Create a KCS article for an incident in CoreUI

To update it:

-   Manually, select **No, write it myself** and updated the contents in the fields manually.
-   Using Now Assist, select **Yes, draft with Now Assist**. Now Assist adds content to the **Issue** and **Resolution** fields.
-   Select **Submit** after you make the changes.
**Note:** Select **Edit using improved editor**. The new Knowledge Article Advanced Editor page opens in the Knowledge Center where you can edit the content and click **Save** to save the edits.

</td></tr></tbody>
</table>7.  If you’re creating a draft of the article with Now Assist, you can select more than one incident to create the article .

    **Note:** Make sure that AI Search is activated.

    To verify, go to **All** &gt; **AI Search** &gt; **AI Search Status** and verify that AI Search is active.

    \[Omitted image "now-assist-itsm-ai-search.png"\] Alt text: AI Search activated

<table id="choicetable_d3l_scz_23c"><thead><tr><th align="left" id="d317622e673">

Type of UI

</th><th align="left" id="d317622e676">

Procedure

</th></tr></thead><tbody><tr><td id="d317622e682">

**In Service Operation Workspace**

</td><td>

1.  Open an incident.
2.  Select **Create Knowledge**.
3.  Select the Delete icon and select **Clear Canvas**.

The 'Write about \(incident number\)' displays.

4.  Enter an incident number or an incident short description and press the arrow icon\[Omitted image "now-assist-itsm-arrow-icon.png"\] Alt text:.
\[Omitted image "now-assist-itsm-sow-clear-canvas.png"\] Alt text: Clear the canvas to view incidents with similar tasks-   When an incident number is provided, Now Assist generates the article based on the incident number.
-   When an incident short description is copied and pasted, Now Assist searches the top three similar incidents to generate the article.
The Knowledge article is created and attached to all selected similar incidents.

\[Omitted image "now-assist-itsm-sow-similar-inc-knowledge.png"\] Alt text: Knowledge created for similar incidentsSelect **Save** to save the article.

</td></tr><tr><td id="d317622e751">

**In Core UI**

</td><td>

1.  In CoreUI, open an incident with similar incidents.
2.  Select **Create Knowledge**.
3.  Select **Yes, draft with Now Assist**.

A popup displays similar incidents. You can select up to 5 incidents.

4.  Select **Continue without more tasks**.

The knowledge article is created.

5.  Select **Save**.

The knowledge article is attached to all similar incidents.

 \[Omitted image "now-assist-itsm-coreui-multiple-inc-knowledge.png"\] Alt text: Multiple related incidents in CoreUI

</td></tr></tbody>
</table>8.  Review the article and edit it if necessary.

9.  Select **Save** or **Publish**.

    -   The Now Assist success message disappears indicating that it’s no longer a Now Assist generated article.
    -   If Now LLM Service fails to generate a result, you see an error message.
    -   When creating an article using Now Assist, the process once triggered can’t be stopped. Now Assist continues to generate the article even if you close the dialog box.
    -   **Note:** You can edit a knowledge article in an incident using the **Edit knowledge article** button. This button displays under the following conditions:

-   When the incident is in resolved or closed state or for any state your system administrator has enabled the **com.snc.incident.create\_knowledge.multistate.enable** system property.
-   If you have only one article attached to the incident and you have write access to the article.

**Related topics**  


[Now Assist in Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-in-knowledge-management/now-assist-knowledge-management.md)

