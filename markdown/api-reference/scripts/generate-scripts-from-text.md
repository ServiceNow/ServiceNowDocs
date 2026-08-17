---
title: Generate code with AI-powered code generation
description: Generate code from text with AI-powered ServiceNow Otto for Code.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/scripts/generate-scripts-from-text.html
release: australia
product: Scripts
classification: scripts
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, ServiceNow Otto for Code, Scripting, API implementation, API implementation and reference]
---

# Generate code with AI-powered code generation

Generate code from text with AI-powered ServiceNow Otto for Code.

## Before you begin

Learn how to write prompts to generate better code suggestions. For more information, see [General guidelines for code generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/general-guidelines-code-generation.md).

Role required: now.assist.creator

## Procedure

1.  Navigate to a form with a script field.

    For example, to open a script include form:

    -   Navigate to **All** &gt; **System Definition** &gt; **Script Includes** and select **New** or enter `sys_script_include.do` in the navigation filter.
    -   Navigate to **All** &gt; **System Definition** &gt; **Script Includes** and select a script include.
2.  In the script editor, place your cursor where you want to add code.

3.  Right-click and select **Open Code with Otto** or use one of the following keyboard shortcuts:

    \[Omitted image "soc-generate-code-with-otto.png"\] Alt text: Generate code with Otto

    -   Windows: Ctrl-Enter
    -   Mac: Cmd-Enter
    **Tip:** Select the Help icon \(\[Omitted image "soc-help-icon.png"\] Alt text: Help icon\) to access the list of relevant keyboard shortcuts.

4.  In the **Generate code with Otto** dialog box, enter text that describes the desired goal of the code to generate.

    \[Omitted image "soc-generate-code-with-otto-textbox.png"\] Alt text: In the Generate code with Otto dialog box, enter text that describes the desired goal

    The text you enter must be fewer than 1,000 characters.

5.  Press Enter or select **Submit** \(\[Omitted image "soc-submit-icon.png"\] Alt text: Submit icon\) to generate a code suggestion.

    The code suggestion appears highlighted in the script editor.

    \[Omitted image "soc-generate-code-accept-reject.png"\] Alt text: The code suggestion appears highlighted in the script editor

6.  Review the code suggestion and complete one of the following steps:

    -   To include it in your script and make any edits, select **Accept**.
    -   To regenerate a suggestion, revise the text in the dialog box and select **Submit** \(\[Omitted image "soc-submit-icon.png"\] Alt text: Submit icon\).
    -   To remove it from the script, select **Reject**.
    When you accept a code suggestion, a line next to the line numbers indicates which code was created by AI and hasn't been edited. If you edit AI-generated code, the line indicator doesn’t appear for those lines of code.

    \[Omitted image "soc-generate-code-accept.png"\] Alt text: Line indicating which lines of code are AI-generated.

    If the code suggestion doesn’t meet your requirements, try rephrasing your prompt according to the prompt guidance and generating another code suggestion.

7.  Select **Submit** or **Update** to save your changes.

    **Note:** Depending on your workflow needs, you can use the prompt modal in either inline or floating mode. In the inline mode, the prompt modal is embedded within the script editor. In the floating mode you can move the prompt modal around the script editor. Toggling between these two modes is simple. When in inline mode, select the **Pop Out** \(\[Omitted image "soc-pop-out-in-icon.png"\] Alt text: Pop out icon\) to switch to floating mode. Conversely, when in floating mode, select the **Pop In** \(\[Omitted image "soc-pop-in-out-icon.png"\] Alt text: Pop in icon\) to return to inline mode. The transition between inline and floating modes preserve all text within the modal.


