---
title: Create an incident state model
description: Create an Operational Technology \(OT\) incident state model for your sites. By using an incident state model, you can manage the life cycle of the related incidents.
locale: en-US
release: yokohama
product: Operational Technology Incident Management
classification: operational-technology-incident-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure, Operational Technology Incident Management, Operational Technology]
---

# Create an incident state model

Create an Operational Technology \(OT\) incident state model for your sites. By using an incident state model, you can manage the life cycle of the related incidents.

## Before you begin

-   Set the application scope to **Operational Technology Incident Management**.
-   Role required: admin

## About this task

By using state management, you can configure a state model for OT incident sites and their incident life cycles. You can create one model per site.

For more information about state management and state models, see [State Management](https://www.servicenow.com/docs/access?context=state-model&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

For more information about the incident life cycles, see [Operational Technology Incident Management](../concept/operational-technology-incident-management.md).

## Procedure

1.  Navigate to **All** &gt; **State Management** &gt; **State Models**.

2.  Select the **OT Incident: Default Flow** model.

3.  Set the **Condition**.

4.  In the State Transitions Context menu, configure the State Transition records as required.

    For example, if you want to edit the **Enter Condition** field of the **In Progress** state record, select the state record, add your changes, and select **Update**.

5.  Select **Update**.


## Result

Now, the state model accurately describes the expected record workflow through the life cycle of the incident record.

**Parent Topic:**[Configuring Operational Technology Incident Management](../concept/configuring-operational-technology-incident-mgt.md)

