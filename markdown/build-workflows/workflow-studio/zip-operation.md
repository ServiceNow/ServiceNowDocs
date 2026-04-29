---
title: Zip operation
description: Compress one or more record attachments into a single zip archive. You can also manage the contents of a zip archive by removing specific attachments from the zipped file.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ZIP step, Steps, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Zip operation

Compress one or more record attachments into a single zip archive. You can also manage the contents of a zip archive by removing specific attachments from the zipped file.

|Field|Description|
|-----|-----------|
|Operation|**Zip** operation that archives the attachments in the required record.|
|Source Attachment Records|Records that contain the attachments that you want to archive.|
|Target Zip File Name|Name of the zipped archive.|
|Target record|Record that you want to archive the attachments to.|
|Target Table|Table related to the target record. The table is automatically populated when you select the record from the **Target record** field.|
|Advanced Options|
|Delete Source Files|Field used to remove the original attachments from the source record after the attachments are archived.|

## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see [Action error evaluation](../concept/action-error-evaluation.md).


**Parent Topic:**[ZIP step](zip-step.md)

