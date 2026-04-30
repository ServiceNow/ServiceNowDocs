---
title: Select a Lifecycle Event for Now Mobile
description: Select the Lifecycle Event that you want to use with Now Mobile. When an onboarding case for that event type is created, the new hire completes the to-dos that are associated with that case.
locale: en-US
release: yokohama
product: HR Service Delivery for mobile
classification: hr-service-delivery-for-mobile
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Administer Now Mobile, HR Service Delivery for mobile, HR Service Delivery, Employee Service Management]
---

# Select a Lifecycle Event for Now Mobile

Select the Lifecycle Event that you want to use with Now Mobile. When an onboarding case for that event type is created, the new hire completes the to-dos that are associated with that case.

## Before you begin

Role required: sn\_hr\_le.admin

You must also make sure that the **Display activity sets to subject person** option is selected, as well as the **Show case to subject person** option on the corresponding HR service.

A Lifecycle Event administrator must have set up the Lifecycle Event and the corresponding HR service you want to use with Now Mobile. See [Building a lifecycle event](../concept/hr-lifecycle-event-configuration.md) for more information.

## Procedure

1.  Select the Lifecycle Event you want to use with Now Mobile.

    Also make sure that the **Display activity sets to subject person** option is selected.

    1.  Navigate to **Lifecycle Events** &gt; **Administration** &gt; **Manage Lifecycle Events**.

    2.  Open the Lifecycle Event record.

        **Note:** A preconfigured Lifecycle Event named New Hire Onboarding is available to use.

    3.  On the Lifecycle Event form, set the **Event type** field to `Onboarding`.

        ![Set the Event type field to Onboarding.](../image/mobile-onboarding-le-form-event-type.png)

    4.  Make sure that the **Display activity sets to subject person** option is selected.

        ![Select the Display activity sets to subject person option.](../image/mobile-onboarding-le-form-checkbox.png)

2.  On the corresponding HR service form, make sure that the **Show case to subject person** option is selected.

    1.  Navigate to **HR Administration** &gt; **HR Services** &gt; **HR Service Configuration**.

    2.  Open the corresponding HR service record.

        **Note:** A preconfigured HR service named New Hire Onboarding is available to use.

    3.  Make sure that the **Show case to subject person** option is selected.

        ![Select the Show case to subject person option.](../image/mobile-onboarding-hr-service-checkbox.png)


**Parent Topic:**[Administer Now Mobile](../concept/administer-mobile-employee-onboarding-for-hr-service-delivery.md)

