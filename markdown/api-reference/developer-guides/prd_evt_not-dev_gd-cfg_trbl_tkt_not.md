---
title: Configure trouble ticket notifications using the Producer Event Notification Framework
description: The base implementation of trouble ticket notification includes a set of trouble ticket events to demonstrate the capabilities of the system.
locale: en-US
release: zurich
product: Developer Guides
classification: developer-guides
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Producer Event Notification Framework developer guide, Developer guides, API implementation and reference]
---

# Configure trouble ticket notifications using the Producer Event Notification Framework

The base implementation of trouble ticket notification includes a set of trouble ticket events to demonstrate the capabilities of the system.

These trouble ticket events include:

-   Trouble ticket created \(incident\): `TROUBLE_TICKET_CREATE: "TroubleTicketCreateEvent"`
-   Trouble ticket created \(case\): `TROUBLE_TICKET_CREATE_FOR_CASE: "TroubleTicketCreateEventForCase"`
-   Trouble ticket status change \(incident\): `TROUBLE_TICKET_STATUS_CHANGE: "TroubleTicketStatusChangeEvent"`
-   Trouble ticket attribute value change \(incident\): `TROUBLE_TICKET_ATTRIBUTE_CHANGE: "TroubleTicketAttributeChangeEvent"`

If needed, you can add trouble ticket events to your implementation by performing the following steps:

1.  Add a new [business rule](../../../../script/business-rules/concept/c_BusinessRules.md#). This business rule must be associated with the table in which the record, incident or case, is stored. For additional information, see [Add a business rule for a new trouble ticket event](../reference/prd_evt_not-dev_gd-add_bus_rule.md).
2.  Configure the payload generation for the new trouble ticket event. For additional information see, [Generate the payload for a new trouble ticket event](../reference/prd_evt_not-dev_gd-gen_evt_pay.md)

You can also modify the payload of existing trouble ticket events. For details, see [Modify a trouble ticket event payload](../reference/prd_evt_not-dev_gd-mod-evt-pay.md).

