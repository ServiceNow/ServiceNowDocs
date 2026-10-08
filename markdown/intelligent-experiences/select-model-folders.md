---
title: Select AI model and workspace folders
description: Select the AI model the agent uses, confirm its connection, and set the folders it works in. These settings control the quality of the agent's responses and limits file access to the selected folders.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/select-model-folders.html
release: brazil
topic_type: task
last_updated: "2026-09-27"
reading_time_minutes: 1
keywords: [general settings, AI model, workspace folders, local models]
breadcrumb: [Use, ServiceNow Cowork, Extending AI with external systems and providers, Enable AI Experiences]
---

# Select AI model and workspace folders

Select the AI model the agent uses, confirm its connection, and set the folders it works in. These settings control the quality of the agent's responses and limits file access to the selected folders.

## Before you begin

Role required: sn\_app\_cowork.user

## Procedure

1.  Navigate to **Settings** &gt; **General**.

2.  Under Connection &amp; Model, select a model from the **AI Model** list.

    To use a different model for a single chat, select a model from the model list in the conversation box.

3.  Select **Test Connection**.

4.  Under Workspace, set the folders the agent can read and write without prompting for approval.

    -   To add a folder, select **Add folder** and **Mark as primary** to make it your primary folder.
    -   To change a folder, select the edit icon next to it.
    -   To remove a folder, select the remove icon next to it and select **Remove folder** in the dialog box.
    -   To return to your home folder as the only workspace, select **Reset to Home**.
5.  Under Local Models, confirm that each model shows **Installed**.

    These models run on your device, so dictation and semantic search are processed locally on your device.


## Result

The agent uses the model you selected, and a prompt appears before the agent reads or writes anything outside your workspace folders.

**Parent Topic:**[Using ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/servicenow-cowork-using.md)

