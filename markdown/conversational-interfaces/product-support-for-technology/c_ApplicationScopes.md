---
title: Application scopes
description: To upload and distribute custom applications on the ServiceNow Store, you need to create a private scope for your applications.
locale: en-US
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: concept
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Installing Proactive Triggers, Proactive Triggers, Manage people and work, Conversational Interfaces]
---

# Application scopes

To upload and distribute custom applications on the ServiceNow Store, you need to create a private scope for your applications.

All applications have an application scope that determines which of its resources are available to other parts of the system. Application scoping ensures that one application does not impact another application. You specify what parts of an application other applications can access by setting application access controls.

For example, if you create a conference room booking application in its own application scope, by default, the application can access and change its own tables and business logic, but other applications such as Incident Management cannot make changes to it without explicit permission.

An application scope ensures that:

-   The conference room booking application does not interrupt core business services.
-   Other applications do not interfere with its normal functioning.

Application scope is available for new and upgraded instances starting with the Fuji release.

