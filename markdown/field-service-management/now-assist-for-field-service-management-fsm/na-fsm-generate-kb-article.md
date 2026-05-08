---
title: Generate a knowledge article from the CSM/FSM Configurable Workspace and classic environment with Now Assist
description: As an agent, generate knowledge articles for closed work order tasks within the CSM/FSM Configurable Workspace and classic environment with Now Assist.
locale: en-US
release: australia
product: Now Assist for Field Service Management \(FSM\)
classification: now-assist-for-field-service-management-fsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use generative AI skills, Now Assist for FSM]
---

# Generate a knowledge article from the CSM/FSM Configurable Workspace and classic environment with Now Assist

As an agent, generate knowledge articles for closed work order tasks within the CSM/FSM Configurable Workspace and classic environment with Now Assist.

## Before you begin

To generate a knowledge article for a work order task, the work order task must be in a closed complete or closed incomplete state. Additionally, the work order task must not already have a knowledge article linked to it.

The following system property configurations are required so that agents can use the Knowledge Centered Service \(KCS\) template when generating knowledge articles.

-   Install the Knowledge Management Advanced plugin. For details, see Activate the Knowledge Management Advanced plugin.
-   Enable Knowledge Centered Services \(KCS\) for FSM by setting the system property **sn\_fsm.enable\_knowledge\_kcs** to true. Otherwise, Now Assist uses the standard template.

To enable an agent to see the Now Assist experience on the Create Article page, ensure that the following knowledge base generation criteria is configured:

-   The Customer workflow, FSM, and Platform workflow knowledge skills are activated.
-   In the Now Assist Admin console, ensure that the following criteria are in place:
    -   The table record and input fields must be specified.
    -   Conditions for the skill availability must be specified from the list of attributes.
    -   Display of the knowledge base generation feature In-product and the Now Assist panel must be specified.
-   **Create Article** must be configured to apply the supported template; For example, Standard and KCS article HTML.

-   Currently, only the **Create Article** experience is available.

Role required: wm\_dispatcher, wm\_manager

## About this task

In the FSM Configurable Workspace and classic environment, you can generate the knowledge article information for a work order task by selecting **Create Knowledge** on the work order task record. This UI action displays the Use Al to draft this article modal. By using this modal, you can choose to write the article yourself or draft an article with Now Assist and review and edit the knowledge article text.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Open a work order task that is assigned to you.

    The work order task record state should be Closed.

3.  Create the article by selecting **Create Knowledge** from the UI actions for the work order task record.

    **Note:**

    The **Create Knowledge** UI action is only visible when a work order task doesn't have an existing knowledge article associated with it.

4.  In the Create article modal, select a knowledge base and an Article template, if displayed.

    **Note:** If no options are displayed, the default template selected by your administrator in the Now Assist Admin console is used.

5.  Select **Create Article**.

6.  In the Use Al to draft this article modal, select **Yes, draft with Now Assist**.

    **Note:** When creating an article using Now Assist, once the process is triggered, it can't be stopped. Now Assist continues to generate the article even if you close the modal.

7.  From the Select options modal, select the **Knowledge base** in which you would like to publish the article and, the **Article language** to be used to generate the article.

    **Note:** For more information on language selection, see Generate a Knowledge article using multi-language support.

8.  Select **Continue**.

9.  Choose up to five relevant work order tasks in the new modal to generate the article and select **Continue with the selected tasks**, otherwise select **Cancel**.

    **Note:** If no similar work order tasks exist, this modal will not appear, and the article will be created. The generated article, based on the chosen relevant records, will be linked to both the account work order task and all the relevant work order tasks selected.

    1.  Once the article appears in a new tab with a unique ID number for the knowledge article, you can click the sparkle icon to **Elaborate** or **Shorten** the selected text.

    2.  Select **Insert** to include the modified text, or manually update the text.

10. Review the Now Assist generated article and select **Submit** or **Publish**.

    The Now Assist success message disappears indicating that it is no longer a Now LLM Service generated article.


**Parent Topic:**[Using Now Assist for Field Service Management \(FSM\)](../concept/using-now-assist-fsm.md)

