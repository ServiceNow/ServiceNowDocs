---
title: Attorney Client Privilege
description: Attorney Client Privilege enables legal fulfiller or matter owner to designate legal matters as privileged and confidential. It restricts access to authorized stakeholders, marks communications with confidentiality banners, and maintains a document audit trail to help you protect sensitive legal communications.
locale: en-US
release: australia
product: Legal Matter Management
classification: legal-matter-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [ACP, Attorney client privilege, Privileged and confidential]
breadcrumb: [Explore, Legal Matter Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Attorney Client Privilege

Attorney Client Privilege enables legal fulfiller or matter owner to designate legal matters as privileged and confidential. It restricts access to authorized stakeholders, marks communications with confidentiality banners, and maintains a document audit trail to help you protect sensitive legal communications.

Attorney Client Privilege applies to following:

-   Legal Request: Legal fulfillers can mark legal requests as privileged and confidential, when the request is in Assigned or Work in Progress state. The system enforces access control, adds confidentiality markers to emails, and restricts collaboration to authorized stakeholders.
-   Legal Matter: Legal fulfillers and matter owners can independently mark or unmark individual matters as privileged and confidential, provided the matter is in the Assigned or Work in Progress state.

## Assignment group permission changes

When privileged and confidential is enabled on a legal matter, the system automatically updates the assignment group permission to No access.

## Indicators of a privileged and confidential matter

You can identify a privileged and confidential matter by following UI elements.

-   Privileged and Confidential flag: Displayed in the secondary header of the matter when it is marked as privileged and confidential.
-   Privileged document access related list to display the status of each attachment.

![Identify privileged and confidential matter](../../legal-request-management/image/lmm-acp-indicator.png)

## Email notifications

Email communications generated from Privileged and Confidential matters include confidentiality markers to comply with legal requirements. This applies to both system-generated notifications and fulfiller-initiated outbound emails.

## Stakeholder change notifications

When the collaborator list, watchlist, or fulfiller assignment is modified for a privileged and confidential matter, the system sends email notifications to the requester, fulfiller, and collaborators. Notifications are triggered when:

-   A new collaborator is added to the matter.
-   A new watchlist entry is added.
-   The fulfiller assignment changes.

All notifications for privileged and confidential matter include the confidentiality markers.

## Promote legal request to legal matter

You can promote a legal request to legal matter by creating a new matter or adding to an existing matter.

-   When legal request is promoted by creating a new matter, the Privileged and Confidential status of the created matter is dependent on the Privileged and Confidential status of the request. You can change the status later.
-   When legal request is promoted by adding to an existing matter, the Privileged and Confidential status of the existing matter is retained irrespective of the Privileged and Confidential status of the request.

The Privileged and Confidential status of a legal request and its associated matter are tracked independently. Changing the Privileged and Confidential status of a request does not automatically change the Privileged and Confidential status of the associated matter, and vice versa.

**Related topics**  


[Work on a legal matter](../task/work-on-legal-matter-1.md)

[Disable attorney client privilege for legal matter](../task/lmm-acp-disable.md)

