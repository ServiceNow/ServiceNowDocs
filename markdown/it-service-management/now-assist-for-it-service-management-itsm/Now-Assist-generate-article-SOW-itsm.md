---
title: Generate a knowledge article from the Service Operations Workspace for ITSM and classic environment by using Now Assist
description: As an agent or knowledge writer, quickly generate knowledge articles from resolved and closed incidents within the Service Operations Workspace for ITSM application and classic environment by using the Now Assist application.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Use generative AI skills, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Generate a knowledge article from the Service Operations Workspace for ITSM and classic environment by using Now Assist

As an agent or knowledge writer, quickly generate knowledge articles from resolved and closed incidents within the Service Operations Workspace for ITSM application and classic environment by using the Now Assist application.

## Before you begin

You can generate a knowledge article in any incident state that is set by your administrator using the **com.snc.incident.create\_knowledge.multistate.enable** system property. The incident must also not have an existing knowledge article that is associated with it.

The Knowledge generation skill is turned on by default. The skill will be automatically available to appropriate role users for the application. When new customers install a Now Assist product, designated skills are turned on automatically. For existing users who upgrade, there will be no change to the skill activation. For more information, see Now Assist skills, agents, and agentic workflows on by default.

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

-   Install the knowledge skills. For more information, see [Configure Now Assist for IT Service Management \(ITSM\)](../../now-assist-itsm/task/configure-now-assist-for-itsm.md).
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

    ![Now assist in knowledge article option in knowledge article option.](../../now-assist-itsm/image/now-assist-itsm-knowledge-option.png)

    **Note:**

    -   The **Create knowledge** UI action is only visible when an incident doesn't have an existing knowledge article that is associated with it.
    -   When the **Create knowledge** action is initiated, it gets redirected to an interceptor page. The Knowledge article interceptor page displays only when the KCS integration for incident management \(com.snc.incident.knowledge\) plugin is not installed. A series of steps is then executed within the Knowledge Management application.

        This includes determining if the following actions must be done:

        -   Display the write option using Now Assist.
        -   Present a list of similar records.
        -   Generate a submission record if the **glide.knowman.submission.workflow** property is enabled.
    -   If you encounter a duplicate **Create Knowledge** button, see the [Resolving duplicate Create Knowledge actions](https://www.servicenow.com/community/itsm-articles/issue-and-resolution-two-quot-create-knowledge-quot-actions-in/ta-p/3418702) community article for the resolution.
4.  In the Knowledge article interceptor page, select a knowledge base and an article template.

    Knowledge article interceptor page for Service Operation Workspace![Knowledge interceptor page in SOW](../../now-assist-itsm/image/now-assist-itsm-kb-interceptor-sow.png)

    Knowledge article interceptor page in Core UI![Knowledge interceptor page in UI16](../../now-assist-itsm/image/now-assist-itsm-kb-interceptor-ui16.png)

5.  Select **Next**.

    **Note:** When you use the standard template, the content from the incident's **Description**, **Resolution**, and **Additional comments** fields are populated in the **Issue**, **Resolution**, and **Additional comments** sections respectively in the article body of the standard template.

    ![Fields populated in the article body of the standard template](../../now-assist-itsm/image/now-assist-itsm-standard-template-art-body1.png)

6.  In the Use AI to draft this article? modal, choose to write the article yourself, or draft an article with Now Assist.

    ![Now Assist ITSM KB generation modal](../../now-assist-itsm/image/now-assist-itsm-kb-gen-modal1.png)

7.  If you’re drafting the article with Now Assist, you can choose up to five relevant tasks for the creation of the article, and select **Use selected tasks to help draft new article**; otherwise, select **Cancel**.

    ![Now Assist in ITSM knowledge article related incidents modal.](../../now-assist-itsm/image/now-assist-itsm-similar-incidents.png)

    When creating an article that includes information that spans multiple similar incidents, a single article is created containing the details from the selected incidents.

    The article appears in a new tab, has a unique ID number for the knowledge article, and is attached to the parent record.

8.  Review the article and edit it if necessary.

    ![Now Assist in ITSM knowledge article.](../../now-assist-itsm/image/now-assist-itsm-kb-gen-art.png)

9.  Select **Save** or **Publish**.

    -   The Now Assist success message disappears indicating that it’s no longer a Now Assist generated article.
    -   If Now LLM Service fails to generate a result, you see an error message.
    -   When creating an article using Now Assist, the process once triggered can’t be stopped. Now Assist continues to generate the article even if you close the dialog box.
    -   **Note:** You can edit a knowledge article in an incident using the **Edit knowledge article** button. This button displays under the following conditions:

-   When the incident is in resolved or closed state or for any state your system administrator has enabled the **com.snc.incident.create\_knowledge.multistate.enable** system property.
-   If you have only one article attached to the incident and you have write access to the article.

**Related topics**  


[bundle-platcap.now-assist-knowledge-management]

