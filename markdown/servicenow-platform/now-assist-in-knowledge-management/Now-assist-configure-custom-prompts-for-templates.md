---
title: Configure skills with custom prompts for knowledge article templates
description: ServiceNow Otto in Knowledge Management extends the out-of-box \(OOB\) KB generation skill to create custom prompts for OOB and custom knowledge article templates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/now-assist-in-knowledge-management/Now-assist-configure-custom-prompts-for-templates.html
release: zurich
product: Now Assist in Knowledge Management
classification: now-assist-in-knowledge-management
topic_type: task
last_updated: "2026-07-20"
reading_time_minutes: 3
breadcrumb: [Configure ServiceNow Otto in Knowledge Management, ServiceNow Otto in Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure skills with custom prompts for knowledge article templates

ServiceNow Otto in Knowledge Management extends the out-of-box \(OOB\) KB generation skill to create custom prompts for OOB and custom knowledge article templates.

## Before you begin

In the form configuration of the article record, admin must check for the availability of **Knowledge Gen AI Message** and **Knowledge Modal**. For OOB configurations, they are automatically added to the form view configurator. However, for customized configurations, the admin must add them manually. To do so, navigate to the form layout from the header of the knowledge article \(kb\_knowledge.do\) and add them from **Available** list to the **Selected** list and save. Navigate to Cache \(cache.do\) and clear cache.

Role required: sn\_skill\_builder.admin, sn\_nowassist\_admin.nsa\_admin

## About this task

To create custom prompts for OOB and custom knowledge article templates, copy the existing KB generation skill from the ServiceNow Otto Skill Kit \(NASK\). For more information, see [AI Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skill-kit-landing.md). Configuration happens in three steps:

-   Copy the OOB KB generation skill
-   Prompt configuration
-   Activate the skill

## Procedure

1.  Navigate to **All** &gt; **AI Skill Kit** &gt; **Home**.

2.  In the **ServiceNow skills** tab, search for KB generation skill.

    \[Omitted image "NASK.png"\] Alt text: Select KB generation skill to be copied.

3.  Open the KB generation skill associated with the workflow \(ITSM, CSM, and so on\) that you want to configure.

4.  Select **Clone** to create a copy of the OOB skill.

    **Note:** Prompts can be configured only in the copied skill and not the OOB skill.

5.  In the **Clone skill** window, fill the required fields and select **Clone**.

    \[Omitted image "image.Clone-skill"\] Alt text: Enter the name of the skill and provider details.

6.  On the success message window, select **Open Cloned Skill**.

7.  On the cloned skill page, navigate to the **Prompts** menu and select the **Add** icon.

    \[Omitted image "image.Add-prompt"\] Alt text: Select Add from Prompts menu

8.  In the **Add prompt** table, fill the required fields as follows and select **Add**.

    |Field name|Description|
    |----------|-----------|
    |Prompt name|Enter a name to define your prompt|
    |Provider|Select the third-party AI provider that you want to use|
    |Provider API|Select the API details of the third-party AI provider|

9.  To develop a prompt, see [Guidelines for creating prompts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-in-knowledge-management/guidelines-for-creating-prompts.md).

10. Save the prompt.

11. Evaluate the prompt.

    For more, see [Evaluate a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/evaluate-prompt.md)

12. Select the **Settings** icon to open the **Configurations** settings panel.\[Omitted image "image.Config-settings"\] Alt text: Select configuration settings

13. Scroll down to **Usage conditions** and select the **Add** icon to define the conditions on when to use the prompt based on inputs.

    \[Omitted image "Usage-conditions.png"\] Alt text: Add usage conditions.

14. Fill in the **Key** and **Value** fields to build filters in the **Usage conditions** modal and select **Apply**.

    |Key|Value|
    |---|-----|
    |`prompt_type`|Type single or multi|
    |`source_table`|Type the table name for the configured skill. For example, if you are working on cloned KB Generation skill for CSM then table name should be sn\_customerservice\_case.|
    |`target_table`|Type name of the template table|

15. Select **Finalize prompt**.

    Finalize the prompt after checking the JSON output map with the prompts provided.

16. Repeat the steps 8 to 15 to create prompts for MultiKB articles.

    **Note:** Repeat steps 8 to 15 for each template you want to configure. Finalize the prompts for both single KB and multi-KB articles before publishing the skill.

17. Select **Publish** to publish the prompts for both single KB and multi-KB articles.

    \[Omitted image "Publish-skill.png"\] Alt text: Select finalized prompts to be included in the published skill.

    The skill is published and available in the **AI Admin** page for the selected workflow. Activate the skill to make it available for article generation.

18. To activate the skill, navigate to **AI Admin** and select **Link to NAA** in the **Skill published** window.

19. Select **Activate skill** to activate the copied skill.

    The KB generation skill is activated and ready to use the custom templates defined by the prompt.


-   **[Guidelines for creating prompts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-in-knowledge-management/guidelines-for-creating-prompts.md)**  
Guidelines for writing prompts for out-of-box \(OOB\) and custom knowledge article templates to optimize the use of AI models for generating knowledge articles.

**Parent Topic:**[Configuring ServiceNow Otto in Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-in-knowledge-management/configuring-now-assist-km.md)

