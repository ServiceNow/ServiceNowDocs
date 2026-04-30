---
title: Edit code with Now Assist
description: Quickly enhance your scripts by instructing Now Assist on how to improve the code.
locale: en-US
release: zurich
product: Scripts
classification: scripts
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use Now Assist for Code, Now Assist for Code, Scripting, API implementation, API implementation and reference]
---

# Edit code with Now Assist

Quickly enhance your scripts by instructing Now Assist on how to improve the code.

## Before you begin

Role required: authenticated user

## About this task

When code generation is enabled on an instance, a Now Assist icon \(![Now Assist icon.](../../../common/image/icon-ai-sparkle.png)\) appears in the script editor.

## Procedure

1.  Navigate to a script.

    For example, to open a script include form, navigate to **All** &gt; **System Definition** &gt; **Script Includes** and select a script include.

2.  In the script editor, use one of the following options to edit code:

    -   Select the code that you want to edit. Right-click and select **Open Code with Now Assist**.

        ![Open code with Now Assist](../image/now-assist-code-open-code.png)

    -   Select the code and then select the **Quick Actions** button.![Edit code with Quick Actions](../image/now-assist-code-quick-actions.png)
    -   Select the code and use one of the following keyboard shortcuts:
        -   Windows: Ctrl-Enter
        -   Mac: Cmd-Enter
    **Tip:** Select the Help icon \(![Help icon.](../../general-scripting/image/Help.png)\) to access the list of relevant keyboard shortcuts.

3.  In the **Edit code with Now Assist** dialog box, enter text that describes how you want to refactor the code.

    The text you enter must be fewer than 1,000 characters.

4.  Press Enter to generate an edited code suggestion.

    A view comparing the original code and the edited code suggestion appears in the script editor.

    ![Original code and edited code suggestion compared in the script editor.](../image/now-assist-code-edit-diff.png)

5.  Review the edited code suggestion and complete one of the following steps:

    -   To overwrite the original code with the edited code suggestion, select **Accept**.
    -   To regenerate a suggestion, revise the text in the dialog box and select the arrow icon \(![Arrow icon.](../image/now-assist-code-arrow.png)\).
    -   To remove the edited code from the script and keep only the original code, select **Reject**.
    When you accept a code suggestion, a line next to the line numbers indicates which code was created by AI and hasn't been edited. If you edit AI-generated code, the line indicator doesn’t appear for those lines of code.

    ![Line indicating which lines of code are AI-generated.](../image/now-assist-code-edit-indicator.png)

    If the code suggestion doesn’t meet your requirements, try rephrasing your prompt according to the prompt guidance and generating another code suggestion.

6.  Select **Submit** or **Update** to save your changes.


