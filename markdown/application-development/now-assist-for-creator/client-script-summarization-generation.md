---
title: Summarize a client script using Now Assist
description: Use the client script summarization skill to generate a plain-language summary of a client script directly in the UI Builder editor.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 2
breadcrumb: [Use, UI generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Summarize a client script using Now Assist

Use the client script summarization skill to generate a plain-language summary of a client script directly in the UI Builder editor.

## Before you begin

Make sure that you install UI generation and that you have the ui\_builder\_admin role. For more information, see [Install UI generation](install-ui-generation.md) and [Grant UI Builder admin role](grant-ui-builder-admin-role.md).

Turn on the Client script summarization skill.

Role required: ui\_builder\_admin

## About this task

Client scripts can be long and complex. The Explain code with Now Assist panel appears on the right side of the Edit client script dialog and generates a structured explanation of the selected script on demand. You can request a new explanation if the first response does not meet your needs.

## Procedure

1.  In the application navigator, navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience with a client script.

3.  Select a page to open the page editor.

4.  From the Data and scripts panel, open a client script.

    The Explain Code panel appears if you have the ui\_builder\_admin role and have enabled the Client script summarization skill.

5.  Select **Explain this code**.

    Now Assist sends the script to the skill endpoint. When processing is complete, the panel displays two sections:

    -   Summary: A concise description of what the script does.
    -   Code explanation: A detailed explanation of how the script works, including which APIs are used and what each state variable does.
    **Note:** If you change the script, a message in the **Explain code panel** notifies you of the update and asks whether the code should be explained again. Select **Explain again** to generate a new summary.

6.  If the generated summary does not provide sufficient clarity, select the regenerate icon to request a new response from Now Assist.

    The model generates an alternative explanation for the same script.

7.  Review the summary and code explanation, then select **Cancel** or **Apply** as appropriate to close the dialog.


## Result

A concise summary, information about where the client script is triggered, and a detailed explanation of the script's functionality are displayed. Use this information to decide whether to keep, modify, or replace the script.

|Symptom|Likely Cause|Resolution|
|-------|------------|----------|
|Explain Code panel does not appear|Client script summarization skill is disabled, or user lacks the ui\_builder\_admin role.|Activate Client script summarization skill in Now Assist Admin. Confirm the user has the ui\_builder\_admin role.|

**Parent Topic:**[Using UI generation](../concept/using-ui-generation.md)

**Related topics**  


[bundle-crapiref.client-scripts]

[Client script summarization](../concept/client-script-summarization.md)

[Use case: Summarize a client script using Now Assist](../concept/use-case-client-script-summarization.md)

