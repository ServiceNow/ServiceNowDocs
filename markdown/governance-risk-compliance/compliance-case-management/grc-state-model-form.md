---
title: GRC State Model form
description: Use the GRC State Model form to define the workflow states and transition conditions in the Compliance Case Management application.
locale: en-US
release: australia
product: Compliance Case Management
classification: compliance-case-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create compliance state model, Configure, Compliance Case Management, Governance, Risk, and Compliance]
---

# GRC State Model form

Use the GRC State Model form to define the workflow states and transition conditions in the Compliance Case Management application.

See the following table for a description of the field values.

|Field|Description|
|-----|-----------|
|Name|Name of the state model. For example, Breach case.|
|Application|Name of the application that this state model applies to. This field is automatically set to **GRC: Compliance Case Management**.|
|Active|Option to select the state model as active or inactive.|
|Table name|List of applications the State model has to be applied for the business configuration. This field is automatically set to **Compliance case \[sn\_comp\_case\_compliance\_case\]**.|
|State model|Field to hold the state model value in a table that this state model applies to. It is dependent on Table name and displays a list of corresponding state model values.|
|State field|Field to hold the state value in a table that this state model applies to. It is dependent on Table name. This field is automatically set to **State**. You can change the value to match your configuration.|
|Manage Attachments|Select this icon and choose the required files to attach.|

**Parent Topic:**[Create a compliance state model](../task/create-state-model.md)

