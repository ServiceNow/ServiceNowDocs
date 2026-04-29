---
title: Attorney-Client Privilege
description: Attorney Client Privilege functionality enables legal fulfiller to designate legal requests as privileged and confidential. It restricts access to authorized stakeholders, marks communications with confidentiality banners, and maintains a document audit trail to help you protect sensitive legal communications.
locale: en-US
release: australia
product: Legal Request Management
classification: legal-request-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [ACP, Attorney client privilege, Privileged and confidential]
breadcrumb: [Explore, Legal Request Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Attorney-Client Privilege

Attorney Client Privilege functionality enables legal fulfiller to designate legal requests as privileged and confidential. It restricts access to authorized stakeholders, marks communications with confidentiality banners, and maintains a document audit trail to help you protect sensitive legal communications.

Attorney Client Privilege applies to following:

-   Legal Request: Legal fulfillers can mark legal requests as privileged and confidential, when the request is in Assigned or Work in Progress state. The system enforces access control, adds confidentiality markers to emails, and restricts collaboration to authorized stakeholders.
-   Legal Matter: Legal fulfillers and matter owners can independently mark or unmark individual matters as privileged and confidential, provided the matter is in the Assigned or Work in Progress state.

The Attorney Client Privilege feature is not available for legal contracts requests. Example: Non-disclosure Agreement \(NDA\) and Third-party Contracts submitted using Contract Management Pro for Legal Service Delivery application.

## Assignment group permission changes

When Privilege and Confidential is enabled on a legal request, the system automatically updates the assignment group permission to No access.

## Indicators of a privileged and confidential marked request

You can identify a privileged and confidential request by following UI elements.

-   Privileged and Confidential flag: Displayed in the secondary header of the request when it is marked as privileged and confidential.
-   Privileged document access related list to display the permission of each attachment.

![Identify privileged and confidential request](../image/lsd-acp-indicators.png)

## Email notifications

Email notifications generated for Privileged and Confidential marked requests, contain confidentiality markers to comply with legal requirements. This applies to both system-generated notifications and fulfiller-initiated outbound emails.

## Stakeholder change notifications

When the collaborator list, watchlist, or fulfiller assignment is modified for a privileged and confidential request, the system sends email notifications to the requester, fulfiller, and collaborators. Notifications are triggered when:

-   A new collaborator is added to the request.
-   A new watchlist entry is added.
-   The fulfiller assignment changes.

All notifications for privileged and confidential requests include the confidentiality markers.

## Promote legal request to legal matter

You can promote a legal request to legal matter by creating a new matter or adding to an existing matter.

-   When legal request is promoted by creating a new matter, the Privileged and Confidential status of the created matter is dependent on the Privileged and Confidential status of the request. You can change the status later.
-   When legal request is promoted by adding to an existing matter, the Privileged and Confidential status of the existing matter is retained irrespective of the Privileged and Confidential status of the request.

The Privileged and Confidential status of a legal request and its associated matter are tracked independently. Changing the Privileged and Confidential status of a request does not automatically change the Privileged and Confidential status of the associated matter, and vice versa.

**Parent Topic:**[Exploring Legal Request Management](legal-request-management-overview.md)

**Related topics**  


[Work on a legal request](../task/work-on-legal-request.md)

[Disable attorney client privilege for a legal request](lsd-acp-enable.md)

[Manage attachments for a legal request](../task/manage-attachments-legal-request.md)

[Transfer a legal request](../task/transfer-existing-legal-request.md)

