---
title: Create or modify Badge Reader Integration event handlers
description: Configure actions associated with a badge scan event and define the code to execute when a badge is scanned.
locale: en-US
release: australia
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Walk-up Experience Badge Reader Integration setup and configuration, Badge Reader Integration for Walk-up Experience, Configure, Walk-up Experience, IT Service Management]
---

# Create or modify Badge Reader Integration event handlers

Configure actions associated with a badge scan event and define the code to execute when a badge is scanned.

## Before you begin

Role required: sn\_badge.badge\_admin

## About this task

Using the **Badge Event Handlers** module you can map badge event handlers to multiple badge readers. For example, you may have a badge reader at your San Diego, CA walk-up location and another badge reader at your Santa Clara, CA location. Both of these badge readers can be mapped to the same Walk-up Badge Reader event.

Badge Event Handler records are delivered as part of the Walk-up Experience application-specific badge reader integrations.

**Note:**

The code entered in the **Script** field of the Badge Event Handler form is executed using a GlideScopedEvaluator in the BadgeScanProcessor.

## Procedure

1.  Navigate to **All** &gt; **Badge Reader Integration** &gt; **Badge Event Handlers**.

    The Badge Event Handlers list appears and displays any existing badge event handlers.

2.  To modify an existing badge event handler, click on the name.

    Otherwise, to create a new badge event handler, click **New**.

3.  Enter a name for the badge event handler in the **Name** field.

    For example, `Walk-up Badge Event`.

4.  Enter details in the **Short description** field, if desired.

5.  Enter code after `// your code goes here` in the **Script** field.

    ![Badge event handlers script](../image/BadgeEventHandlers.png)

    ![Badge event handler code](../image/BadgeEventHandlerCode.png)

    **Note:** The **Application** field is set to **Global** until you enter the code specifying Walk-up Experience application in the **Script** field and save or submit the record.

6.  Click **Submit** to create the record.


**Parent Topic:**[Walk-up Experience Badge Reader Integration setup and configuration](../concept/walkup-badge-read-integ-config.md)

