---
title: Create state model transition
description: Create state models to control the workflow of a privacy case by defining the states and transition conditions.
locale: en-US
release: xanadu
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Privacy Case Management, Privacy Management, Governance, Risk, and Compliance]
---

# Create state model transition

Create state models to control the workflow of a privacy case by defining the states and transition conditions.

## Before you begin

Ensure that you are in the GRC: Privacy Case Management application.

Role required: sn\_privacy\_case.privacy\_case\_admin

## Procedure

1.  Navigate to **All** &gt; **Privacy Case Management** &gt; **State Models**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the state model. For example, `Breach case`.|
    |Application|Scope of the application. This field is automatically set to **GRC: Privacy Case Management**.|
    |Active|Option to indicate that the state model is active or inactive.|
    |Table name|Table this state model applies to.|
    |State model field|Fields that contain the state model value in the table that this state model applies to.|
    |State field|Fields that contain the state value in the table that this state model applies to. This field is automatically set to **State \[state\]**.|

4.  Select **Submit**.


-   **[Define the workflow states for a privacy case](define-pcm-workflow-states.md)**  
Define the workflow states for a privacy case that govern the lifecycle of the case.

**Parent Topic:**[Configuring Privacy Case Management](../concept/configuring-privacy-case-management.md)

