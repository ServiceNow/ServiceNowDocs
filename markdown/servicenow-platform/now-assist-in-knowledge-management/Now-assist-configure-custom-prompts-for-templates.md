---
title: Configure skills with custom prompts for knowledge article templates
description: Now Assist in Knowledge Management has extended the out-of-box \(OOB\) KB generation skill to create custom prompts for OOB and custom knowledge article templates.
locale: en-US
release: australia
product: Now Assist in Knowledge Management
classification: now-assist-in-knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure Now Assist in Knowledge Management, Now Assist in Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure skills with custom prompts for knowledge article templates

Now Assist in Knowledge Management has extended the out-of-box \(OOB\) KB generation skill to create custom prompts for OOB and custom knowledge article templates.

## Before you begin

In the form configuration of the article record, admin must check for the availability of **Knowledge Gen AI Message** and **Knowledge Now Assist Modal**. For OOB configurations, they are automatically added to the form view configurator. However, for customized configurations, the admin must add them manually. To do so, navigate to the form layout from the header of the knowledge article \(kb\_knowledge.do\) and add them from **Available** list to the **Selected** list and save. Navigate to Cache \(cache.do\) and clear cache.

![Configuring knowledge form.](../image/Configuring-knowledge-form.png)

Role required: sn\_skill\_builder.admin, sn\_nowassist\_admin.nsa\_admin

## About this task

To create custom prompts for OOB and custom knowledge article templates, clone the existing KB generation skill, from the Now Assist skill Kit \(NASK\). For more information, see [Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=now-assist-skill-kit-landing&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) Configuration of the skill happens in three steps:

-   Clone the OOB KB generation skill
-   Prompt configuration
-   Activate the skill

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.

2.  In the **ServiceNow skills** tab, search for KB generation skill.

    ![Select KB generation skill to be cloned.](../image/NASK.png)

3.  Open the KB generation skill associated with the workflow \(ITSM, CSM, and so on\) that you want to configure.

4.  Select **Clone** to create a clone of the OOB skill.

    **Important:** Prompts can be configured only in the cloned skill and not the OOB skill.

5.  In the **Clone skill** window, fill the required fields and select **Clone**.

    ![Enter the name of the skill and provider details.](../image/Clone-skill.png)

6.  On the success message window, select **Open Cloned Skill**.

    ![Select Open cloned skill](../image/Cloned-success.png)

7.  On the cloned skill page, navigate to the **Prompts** menu and select the **Add** icon.

    ![Select Add from Prompts menu](../image/Add-prompt.png)

8.  In the **Add prompt** table, fill the required fields as follows and select **Add**.

    |Field name|Description|
    |----------|-----------|
    |Prompt name|Enter a name to define your prompt|
    |Provider|Select the third-party AI provider that you want to use|
    |Provider API|Select the API details of the third-party AI provider|

9.  To develop a prompt, see [Guidelines for creating prompts](../concept/guidelines-for-creating-prompts.md).

10. Save the prompt.

11. Evaluate the prompt.

    For more, see [Evaluate a prompt](https://www.servicenow.com/docs/access?context=evaluate-prompt&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

12. Select the **Settings** icon to open the **Configurations** settings panel.![Select configuration settings](../image/Config-settings.png)

13. Scroll down to **Usage conditions** and select the **Add** icon to define the conditions on when to use the prompt based on inputs.

    ![Add usage conditions.](../image/Usage-conditions.png)

14. Fill in the **Key** and **Value** fields to build filters in the **Usage conditions** modal and select **Apply**.

    |Key|Value|
    |---|-----|
    |`prompt_type`|Type single or multi|
    |`source_table`|Type the table name for the configured skill. For example, if you are working on cloned KB Generation skill for CSM then table name should be sn\_customerservice\_case.|
    |`target_table`|Type name of the template table|

15. Select **Finalize prompt**.

    Finalize the prompt after checking the JSON output map with the prompts provided.

16. Repeat the steps 8 to 15 to create prompts for MultiKB articles.

    **Note:**

    Finalize the prompts for both single KB and multi KB articles and only then publish the skill.

17. Select **Publish** to publish the prompts for both single KB and multi-KB articles.

    ![Select finalized prompts to be included in the published skill.](../image/Publish-skill.png)

    The skill is published and available in the **Now Assist Admin** page for the selected workflow. However, the skill must be activated to be available for use during article generation from Now Assist.

18. To activate the skill, navigate to **Now Assist Admin** and select **Link to NAA** in the **Skill published** window.

19. Select **Activate skill** to activate the cloned skill.

    ![Activate the KB generation skill.](../image/Activate-skill.png)

    The KB generation skill for Now Assist is activated and ready to use the custom templates as defined by the prompt.


-   **[Guidelines for creating prompts](../concept/guidelines-for-creating-prompts.md)**  
The guidelines help to write prompts for Out-of-Box \(OOB\) and custom knowledge article templates. Follow these instructions to create ideal prompts that optimize the use of AI models for generating knowledge articles.

**Parent Topic:**[Configuring Now Assist in Knowledge Management](../concept/configuring-now-assist-km.md)

