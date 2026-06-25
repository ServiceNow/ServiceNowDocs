---
title: Building a lifecycle event
description: Lifecycle events enable you to automate the fulfillment of HR cases such as new hire onboarding.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/lifecycle-events/hr-lifecycle-event-configuration.html
release: australia
product: Lifecycle Events
classification: lifecycle-events
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Lifecycle Events, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Building a lifecycle event

Lifecycle events enable you to automate the fulfillment of HR cases such as new hire onboarding.

Each lifecycle event is a collection of activities that often span multiple departments and are organized into activity sets. To configure a lifecycle event, you must first document the business process for your event. Next, you must configure all of the supporting components. You can then configure the lifecycle event and its associated activity sets and activities. Finally, you configure a corresponding HR service so that the lifecycle event can be requested for service.

**Note:** If you are further customizing an existing lifecycle event, follow the configuration tasks as applicable.

1.  [Document the lifecycle event process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/lifecycle-events/define-lifecycle-event-process.md)  
Define and document the lifecycle event process. Lifecycle events are generally cross-departmental and require action from different departments.
2.  [Configure the supporting components for a lifecycle event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/lifecycle-events/configure-supporting-components-for-lifecycle-event.md)  
Configure the supporting components for a lifecycle event. Lifecycle events are a collection of activities. For each activity, you must identify and configure the underlying components that support it, such as HR task templates, order guides, catalog items, and HR services. You must also identify and configure the relevant owning groups, activity types, and audience records.
3.  [Configure a lifecycle event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/lifecycle-events/configure-hr-lifecycle-event-type.md)  
Build a lifecycle event and its associated activity sets and activities with the lifecycle event builder.
4.  [Configure an HR service for a lifecycle event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/lifecycle-events/create-hr-service-for-lifecycle-event.md)  
Create a corresponding HR service so that the lifecycle event can be requested for service. For example, the lifecycle event for New Hire Onboarding has a corresponding HR service also named New Hire Onboarding. When an HR case for that HR service is created, the HR case will be fulfilled by the associated lifecycle event.
5.  [Configure an HR service for a journey](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/lifecycle-events/configure-hr-service-for-journey.md)  
Create a corresponding HR service so that the lifecycle event can be requested for service as part of an employee's journey.
6.  [Using the Test Activity Sets tool for a lifecycle event activity set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/lifecycle-events/hr-lifecycle-event-test-tool.md)  
Use the lifecycle event test tool to thoroughly test a lifecycle event before launching it.
7.  [Select a Lifecycle Event for Now Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/lifecycle-events/select-lifecycle-event-for-mobile-onboarding.md)  
Select the Lifecycle Event that you want to use with Now Mobile. When an onboarding case for that event type is created, the new hire completes the to-dos that are associated with that case.

**Parent Topic:**[Using Lifecycle Events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/lifecycle-events/using-lifecycle-events.md)

**Related topics**  


[Lifecycle Events employee requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/lifecycle-events/employee-requests.md)

[Clone a lifecycle event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/lifecycle-events/clone-lifecycle-event.md)

[Filter lifecycle event activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/lifecycle-events/filter-lifecycle-event-activities.md)

[Lifecycle event properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/lifecycle-events/lifecycle-event-properties-page.md)

[Support multiple jobs in a lifecycle event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/lifecycle-events/adopt-jobs-table.md)

[Configure the UI of the lifecycle event builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/lifecycle-events/le-ui-configuration.md)

[Create an HR case for a lifecycle event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/lifecycle-events/create-hr-lifecycle-event-case.md)

