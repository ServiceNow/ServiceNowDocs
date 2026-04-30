---
title: CSM Walk-up Experience portal security and access
description: Security is built into the application to help prevent end-user facing devices at the Walk-up Experience onsite portal from offering elevated role privileges to users. The Walk-up Experience onsite portal is accessed by an account containing only the sn\_walkup.walkup\_login role. The sn\_walkup.walkup\_login role contains the snc\_external role.
locale: en-US
release: yokohama
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Walk-up Experience for Customer Service Management, Set up self-service, Configuring Customer Service Management, Customer Service Management]
---

# CSM Walk-up Experience portal security and access

Security is built into the application to help prevent end-user facing devices at the Walk-up Experience onsite portal from offering elevated role privileges to users. The Walk-up Experience onsite portal is accessed by an account containing only the sn\_walkup.walkup\_login role. The sn\_walkup.walkup\_login role contains the snc\_external role.

## Understanding Walk-up Experience portal security

Accessing the onsite Walk-up Experience portal requires the singularly assigned sn\_walkup.walkup\_login role. The user record with this role cannot contain any other roles. Because most user records contain multiple roles, the sn\_walkup.walkup\_login role is assigned to a user record account, not a human user. The security feature helps prevent the onsite portal check-in device from permitting users who might try accessing the portal with an elevated privilege role.

The sn\_walkup.walkup\_login role is granted to a user record for an account used to log in to the check-in device. Typically, the device at the onsite Walk-up Experience portal is a tablet. It is not an actual human being with an assigned role, but an account with a role. For example, a technician opening the onsite Walk-up portal for business logs in to the check-in device using the user record that contains the sn\_walkup.walkup\_login role. Again, the portal can only be accessed by a user record that contains this role only. A user cannot access the portal with the admin role or if the user record contains roles other than the sn\_walkup.walkup\_login role.

## Access to Walk-up Experience

Technicians opening up the onsite Walk-up location for business, or joining the support team during operation hours, access the user record account. Technicians with sn\_walkup.walkup\_login role can log in to the Walk-up Experience portal. Internal and external users can access the onsite Walk-up Experience portal via a check-in device, typically a tablet, to enter a queue. Internal, authenticated users can also access an online queue check-in via desktop.

