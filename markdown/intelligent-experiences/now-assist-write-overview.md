---
title: Now Assist context menu
description: The Now Assist context menu uses generative AI to help agents summarize, create, and edit written content, thus streamlining their writing tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-write-overview.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Now Assist, Now Assist context menu, Generative AI, Gen AI, Streamline]
breadcrumb: [Now Assist Experiences, Exploring Now Assist Admin, Now Assist, Enable AI experiences]
---

# Now Assist context menu

The Now Assist context menu uses generative AI to help agents summarize, create, and edit written content, thus streamlining their writing tasks.

Agents produce various types of content, including emails and chat replies. The Now Assist context menu uses generative AI to assist agents in summarizing, creating, and editing emails and chat replies. Agents can preview AI generated content, scroll through previously created content, and refine the text using the AI. The Now Assist context menu can be triggered from any application or field in a ServiceNow workspace where the Now Assist context menu is enabled.

The Now Assist context menu unlocks the power of generative AI and is available in Next Experience for:

-   Customer Service Management \(CSM\)
-   Human Resources \(HR\)
-   IT Service Management \(ITSM\)
-   Strategic Portfolio Management \(SPM\)
-   IT Operations Management \(ITOM\)

The Now Assist context menu isn’t available with Core UI.

## Using the Now Assist context menu

The Now Assist context menu is available on any field where the floating Now Assist button \(\[Omitted image "wwna-icon.png"\] Alt text: Now Assist context menu icon\) appears. If you start typing in the field, a menu appears with the available Now Assist context menu actions. The Now Assist context menu helps you summarize, create or modify existing documentation.

You can configure the Advanced filter to hide or show the Now Assist Context Menu quick actions option using the wwna\_quick\_actions table. To view more variable set configuration options, see [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/nacm-variable-set-description.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/nacm-variable-set-description.md).

-   **Chat window using the Now Assist context menu**

    You can use the Now Assist context menu when communicating with users in Agent Chat:

    If it takes too long to generate text or the Now LLM Service isn't available, an error message appears.

    \[Omitted image "wwna-agent-chat-window.png"\] Alt text: Agent Chat window with the Now Assist context menu icon

-   **Change request risk explanation using the Now Assist context menu**

    The Now Assist context menu makes the change request risk explanation available on the workspace and on UI16 after assessment and calculation.

    When the risk is assessed and calculated, you’ll see the **Explain risk** button with the Now Assist \[Omitted image "wwna-icon.png"\] Alt text: The Now Assist icon. icon on the workspace showing the risk explanation in a dialogue box in the Record information section.

    \[Omitted image "change-risk-explntn-wrkspc-nacm.png"\] Alt text: The change request risk explanation powered by Now Assist.

    When the risk is assessed and calculated, you’ll see the Now Assist \[Omitted image "wwna-icon.png"\] Alt text: The Now Assist icon. icon against the **Risk** field on UI16, showing the risk explanation in a dialogue box.

    \[Omitted image "change-risk-explntn-nacm.png"\] Alt text: Now Assist showing the change risk explanation.

    **Note:** The risk explanation that is presented in the dialogue box is assessed and calculated on the change request form.

    For more information about risk assessment and calculation, see .

-   **Content editing in Knowledge Base articles using the Now Assist content menu**

    The Now Assist context menu enables generative AI assisted content editing capabilities for Knowledge Base authoring and to provide resolution notes in workspaces and UI16.

    When you open a knowledge article and select the content in it, you’ll see the Now Assist \[Omitted image "wwna-icon.png"\] Alt text: The Now Assist icon. icon pop-up and float along with your mouse device.

    When you hover over the Now Assist icon, you’ll see the following menu options to help you edit the content:

    -   **Elaborate**: Generative AI details the selected text.
    -   **Shorten**: Generative AI shortens the selected text.
    \[Omitted image "now-assist-context-menu.png"\] Alt text: Now Assist context menu options for the selected text.

    You can insert the generative AI elaborated or shortened content into the Knowledge Base articles, using the **Insert** button and update or publish them.

    \[Omitted image "insert-nacm-ai-text.png"\] Alt text: Insert the AI generated text into the Knowledge Base article.

    For more information about generating Knowledge Base articles using the Now Assist context menu, see [Edit an article using the Now Assist context menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/Now-Assist-generate-article-using-context-menu.md).

-   **Change Tone using Now Assist context menu**

    The Now Assist context menu enables users to change the tone of their content. Users can choose between casual, formal, and sympathetic tone to enhance their content further, using the generative AI capabilities.

    When you hover over the Now Assist icon or select **Refine** menu, you see **Change Tone** menu option.

    You can further choose a preferred tone and select **Formal**, **Casual**, and **Sympathetic**. Review the changes and select **Insert** to finalize the new text.

    \[Omitted image "nacm-change-tone.png"\] Alt text: Now Assist change tone selections.

    **Note:** If you do not see the change tone option for your application or product, reach out to ServiceNow.

-   **Limit the number of content refinement calls using the Now Assist context menu**

    Configure and limit the number of content refinements to the skill per session using the Now Assist context menu. By default, the maximum number of refinements isn’t set and you can configure to limit it.

    You can configure the refinement calls limitation at the **Recommendations Dialog Props** field in the **Limit refinements** record using the **refineCount** property.

    **Note:** The **Limit refinements** record is available in the Now Assist config var set record in the Now Assist Skill context menu application.

    \[Omitted image "nacm-limit-refines.png"\] Alt text: Configure the content refine limits to using the refineCount property.

    You can set the refineCount as follows:

    -   The default value of the property is **-1**. If the value is less than 0, then the number of refinements to the skill are unlimited.
    -   If you provide 0 as the value, then the refine button will be disabled and the `You reached the limit for refining content.` message is displayed.

        \[Omitted image "nacm-refineCount-zero.png"\] Alt text: The content refinement limited to zero or the refinements reached the maximum count.

    -   If you configure it with a value greater than 0, you’ll be able to refine the content according to the set value. For example, if you set the refineCount to 2, then you will be able to refine the content only twice.

        \[Omitted image "nacm-refineCount-configured.png"\] Alt text: The content refinement limit value set to two.

-   **Create knowledge article with open prompt**

    Use NAcm to create inline knowledge article using open prompts. See [Generate KB article with Now Assist context menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/generate-kb-article-with.md).

-   **Set the minimum word count for the Now Assist icon**

    You can set a minimum word count required for the Now Assist icon to appear, to control when the icon is displayed based on content length. To set the minimum word count, update the value for the `minSelectedWordCount` property.


-   **[Email recommendations using the Now Assist context menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/email-recommendations-nacm.md)**  
Use the Now Assist context menu to compose or respond to emails with recommendations from Now Assist with generative AI template suggestions. The Now Assist context menu enables users to generate email response recommendations in new, forward, reply, or reply all scenarios.
-   **[Summarize records with the Now Assist context menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/summarisation-with-now-assist-context-menu.md)**  
Use the Now Assist context menu to generate a record summary for the page, using Generative AI application assisted summarization capabilities in workspaces and UI16. The Now Assist context menu can generate a new summary, expand or collapse the summary card, share the summary to work notes, regenerate, or copy the summary.
-   **[Improve Docs content in Strategic Portfolio Management with Now Assist context menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/answer-queries-with-now-assist-context-menu.md)**  
Use the Now Assist context menu to start conversations and raise queries, using generative AI capabilities and custom built in skills in Strategic Portfolio Management.
-   **[Generate KB article with Now Assist context menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/generate-kb-article-with.md)**  
Use the Now Assist context menu to generate Knowledge Base articles in Knowledge Management.
-   **[Now Assist context menu usage dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-context-menu-dashboard.md)**  
Use the Now Assist Context Menu dashboard to monitor the use of Now Assist context menu across the different applications.
-   **[Use Now Assist context menu for custom skill deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/use-now-assist-context-menu-for-custom-skill-deployment.md)**  
Use the Now Assist context menu to deploy the custom skills created using Now Assist skill kit.

**Parent Topic:**[Now Assist Experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-experiences.md)

