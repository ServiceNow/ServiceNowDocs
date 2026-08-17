---
title: Generate audio summaries and query documents using voice
description: Generate audio summaries and interact using voice-based questions to understand and extract key information from documents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/generate-audio-summary-voice-questions-now-assist.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, ServiceNow Otto in Document Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Generate audio summaries and query documents using voice

Generate audio summaries and interact using voice-based questions to understand and extract key information from documents.

## Before you begin

Configure the Voice Assist for docs skill. For more information, see [Configure Voice Assist for Docs skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configure-skill-voice-assist.md).

**Warning:** Voice Q&amp;A uses Google's Gemini API. Your use of this feature is subject to the Google Gemini API Terms of Service or other applicable agreement you may have with Google governing your use of this API. You must grant microphone access to use voice Q&amp;A.

Role required: sn\_voice\_doc.user and admin defined roles

## Procedure

1.  Navigate to your workspace.

2.  Select a record from a list that has the Voice Assist for docs skill activated.

    For example, select an incident record.

3.  Open an attached document to view it in the document viewer.

    **Note:**

    -   Maximum document size: 10 MB
    -   Maximum pages: 30
    -   Supported file types: pdf, docx, pptx, xlsx, doc, ppt, xls, jpeg, png
4.  Select the **Ask Otto** drop-down button \[Omitted image "icon-ask-otto-dropdown.png"\] Alt text: Ask otto dropdown button icon

5.  Select **Show Voice-Assist**.

6.  For Audio Summary feature:

    1.  Select **Generate audio summary**
    2.  Select \[Omitted image "icon-play.png"\] Alt text: play button icon to generate an audio summary of the document.
    3.  Select \[Omitted image "icon-toggle.png"\] Alt text: toggle button icon to view auto-generated transcript of the audio summary.
7.  For Voice Q&amp;A feature:

    1.  Select **Start Voice Q&amp;A** to ask questions regarding the documents by using your voice.
    2.  Select the check box in **Voice Q&amp;A-User Consent** section.
    3.  Select **Grant access**.
    4.  Ask questions related to your document.
    5.  To mute the microphone, select \[Omitted image "microphone-outline-24.svg"\] Alt text: microphone icon
    6.  To unmute the microphone, select \[Omitted image "microphone-slash-fill-24.svg"\] Alt text: unmute icon
    7.  To generate live captions, select \[Omitted image "icon-livecaption.png"\] Alt text: live caption icon
8.  When you finish, select **End**, to end the voice conversation.


