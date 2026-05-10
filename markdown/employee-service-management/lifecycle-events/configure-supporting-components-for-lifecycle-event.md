---
title: Configure the supporting components for a lifecycle event
description: Configure the supporting components for a lifecycle event. Lifecycle events are a collection of activities. For each activity, you must identify and configure the underlying components that support it, such as HR task templates, order guides, catalog items, and HR services. You must also identify and configure the relevant owning groups, activity types, and audience records.
locale: en-US
release: australia
product: Lifecycle Events
classification: lifecycle-events
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Building a lifecycle event, Using Lifecycle Events, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Configure the supporting components for a lifecycle event

Configure the supporting components for a lifecycle event. Lifecycle events are a collection of activities. For each activity, you must identify and configure the underlying components that support it, such as HR task templates, order guides, catalog items, and HR services. You must also identify and configure the relevant owning groups, activity types, and audience records.

-   Owning groups
-   Activity types
-   Audiences

## Owning groups

Owning groups control who owns a lifecycle event activity. Because lifecycle events are generally cross-departmental, it's critical that ownership of each activity is assigned to the appropriate group, such as for HR, IT, or Facilities. Each owning group is responsible for overseeing the activities that fall under their purview. See [Configure an owning group for a lifecycle event](../task/configure-lifecycle-event-owning-group.md) for more information.

To create, update, or delete an activity, you must be both a member of the associated owning group and have the sn\_hr\_le.activity\_writer role. For example, only members of the HR activity writers owning group with the sn\_hr\_le.activity\_writer role can configure an HR activity.

## Activity types

Lifecycle event activities can be approvals, employee activities, fulfiller activities, notifications, and more. Depending on the activity type, you must configure the appropriate components that underlie it.

A key benefit of the Enterprise Onboarding and Transitions application is that you can reuse existing components and processes. These components and processes include existing HR services, HR task templates, or catalog items. For each activity, determine whether there’s an existing component that you can use or if you must configure a new one.

<table id="table_uqp_53t_vgb"><thead><tr><th>

Activity type

</th><th colspan="2">

Configuration requirements

</th></tr></thead><tbody><tr><td>

Approval

</td><td colspan="2">

N/A

 To learn more about approvals, see [Approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/approvals/r_Approvals.md).

</td></tr><tr><td>

Employee task

</td><td colspan="2">

[Configure an HR task template](../task/configure-hr-task-template.md) To learn more about HR templates, see [HR templates](hr-template-configuration.md).

</td></tr><tr><td rowspan="6">

Fulfiller activity

</td><td colspan="2">

Depending on the fulfiller activity type, configure the appropriate supporting components.**Note:** The following fulfiller activity types are preconfigured with the Enterprise Onboarding and Transitions application. To configure additional types, see [Configure an activity configuration for a lifecycle event](../task/configure-lifecycle-event-fulfiller-activity-configuration.md).

</td></tr><tr><td>

Automated Order Guide

</td><td>

[Create an order guide](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/t_CreateAnOrderGuide.md) To learn more about order guides, see [Order guides](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/c_ServiceCatalogOrderGuides.md).

</td></tr><tr><td>

Catalog item

</td><td>

[Create or edit a catalog item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/t_DefineACatalogItem.md) To learn more about catalog items, see [Service catalog items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/c_IntroductionToCatalogItems.md).

</td></tr><tr><td>

HR service

</td><td>

[Configure an HR service](../task/configure-hr-service.md) To learn more about HR services, see [HR services](hr-service-administration.md).

</td></tr><tr><td>

HR task

</td><td>

[Configure an HR task template](../task/configure-hr-task-template.md) To learn more about HR templates, see [HR templates](hr-template-configuration.md).

</td></tr><tr><td>

Incident

</td><td>

[Create an incident template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-management/t_CreateAnIncidentTemplate.md) To learn more about incident management, see [Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-management/c_IncidentManagement.md).

</td></tr><tr><td>

Notification

</td><td colspan="2">

[Create an email template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateAnEmailTemplate.md) To learn more about notifications, see [Notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/notifications.md).

</td></tr><tr><td>

Flow

</td><td colspan="2">

[Create a subflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-subflow.md) **Important:** The only subflow available for use by default is the **Switch primary job** subflow. This subflow is used to [support multiple jobs in a lifecycle event](../task/adopt-jobs-table.md).

To use a different subflow for an activity, additional configuration is required. See the [Implementing multiple subflows in an LE activity \[KB0817520\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0817520) article in the HI knowledge base for more information.

 To learn more about subflows, see [Subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/subflows.md).

</td></tr><tr><td>

Content

</td><td colspan="2">

[Configure a schedule content template for a lifecycle event activity](../task/configure-schedule-content-template-for-lifecycle-event.md) To learn more about Content Experiences and Content Publishing, see [Content Publishing](../../employee-center/concept/ec-publish-content.md).

</td></tr><tr><td>

Activity container

</td><td colspan="2">

N/A

</td></tr></tbody>
</table>## Audiences

Not all lifecycle event activities are required for all employees. Some activities are intended for a target audience. You can use audience records to define the criteria that the subject person of a lifecycle event case must meet for the activity to trigger on their behalf. For more information, see [Audiences](../../employee-center/concept/ecpro-audience.md).

Clearly defined audience criteria enable you to create targeted workflows for different audience types. For example, you can create a tailored onboarding experience for newly hired employees depending on whether the employee is office-based or remote.

**Note:**

-   If an activity isn't associated with an audience record, then the activity triggers for all employees.
-   If a subject person doesn't meet the audience criteria defined for an activity set during the evaluation process, the **State** field in the corresponding activity set is set to **Skipped**.

-   **[Configure an owning group for a lifecycle event](../task/configure-lifecycle-event-owning-group.md)**  
Create or modify an owning group to define the user group that owns a lifecycle event activity. Each owning group is responsible for overseeing the activities that fall under their purview.
-   **[Configure an activity configuration for a lifecycle event](../task/configure-lifecycle-event-fulfiller-activity-configuration.md)**  
Create or modify an activity configuration to define the fulfillment process and conditions for closure for a lifecycle event activity.
-   **[Configure a schedule content template for a lifecycle event activity](../task/configure-schedule-content-template-for-lifecycle-event.md)**  
Create or modify a schedule content template to deliver content as part of a lifecycle event. Each template must be associated with the Schedule Content \[sn\_cd\_content\_visibility\] table, and you can configure the template for mobile content, portal content, notification content, or to-do content.

**Parent Topic:**[Building a lifecycle event](hr-lifecycle-event-configuration.md)

**Previous topic:**[Document the lifecycle event process](define-lifecycle-event-process.md)

**Next topic:**[Configure an owning group for a lifecycle event](../task/configure-lifecycle-event-owning-group.md)

