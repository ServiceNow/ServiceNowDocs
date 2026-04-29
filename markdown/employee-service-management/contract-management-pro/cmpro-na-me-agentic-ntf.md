---
title: Enable notifications for AI extracted metadata and obligations
description: Enable the email notifications for metadata extraction and obligation extraction to notify users when metadata extraction and obligation extraction are complete.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure agentic workflows, Configure, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Enable notifications for AI extracted metadata and obligations

Enable the email notifications for metadata extraction and obligation extraction to notify users when metadata extraction and obligation extraction are complete.

## Before you begin

Role required: admin

## About this task

The **AgenticAIMetadata extraction - Completed** and **AgenticAIObligationExtractionCompleted** notifications are not active by default.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  In the Name column, search for `AgenticAI`.

3.  Select the notification.Select .

    -   To activate notifications for metadata extraction, select **AgenticAIMetadata extraction - Completed**.
    -   To activate notifications for obligation extraction, select **AgenticAIObligationExtractionCompleted**.
    ![Notifications for metadata extraction and obligation extraction.](../image/cmpro-agentic-ai-notf.png "Agentic AI notifications")

4.  On the Notification form, select the **Active** check box.

5.  Select **Update**.


## What to do next

[Configure the workspace URL for contract metadata extraction notifications](cncore-config-ext-wrkspc-email.md)

**Parent Topic:**[Configuring agentic workflows in Now Assist in Contract Management](../concept/cmpro-conf-agentic-workflow.md)

**Related topics**  


[Activate business rules for the Manage contract repository agentic workflow](conf-repository-agentic-ai.md)

[Set the default notice period for the Manage contract repository agentic workflow](conf-sys-prop-default-np.md)

[Update the contracts AI agents handler script include](cmpro-script-includ-agenticAI.md)

