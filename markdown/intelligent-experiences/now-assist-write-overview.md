---
title: Now Assist context menu
description: The Now Assist context menu uses generative AI to help agents summarize, create, and edit written content, thus streamlining their writing tasks.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
keywords: [Now Assist, Now Assist context menu, Generative AI, Gen AI, Streamline]
breadcrumb: [Exploring Now Assist, Now Assist, Enable AI experiences]
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

The Now Assist context menu is available on any field where the floating Now Assist button \(![Now Assist context menu icon](../images/wwna-icon.png)\) appears. If you start typing in the field, a menu appears with the available Now Assist context menu actions. The Now Assist context menu helps you summarize, create or modify existing documentation.

-   **Chat window using the Now Assist context menu**

    You can use the Now Assist context menu when communicating with users in Agent Chat:

    If it takes too long to generate text or the Now LLM Service isn't available, an error message appears.

    ![Agent Chat window with the Now Assist context menu icon](../images/wwna-agent-chat-window.png)

-   **Change request risk explanation using the Now Assist context menu**

    The Now Assist context menu makes the change request risk explanation available on the workspace and on UI16 after assessment and calculation.

    When the risk is assessed and calculated, you’ll see the **Explain risk** button with the Now Assist ![The Now Assist icon.](../images/wwna-icon.png) icon on the workspace showing the risk explanation in a dialog box in the Record information section.

    ![The change request risk explanation powered by Now Assist.](../images/change-risk-explntn-wrkspc-nacm.png)

    When the risk is assessed and calculated, you’ll see the Now Assist ![The Now Assist icon.](../images/wwna-icon.png) icon against the **Risk** field on UI16, showing the risk explanation in a dialog box.

    ![Now Assist showing the change risk explanation.](../images/change-risk-explntn-nacm.png)

    **Note:** The risk explanation that is presented in the dialog box is assessed and calculated on the change request form.

    For more information about risk assessment and calculation, see [Risk assessment](https://www.servicenow.com/docs/access?context=c_RskAsmtCalc&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

-   **Content editing using Now Assist content menu**

    The Now Assist context menu enables generative AI assisted content editing capabilities for user authoring and providing resolution notes in workspaces and UI16.

    When you select some content, you’ll see the Now Assist ![The Now Assist icon.](../images/wwna-icon.png) icon pop-up and float along with your mouse device.

    When you hover over the Now Assist icon or select **Refine** menu, you will see the following menu options to help you edit the content:

    -   **Elaborate**: Generative AI details the selected text.
    -   **Shorten**: Generative AI shortens the selected text.
    -   **Change Tone**: Generative AI changes the tone of the selected text to sound formal, casual, or Sympathetic.
    If you select **Elaborate** or **Shorten**, generative AI provides alternative content option. You can select **Insert** button to update the content and publish. For more information, see [Edit an article using the Now Assist context menu](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-using-context-menu&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

    If you select **Change Tone**, Now Assist context menu allows you to further choose a preferred tone between **Formal**, **Casual**, and **Sympathetic**. Select **Insert** to add the refined text.

    ![Now Assist change tone selections.](../images/nacm-change-tone.png)

-   **Limit the number of content refinement calls using the Now Assist context menu**

    Configure and limit the number of content refinements to the skill per session using the Now Assist context menu. By default, the maximum number of refinements isn’t set and you can configure to limit it.

    You can configure the refinement calls limitation at the **Recommendations Dialog Props** field in the **Limit refinements** record using the **refineCount** property.

    **Note:** The **Limit refinements** record is available in the Now Assist config var set record in the Now Assist Skill context menu application.

    ![Configure the content refine limits to using the refineCount property.](../images/nacm-limit-refines.png)

    You can set the refineCount as follows:

    -   The default value of the property is **-1**. If the value is less than 0, then the number of refinements to the skill are unlimited.
    -   If you provide 0 as the value, then the refine button will be disabled and the `You reached the limit for refining content.` message is displayed.

        ![The content refinement limited to zero or the refinements reached the maximum count.](../images/nacm-refineCount-zero.png)

    -   If you configure it with a value greater than 0, you’ll be able to refine the content according to the set value. For example, if you set the refineCount to 2, then you will be able to refine the content only twice.

        ![The content refinement limit value set to two.](../images/nacm-refineCount-configured.png)


**Related topics**  


[Edit an article using the Now Assist context menu](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-using-context-menu&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

