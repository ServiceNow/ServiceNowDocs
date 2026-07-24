---
title: Create a chat launcher button in Care Team Mobile
description: Create a prominent action button that launches Now Assist chat or voice in the Care Team Mobile app.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hco-now-assist-create-launcher-button.html
release: australia
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 1
keywords: [Now Assist, chat launcher button, voice assistant, Care Team Mobile, prominent action button]
breadcrumb: [Configure, Now Assist for Care Team Operations, Healthcare and Life Sciences]
---

# Create a chat launcher button in Care Team Mobile

Create a prominent action button that launches Now Assist chat or voice in the Care Team Mobile app.

## Before you begin

Role required: admin

-   Verify that Now Assist is enabled on your instance. For more information, see [Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md).
-   Confirm that you have the appropriate permissions and licensing for AI voice capabilities, and that you have a Now Assist voice assistant created in Assistant Designer. For more information, see [Create an AI voice assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-an-ai-voice-service.md).

## Procedure

1.  Set the application scope to **Care Team Mobile**.

2.  Navigate to **All** &gt; **sys\_sg\_button.list**.

3.  Select **New**.

4.  Enter a title for your button in the **Name** field.

5.  Set **Type** to **Chat launcher**.

6.  Set **Context** to **Global**.

7.  Right-click and select **Save**.

8.  Navigate to **All** &gt; **sys\_sg\_button\_instance.list**.

9.  Select **New**.

10. Fill in the following fields.

    |Field|Value|
    |-----|-----|
    |Parent table|Mobile app config \[sys\_sg\_native\_client\]|
    |Location|Prominent Action|
    |Icon|Spark-solid \[AIS\]|
    |Active|True|

11. Under **Function**, select the chat launcher button created previously.

12. Under **Location**, select where the button appears on the page.

13. Right-click and select **Save**.


## Result

The chat launcher button is created and configured as a prominent action button in the Care Team Mobile app.

## What to do next

[Assign the chat launcher to a Care Team Mobile assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-now-assist-assign-launcher-assistants.md).

