---
title: Edit code with Now Assist
description: Edit scripts quickly by telling Now Assist how to improve the code.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/api-reference/scripts/edit-code-now-assist.html
release: xanadu
product: Scripts
classification: scripts
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Now Assist for code generation, Scripting, API implementation, API implementation and reference]
---

# Edit code with Now Assist

Edit scripts quickly by telling Now Assist how to improve the code.

## Before you begin

Role required: now.assist.creator

## About this task

When code generation is enabled on an instance, a Now Assist icon \(\[Omitted image "icon-ai-sparkle.png"\] Alt text: Now Assist icon.\) appears in the script editor.

## Procedure

1.  Navigate to a script.

    For example, to open a script include form, navigate to **All** &gt; **System Definition** &gt; **Script Includes** and select a script include.

2.  In the script editor, highlight the code to edit.

3.  Right-click and select **Open Code with Now Assist** or use one of the following keyboard shortcuts:

    -   Windows: Ctrl-Enter
    -   Mac: Cmd-Enter
    **Tip:** Select the Help icon \(\[Omitted image "Help.png"\] Alt text: Help icon.\) to access the list of relevant keyboard shortcuts.

4.  In the **Edit code with Now Assist** dialog box, enter text that describes how you want to refactor the code.

    The text you enter must be fewer than 1,000 characters.

5.  Press Enter to generate an edited code suggestion.

    A view comparing the original code and the edited code suggestion appears in the script editor.

    \[Omitted image "now-assist-code-edit-diff.png"\] Alt text: Original code and edited code suggestion compared in the script editor.

6.  Review the edited code suggestion and complete one of the following steps:

    -   To overwrite the original code with the edited code suggestion, select **Accept**.
    -   To regenerate a suggestion, revise the text in the dialog box and select the arrow icon \(\[Omitted image "now-assist-code-arrow.png"\] Alt text: Arrow icon.\).
    -   To remove the edited code from the script and keep only the original code, select **Reject**.
    When you accept a code suggestion, a line next to the line numbers indicates which code was created by AI and hasn't been edited. If you edit AI-generated code, the line indicator doesn’t appear for those lines of code.

    \[Omitted image "now-assist-code-edit-indicator.png"\] Alt text: Line indicating which lines of code are AI-generated.

    If the code suggestion doesn’t meet your requirements, try rephrasing your prompt according to the prompt guidance and generating another code suggestion.

7.  Select **Submit** or **Update** to save your changes.


