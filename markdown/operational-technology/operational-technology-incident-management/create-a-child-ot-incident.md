---
title: Create a child incident
description: Create a child Operational Technology \(OT\) incident record to capture part of the deviation reported so that it can be worked on separately. Creating child incidents can help you organize multiple incidents related to the same parent.
locale: en-US
release: zurich
product: Operational Technology Incident Management
classification: operational-technology-incident-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Operational Technology Incident Management, Operational Technology]
---

# Create a child incident

Create a child Operational Technology \(OT\) incident record to capture part of the deviation reported so that it can be worked on separately. Creating child incidents can help you organize multiple incidents related to the same parent.

## Before you begin

-   Enable the Create child incident feature \(**com.snc.incident.create.child.enable**\) property. For more information, see [Set the system properties](configure-ot-incident-management-properties.md).
-   Role required: sn\_ot\_incident\_write

## About this task

Fields that are copied over to the child incident are configured by using the **com.snc.sn\_ot\_incident.copy.attributes** system property.

## Procedure

1.  Navigate to the **OT Incidents** list module in the Industrial Workspace.

    Alternatively, you can go to an OT device record or equipment model entity record and select the **OT Incidents** tab.

2.  Open the OT incident that you want to create a child incident for.

3.  Select the **Child Incidents** related list.

4.  Select **New**.

5.  Fill in the details of the child incident.

6.  Select **Save**.


## Result

Now, you can view and edit the child incident in the parent incident record.

**Parent Topic:**[Using Operational Technology Incident Management](../concept/using-operational-technology-incident-mgt.md)

