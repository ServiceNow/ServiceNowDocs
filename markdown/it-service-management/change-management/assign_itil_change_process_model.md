---
title: Assign an ITIL change process to a change model
description: Assign an ITIL change process to a change model so the ChangeRequest API uses that model when it creates a matching change request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/assign\_itil\_change\_process\_model.html
release: brazil
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [assign, ITIL change process, change model]
breadcrumb: [ITIL change process assignment for change models, Configure, Change Management, IT Service Management]
---

# Assign an ITIL change process to a change model

Assign an ITIL change process to a change model so the ChangeRequest API uses that model when it creates a matching change request.

## Before you begin

Role required: `change_manager`

## About this task

Define which change model represents the Normal, Standard, or Emergency ITIL change process.

## Procedure

1.  Open the change model record that you want to represent an ITIL change process.

    Open an existing change model from the **Change Models** list, or create a change model by selecting **New** and entering a **Name**.

2.  Complete the following field:

    |Field|Description|
    |-----|-----------|
    |**ITIL change process**|Select the ITIL change process this change model represents: **Standard**, **Normal**, or **Emergency**. Leave the field set to **-- None --** if the model does not represent any of these processes. Only one active change model per domain can be set for each process.|

    **Note:** If you do not have write access to the change model already assigned to the selected process, the system blocks the save. A message appears stating that you do not have write access to the existing model for that ITIL change process.

3.  Select **Save**.

    **Note:** If you cannot save the change model with the selected ITIL change process, another active change model in your domain may already represent that process. Deactivate or update the other change model, or select a different process on this record.


## Result

The system saves the change model with the selected ITIL change process. The next time the ChangeRequest API creates a change request for that process, it uses this change model.

**Parent Topic:**[ITIL change process assignment for change models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/itil_change_process_models.md)

