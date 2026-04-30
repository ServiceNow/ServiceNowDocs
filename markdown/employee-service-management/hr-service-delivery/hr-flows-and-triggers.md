---
title: HR flows and triggers
description: HR flows created in Workflow Studio use natural language to automate approvals, tasks, notifications, and record operations without coding.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [HR Administration, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# HR flows and triggers

HR flows created in Workflow Studio use natural language to automate approvals, tasks, notifications, and record operations without coding.

Three new flows are available to automate the triggering of Lifecycle Events. The triggers are based on changes in the HR Profile \[sn\_hr\_core\_profile\] or Job \[sn\_hr\_core\_job\] tables. These flows reduce or eliminate the need to write business rules to trigger Lifecycle Events.

**Note:** Customize these flows to use in other Lifecycle Events other than on boarding events.

The following flows are installed with the Human Resources: Core application. These HR flows are deactivated by default.

-   **New Hire on Boarding Case Trigger HR Profile**

    The trigger is based on the employee's start date in the HR Profile Table \[sn\_hr\_core\_profile\]. If the employment start date is at or after today, the flow creates an HR Onboarding case. This flow runs every time an HR profile is created or updated.

    For more information about the HR Profile, see [Employee Profile table](employee-profile.md) and [HR Profile](c_HRProfileRecords.md).

-   **New Hire on Boarding Case Trigger Job**

    The trigger is based on the employee's start date in the Job Table \[sn\_hr\_core\_job\]. If the employment start date is at or after today, the flow creates an HR Onboarding case. This flow runs every time an HR profile is created or updated.

    For more information about the Job Table and related profile records, see [Capturing multiple job records for a user](support-hr-users-with-multiple-jobs.md).

-   **Case Trigger Custom Condition**

    Table: HR Profile \[sn\_hr\_core\_profile\]

    This flow can be used as a template to create a customized trigger. The trigger is based on a custom date check for the employee start date. The default trigger is initiated two days prior to the employee start date. For more information about flows and triggers, see [Flows](https://www.servicenow.com/docs/access?context=flows&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).


These flows create an HR case adding an entry in the HR Lifecycle Events Case \[sn\_hr\_le\_case\] table. If multiple flows are active at the same time, there is a high probability of creating duplicate records and cases.

**Note:** Only one of these flows should be active at any given time for a particular lifecycle event.

-   **[Activate an HR flow](../task/activate-hr-flow.md)**  
HR flows help automate task and case creation.

**Parent Topic:**[HR Administration](c_AdministerHRServiceManagement.md)

