---
title: Understanding Lifecyle events for enterprise
description: Use Lifecyle events for enterprise to automate the fulfillment of employee lifecycle events such as new hire onboarding, offboarding, relocation, promotion, parental leave, and more. Lifecycle events are a collection of activities organized into activity sets to comprise an employee experience.
locale: en-US
release: zurich
product: Employee Journey Management
classification: employee-journey-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Lifecyle events for enterprise, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Understanding Lifecyle events for enterprise

Use Lifecyle events for enterprise to automate the fulfillment of employee lifecycle events such as new hire onboarding, offboarding, relocation, promotion, parental leave, and more. Lifecycle events are a collection of activities organized into activity sets to comprise an employee experience.

## Lifecyle events for enterprise Overview

Lifecyle events for enterprise enables organizations to easily automate employee experiences and processes that span multiple departments, offering the following benefits.

-   Easily snap together experiences and processes to automate cross-departmental work
-   Drive action across multiple departments and systems for improved efficiency
-   Provide end-to-end visibility on each process to ensure that correct actions are taken
-   Guide employees step-by-step so that they know what to do next
-   Continually optimize the process with insight from lifecycle event dashboards

The following video provides an overview of the Lifecyle events for enterprise application.

This video provides an overview of the Lifecyle events for enterprise application.

## Activation information

Beginning in the Orlando release, Lifecyle events for enterprise is comprised of two plugins. Depending on the HR Service Delivery package you choose, activate one or both of the plugins.

<table id="table_hnj_hcp_3jb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Lifecycle Events \[com.sn\_hr\_lifecycle\_events\]

</td><td>

Enables you to easily configure digital workflows to manage employee lifecycle events within HR. See [Activate Lifecycle Events](../task/activate-enterprise-onboarding-and-transitions-scoped.md) for more information.

</td></tr><tr><td>

Lifecycle Events for Enterprise\[com.sn\_hr\_lifecycle\_ent\]

</td><td>

Enables you to automate onboarding and other employee lifecycle events that span across multiple departments such as HR, IT, Facilities, Finance, and Legal through a single service delivery platform. See [Activate Lifecycle Events for Enterprise](../task/activate-hr-lifecycle-events-for-enterprise-1.md) for more information.**Note:** The lifecycle event for new hire onboarding is included as demo data with the Lifecycle Events for Enterprise \[com.sn\_hr\_lifecycle\_ent\] plugin.

</td></tr></tbody>
</table>## Configuring Lifecyle events for enterprise

Depending on your role, you can access and configure the following:

-   **Lifecycle event administrator**

    Users with the lifecycle event administrator \[sn\_hr\_le.admin\] role can administer and configure any part of the application, including any lifecycle event and its associated activity sets and activities. For more information, see [Building a lifecycle event](hr-lifecycle-event-configuration.md).

-   **Activity set manager**

    Users with the activity set manager \[sn\_hr\_le.activity\_set\_manager\] role can build any lifecycle event and the associated activity sets. You can configure any lifecycle event activity, so long as you are a member of the owning group that owns the activity. For example, if you are a member of the HR owning group, then you can configure any activity that is owned by the HR group, such as an employee task to watch an onboarding video or a fulfiller task to provide relocation assistance.

    -   [Configure a lifecycle event](../task/configure-hr-lifecycle-event-type.md) and the associated activity sets
    -   [Configure a lifecycle event activity](../task/configure-hr-lifecycle-event-activity.md#) if you are a member of the associated owning group
-   **Activity writer**

    Users with the activity writer \[sn\_hr\_le.activity\_writer\] role can configure any lifecycle event activity, so long as you are a member of the owning group that owns the activity. For example, if you are a member of the IT owning group, then you can configure any activity that is owned by the IT group, such as to set up an active directory account or to set up equipment for a new employee. For more information, see [Configure a lifecycle event activity](../task/configure-hr-lifecycle-event-activity.md#) if you are a member of the associated owning group.

-   **Activity reader**

    Users with the activity reader \[sn\_hr\_le.activity\_reader\] role can read any lifecycle event and its associated activity sets and activities.


## Using Lifecyle events for enterprise

Once the Lifecyle events for enterprise application is configured, users with the following roles can write and read lifecycle event cases.

**Note:** A lifecycle event case is an HR case that is fulfilled by a lifecycle event.

-   **Lifecycle event case writer**

    Users with the lifecycle event case writer \[sn\_hr\_le.case\_writer\] role can create, manage, and monitor the status of any lifecycle event case.

    -   [Create an HR case for a lifecycle event](../task/create-hr-lifecycle-event-case.md)
    -   [Monitor the status of a lifecycle event case](../task/t_BundleExContexts.md)
-   **Lifecycle event case reader**

    Users with the lifecycle event case reader \[sn\_hr\_le.case\_reader\] role can read any lifecycle event case.


