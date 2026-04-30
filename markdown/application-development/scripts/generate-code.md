---
title: Generate scripts with AI-powered code generation
description: Generate scripts from text, code, or a combination of both with AI-powered code generation.Write scripts quickly with AI-generated code by telling Now Assist what you want the script to do.Write scripts quickly with AI-generated code completion.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Now Assist for code generation, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Generate scripts with AI-powered code generation

Generate scripts from text, code, or a combination of both with AI-powered code generation.

When code generation is enabled on an instance, a Now Assist icon \(![Now Assist icon.](../../../common/image/icon-ai-sparkle.png)\) appears in the script editor.

Developers must be assigned the now.assist.creator role to use code generation.

## Generate scripts from text

Write scripts quickly with AI-generated code by telling Now Assist what you want the script to do.

### Before you begin

Learn how to write prompts to generate better code suggestions. For more information, see [General guidelines for code generation](https://www.servicenow.com/docs/access?context=general-guidelines-code-generation&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

Role required: now.assist.creator

### Procedure

1.  Navigate to a form with a script field.

    For example, to open a script include form, navigate to **All** &gt; **System Definition** &gt; **Script Includes** and select **New** or enter `sys_script_include.do` in the navigation filter.

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


## Generate scripts from code

Write scripts quickly with AI-generated code completion.

### Before you begin

Role required: now.assist.creator

### Procedure

1.  Navigate to a form with a script field.

    For example, to open a script include form, navigate to **All** &gt; **System Definition** &gt; **Script Includes** and select **New** or enter `sys_script_include.do` in the navigation filter.

2.  In a script field, enter code or a combination of text and code:

    -   Enter the beginning of a function or other code to be automatically completed. For example:

        ```javascript
        var email = current.getValue('email');
        var regex =  
        
        ```

    -   Enter a combination of text in a code comment that describes the desired goal of the code to generate followed by an example of how you want the code to start. For example:

        ```javascript
        // Validate emails using regex
        var email = current.getValue('email');
        var regex =  
        
        ```

3.  Right-click and select **Auto-generate code completion** or use one of the following keyboard shortcuts to generate a code suggestion:

    -   Windows: Ctrl-Windows logo key-Enter
    -   Mac: Ctrl-Cmd-Enter
    **Tip:** Select the Help icon \(![Help icon.](../../general-scripting/image/Help.png)\) to access the list of relevant keyboard shortcuts.

    The code preceding your cursor must be fewer than 1,000 characters when triggering code generation.

    **Note:** If automatic code suggestions are enabled, you get code suggestions automatically after you enter a prompt and then stop typing or moving the cursor for 2.5 seconds.

    You can't edit the prompt after triggering the code generation. If you need to edit your prompt before the code suggestion is returned, you can cancel the code generation by pressing the Backspace key.

    The spinner icon \(![Spinner icon.](../image/now-assist-code-spinner.png)\) appears while generating a suggestion. The code suggestion appears in the lines following your prompt but isn’t added to your script until you accept it.

    ![Prompt and code suggestion in the script editor.](../image/now-assist-code-complete-suggestion.png)

4.  Accept the code to include it in your script or reject it to remove it from the script.

    -   Accept: Press the Tab key or the right arrow key. Selecting within the suggested code also accepts the suggestion.
    -   Reject: Press the Escape key, left arrow key, or up arrow key. Typing or selecting anywhere outside of the suggested code within the script also removes the suggestion.
    When you accept a code suggestion, a line next to the line numbers indicates which code was created by AI and hasn't been edited. If you edit AI-generated code, the line indicator doesn’t appear for those lines of code.

    ![Line indicating which lines of code are AI-generated.](../image/now-assist-code-indicator.png)

    If the code suggestion doesn’t meet your requirements, try modifying your code and generating another code suggestion.

5.  Select **Submit** or **Update** to save your changes.


