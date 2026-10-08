---
title: Multi-Instance Setup
description: Multi-Instance Setup discovers non-production instances related to a production instance and connects instances to support cross-instance communication and data sharing with various ServiceNow applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/multi-instance-setup-overview.html
release: brazil
topic_type: concept
last_updated: "2026-09-18"
reading_time_minutes: 2
keywords: [Multi-Instance Setup, controller, non-production instance, AMF Core, Multi-Instance Framework]
breadcrumb: [Multi-Instance Management, Get started, Administer the ServiceNow AI Platform]
---

# Multi-Instance Setup

Multi-Instance Setup discovers non-production instances related to a production instance and connects instances to support cross-instance communication and data sharing with various ServiceNow applications.

Cross-instance communication is important for secure data exchange, synchronization, and collaboration between instances and is required to promote and govern applications across environments. Multi-Instance Setup simplifies setting up cross-instance communication with a single user interface where administrators can configure and monitor non-production instances connected to a controller. Every connection is requested, reviewed, and approved or rejected to help avoid silent failures or undocumented instance relationships.

\[Omitted image "multi-instance-setup-ui.png"\] Alt text: Managed Instances list in Multi-Instance Setup showing managed instances with environment types, approval statuses, and required actions.

## Multi-Instance Setup and Multi-Instance Management

Multi-Instance Setup is built on Multi-Instance Management and simplifies the process of connecting instances but there are some distinctions between the two features:

-   Multi-Instance Management is the ServiceNow AI Platform framework that establishes trust between individual instances at the level of a specific application or capability. Configuring Multi-Instance Management trust directly means working with manager and managed instance relationships one application at a time.
-   Multi-Instance Setup manages the relationship between a controller and its non-production instances at the environment level, rather than configuring trust per application and capability. Multi-Instance Setup automatically maintains the underlying Multi-Instance Management trust relationships that individual applications rely on. Other ServiceNow applications that need cross-instance trust automatically manage their own per-capability trust profiles.

    Multi-Instance Setup also adds environment types on top of the Multi-Instance Management framework, which only distinguishes non-production instances from production instances.


## Multi-Instance Setup workflow

From Multi-Instance Setup, administrators can configure cross-instance communication in a few steps:

1.  From the production instance, the instance admin sets the instance as the controller.
2.  To add non-production instances to the controller, the admin chooses to run a scan that automatically discovers non-production instances or adds them manually and assigns each one an environment type.

    Multi-Instance Setup automatically sends an access request to each non-production instance's administrator.

3.  From a non-production instance, the admin of that instance approves or denies the request to manage the instance from the controller.

    After the admin approves the request, cross-instance communication between the controller and that non-production instance is active.


For more information about using Multi-Instance Setup, see [Connecting controller and managed instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/connecting-controller-managed-instances.md).

**Related topics**  


[Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/sandboxes-landing.md)

[App Engine Management Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/app-engine-management-center.md)

