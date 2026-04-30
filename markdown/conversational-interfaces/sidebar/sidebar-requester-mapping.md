---
title: Sidebar requester mapping
description: Create a requester mapping to define the requesting user for a record. This requester is used to identify the main contact for a record and Sidebar sends an email notification to the requester when they have unread messages in their discussions in the last 24 hours.
locale: en-US
release: yokohama
product: Sidebar
classification: sidebar
topic_type: task
last_updated: "2025-03-06"
reading_time_minutes: 1
breadcrumb: [Setting up Sidebar, Configuring Sidebar, Sidebar, Conversational Interfaces]
---

# Sidebar requester mapping

Create a requester mapping to define the requesting user for a record. This requester is used to identify the main contact for a record and Sidebar sends an email notification to the requester when they have unread messages in their discussions in the last 24 hours.

## Before you begin

Role required: admin

## Procedure

1.  On the Collaboration Chat Requester Mapping screen, fill in the fields:

<table id="table_tnb_j4y_42c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Activates the requester-mapping record.

</td></tr><tr><td>

Inherit

</td><td>

Extends and applies the feature to the child tables.

</td></tr><tr><td>

Table

</td><td>

Table to which the requester mapping should be applied.

</td></tr><tr><td>

Order

</td><td>

Order of the configuration.

 You can deﬁne multiple requester mapping conﬁgurations for a single table. The system executes the query in the descending order.

</td></tr><tr><td>

Requester

</td><td>

Requester for a record.

</td></tr><tr><td>

Domain

</td><td>

Domain for the record.

</td></tr></tbody>
</table>
