---
title: Enable Voice Assistant in Care Team Mobile
description: Create a prominent action button that launches Now Assist chat or voice in the Care Team Mobile app.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/healthcare-life-sciences/healthcare-and-life-sciences/hco-now-assist-create-launcher-button.html
release: zurich
product: Healthcare and Life Sciences
classification: healthcare-and-life-sciences
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 1
breadcrumb: [Configure Care Team Mobile, Care Team Mobile, Healthcare Operations, Healthcare and Life Sciences]
---

# Enable Voice Assistant in Care Team Mobile

Create a prominent action button that launches Now Assist chat or voice in the Care Team Mobile app.

## Before you begin

Role required: admin

-   Verify that Now Assist is enabled on your instance. For more information, see Now Assist.
-   Confirm that you have the appropriate permissions and licensing for AI voice capabilities, and that you have a Now Assist voice assistant created in Assistant Designer. For more information, see Create an AI voice assistant.

## Procedure

1.  Set the scope to **Care Team Mobile**.

2.  Navigate to **All** &gt; **sys\_sg\_button.list**.

3.  Select an existing button or select **New** to create one.

4.  Enter a title for your button in the **Name** field.

5.  Set **Type** to **Chat launcher**.

6.  Set **Context** to **Global**.

7.  Right-click and select **Save**.

8.  Navigate to **All** &gt; **sys\_sg\_button\_instance.list**.

9.  Select an existing record or select **New** to create one.

10. Fill in the following fields.

    |Field|Value|
    |-----|-----|
    |Name|CTO PAB|
    |Parent table|Mobile app config \[sys\_sg\_native\_client\]|
    |Function|CTO PAB|
    |Label|CTO PAB|
    |Location|Prominent Action|
    |Icon|Spark-solid \[AIS\]|
    |Active|Set to true.|

11. Under **Function**, select the chat launcher button you created previously.

12. Under **Location**, select where the button appears on the page.

13. Right-click and select **Save**.


