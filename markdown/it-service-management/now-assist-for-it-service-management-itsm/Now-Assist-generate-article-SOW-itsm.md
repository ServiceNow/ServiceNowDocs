---
title: Generate a knowledge article from the Service Operations Workspace for ITSM and classic environment by using Now Assist
description: As an agent or knowledge writer, quickly generate knowledge articles from resolved and closed incidents within the Service Operations Workspace for ITSM application and classic environment by using the Now Assist application.
locale: en-US
release: xanadu
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Use, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Generate a knowledge article from the Service Operations Workspace for ITSM and classic environment by using Now Assist

As an agent or knowledge writer, quickly generate knowledge articles from resolved and closed incidents within the Service Operations Workspace for ITSM application and classic environment by using the Now Assist application.

## Before you begin

Generate a KB article from similar incidents by using Now Assist 

To generate a knowledge article for an incident, the incident must be in the resolved or closed state, and not have an existing knowledge article that is associated with it.

**Important:**

-   Install the applications and plugins listed in the tables below and update them to the corresponding store app version before configuring the Knowledge Generation skill.
-   For information on the plugin version numbers that correspond to the release you are installing, see [https://store.servicenow.com/store/app/2c09636e1be06a50a85b16db234bcb74\#versionSummary](https://store.servicenow.com/store/app/2c09636e1be06a50a85b16db234bcb74#versionSummary)

-   For knowledge management, you must install and update the following store apps to the corresponding application version.

    |Store application name|Plugin ID|
    |----------------------|---------|
    |Now Assist in Knowledge Management \[app-knowledge-gen-ai\]|com.sn.km.gen.ai, sn\_km\_gen\_ai|
    |Knowledge Capabilities in UI Builder \[app-knowledge-uib\]|com.snc.uib.knowledge, sn\_km\_uib|

-   For ITSM Service Operations Workspace,you must install and update the following store apps to the corresponding application version.

    |Application name|Plugin ID|
    |----------------|---------|
    |Service Operations Workspace ITSM Applications|sn\_sow\_itsm\_cont|
    |Now Assist for IT Service Management \(ITSM\)|sn\_itsm\_gen\_ai|
    |Service Operations Workspace Core|sn\_sow|
    |Record Page for Service Operations Workspace|sn\_sow\_record|
    |Service Operations Workspace ITSM Common|sn\_sow\_itsm\_common|
    |Incident Management for Service Operations Workspace|sn\_sow\_inc|
    |Interaction Management for Service Operations Workspace|sn\_sow\_interaction|

-   To use the Knowledge Centered Services \(KCS\) template \(Incident-KCS article - HTML\) in the Service Operations Workspace ITSM application, you must install the KCS Integration for Incident Management plugin. Otherwise, Now Assist uses the Standard article.

To enable an agent to see the Now Assist experience on the Create Article page, configure the following knowledge base generation criteria:

-   Install the knowledge skills. For more information, see [Configure Now Assist for IT Service Management \(ITSM\)](../../now-assist-itsm/task/configure-now-assist-for-itsm.md).
-   Make sure that the following criteria are in place in the Now Assist Admin console:
    -   Specify the table record and input fields.
    -   Specify the conditions for the skill availability from the list of attributes.
    -   Specify that the knowledge base generation feature for the In-product or Now Assist panel is displayed.
-   Configure the Create Article feature to apply the supported template, Incident-KCS article - HTML, or Standard article.

-   Currently, only the Create Article experience is available.

Role required: itil

## About this task

In the Service Operations Workspace for ITSM and classic environment, you can generate the knowledge article information for an incident by selecting **Create Knowledge** on the incident record. This UI action displays the Use Al to draft this article modal. By using this modal, you can choose to write the article yourself or draft an article and then you can review and edit the knowledge article text.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  Open an incident that is assigned to you.

    In the incident record, resolve and close the incident.

3.  Create the article by selecting the **Create knowledge** option from the UI action drop-down menu in the incident.

    ![Now Assist in ITSM knowledge article option.](../../now-assist-itsm/image/now-assist-itsm-knowledge-option.png)

    **Note:** The Create knowledge UI action is only visible when an incident doesn't have an existing knowledge article that is associated with it.

4.  In the Create article modal, select a Knowledge Base and an Article template, if displayed.

    **Note:** Using the templates to create the articles is optional. Your system administrator must enable the **sn\_sow\_inc.enable\_kb\_template** system property and you must have at least one active template to see the modal. For information on available templates, see [Knowledge article templates](https://www.servicenow.com/docs/access?context=knowledge-article-templates&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

    The KCS template \(Incident-KCS article - HTML\) is used to generate the article only if the KCS plugin is installed. If the plugin isn’t installed, the article is generated by using the Standard article.

    ![Now Assist in ITSM create article modal](../../now-assist-itsm/image/itsm-now-assist-create-article-modal.png)

    The Knowledge Base is selected based on your administrator's configuration in the Now Assist Admin console.

5.  Select **Create article**.

6.  In the Use AI to draft this article? modal, choose to write the article yourself, or draft an article with Now Assist.

    ![Now Assist in ITSM knowledge article choice modal.](../../now-assist-itsm/image/now-assist-itsm-kb-gen-modal.png)

7.  If you are drafting the article with Now Assist, you can choose up to five relevant tasks for the creation of the article, and select **Use selected tasks to help draft new article**; otherwise, select **Cancel**.

    ![Now Assist in ITSM knowledge article related incidents modal.](../../now-assist-itsm/image/now-assist-itsm-similar-incidents.png)

    When creating an article that includes information that spans multiple similar incidents, a single article is created containing the details from the selected incidents.

    **Note:**

    If no similar tasks exist, this modal won’t appear, and the article is created. The generated article, based on the chosen relevant records, is linked to both the parent task and all the relevant cases selected.

    The article appears in a new tab, has a unique ID number for the knowledge article, and is attached to the parent record.

8.  Review the article and edit it if necessary.

    ![Now Assist in ITSM knowledge article.](../../now-assist-itsm/image/now-assist-itsm-kb-gen-art.png)

9.  Select **Save** or **Publish**.

    The Now Assist success message disappears indicating that it’s no longer a Now Assist generated article.

    If Now LLM Service fails to generate a result, you see an error message.

    When creating an article using Now Assist, the process once triggered can’t be stopped. Now Assist continues to generate the article even if you close the dialog box.


**Parent Topic:**[Using Now Assist for IT Service Management \(ITSM\)](../../now-assist-itsm/concept/using-now-assist-for-itsm.md)

**Related topics**  


[Now Assist in Knowledge Management](https://www.servicenow.com/docs/access?context=now-assist-knowledge-management&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

