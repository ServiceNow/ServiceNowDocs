---
title: Generate code with AI-powered code generation
description: Generate code from text with AI-powered Now Assist for Code.
locale: en-US
release: australia
product: Scripts
classification: scripts
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use Now Assist for Code, Now Assist for Code, Scripting, API implementation, API implementation and reference]
---

# Generate code with AI-powered code generation

Generate code from text with AI-powered Now Assist for Code.

## Before you begin

Learn how to write prompts to generate better code suggestions. For more information, see [General guidelines for code generation](../concept/general-guidelines-code-generation.md).

Role required: now.assist.creator

## Procedure

1.  Navigate to a form with a script field.

    For example, to open a script include form:

    -   Navigate to **All** &gt; **System Definition** &gt; **Script Includes** and select **New** or enter `sys_script_include.do` in the navigation filter.
    -   Navigate to **All** &gt; **System Definition** &gt; **Script Includes** and select a script include.
2.  In the script editor, place your cursor where you want to add code.

3.  Right-click and select **Open Code with Now Assist** or use one of the following keyboard shortcuts:

    -   Windows: Ctrl-Enter
    -   Mac: Cmd-Enter
    **Tip:** Select the Help icon \(![Help icon.](../../general-scripting/image/Help.png)\) to access the list of relevant keyboard shortcuts.

4.  In the **Code with Now Assist** dialog box, enter text that describes the desired goal of the code to generate.

    The text you enter must be fewer than 1,000 characters.

5.  Press Enter to generate a code suggestion.

    The code suggestion appears highlighted in the script editor.

    ![Code with Now Assist dialog box with the text "Validate emails using regex" and a code suggestion in the script editor.](../image/now-assist-code-dialog.png)

6.  Review the code suggestion and complete one of the following steps:

    -   To include it in your script and make any edits, select **Accept**.
    -   To regenerate a suggestion, revise the text in the dialog box and select the arrow icon \(![Arrow icon.](../image/now-assist-code-arrow.png)\).
    -   To remove it from the script, select **Reject**.
    When you accept a code suggestion, a line next to the line numbers indicates which code was created by AI and hasn't been edited. If you edit AI-generated code, the line indicator doesn’t appear for those lines of code.

    ![Line indicating which lines of code are AI-generated.](../image/now-assist-code-indicator-modal.png)

    If the code suggestion doesn’t meet your requirements, try rephrasing your prompt according to the prompt guidance and generating another code suggestion.

7.  Select **Submit** or **Update** to save your changes.

    **Note:** Depending on your workflow needs, you can use the prompt modal in either inline or floating mode. In the inline mode, the prompt modal is embedded within the script editor. In the floating mode you can move the prompt modal around the script editor. Toggling between these two modes is simple. When in inline mode, select the **Pop Out** toggle to switch to floating mode. Conversely, when in floating mode, select the **Pop In** toggle to return to inline mode. The transition between inline and floating modes preserve all text within the modal.


