---
title: Select a Lifecycle Event for Now Mobile
description: Select the Lifecycle Event that you want to use with Now Mobile. When an onboarding case for that event type is created, the new hire completes the to-dos that are associated with that case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/lifecycle-events/select-lifecycle-event-for-mobile-onboarding.html
release: zurich
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Building a lifecycle event, Use, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Select a Lifecycle Event for Now Mobile

Select the Lifecycle Event that you want to use with Now Mobile. When an onboarding case for that event type is created, the new hire completes the to-dos that are associated with that case.

## Before you begin

Role required: sn\_hr\_le.admin

You must also make sure that the **Display activity sets to subject person** option is selected, as well as the **Show case to subject person** option on the corresponding HR service.

A Lifecycle Event administrator must have set up the Lifecycle Event and the corresponding HR service you want to use with Now Mobile. See [Building a lifecycle event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/lifecycle-events/hr-lifecycle-event-configuration.md) for more information.

## Procedure

1.  Select the Lifecycle Event you want to use with Now Mobile.

    Also make sure that the **Display activity sets to subject person** option is selected.

    1.  Navigate to **Lifecycle Events** &gt; **Administration** &gt; **Manage Lifecycle Events**.

    2.  Open the Lifecycle Event record.

        **Note:** A preconfigured Lifecycle Event named New Hire Onboarding is available to use.

    3.  On the Lifecycle Event form, set the **Event type** field to `Onboarding`.

        \[Omitted image "mobile-onboarding-le-event-type-2.png"\] Alt text: Set the Event type field to Onboarding.

    4.  Make sure that the **Display activity sets to subject person** option is selected.

        \[Omitted image "mobile-onboarding-le-checkbox-2.png"\] Alt text: Select the Display activity sets to subject person option.

2.  On the corresponding HR service form, make sure that the **Show case to subject person** option is selected.

    1.  Navigate to **HR Administration** &gt; **HR Services** &gt; **HR Service Configuration**.

    2.  Open the corresponding HR service record.

        **Note:** A preconfigured HR service named New Hire Onboarding is available to use.

    3.  Make sure that the **Show case to subject person** option is selected.

        \[Omitted image "mobile-onboarding-hr-service-2.png"\] Alt text: Select the Show case to subject person option.


**Parent Topic:**[Building a lifecycle event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/lifecycle-events/hr-lifecycle-event-configuration.md)

**Previous topic:**[Preview and test a lifecycle event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/lifecycle-events/test-lifecycle-event.md)

**Next topic:**[Lifecycle Events employee requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/lifecycle-events/employee-requests.md)

