---
title: Configure Approval options
description: Add approvers to approve cases created through Workplace services.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-case-management/config-approval-optns.html
release: australia
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Configure Approval options

Add approvers to approve cases created through Workplace services.

## Before you begin

**Warning:** Starting with Workplace Case Management version 1.8.2, the option to configure approval options has been moved to the core application Workplace Core version 2.9.2. To create or view approval options, navigate to **Workplace Core** &gt; **Administration** &gt; **Performer Criteria**.

-   After the upgrade, the existing approvers are migrated from the Approval Option \[sn\_wsd\_case\_approval\_option\] table in the Workplace Case Management to the Workplace Performer Criteria \[sn\_wsd\_core\_performer\_criteria\] table in Workplace Core.
-   The **Workplace Performer Criteria** has the same functionality as the Workplace Case Management **Approval** option. In addition, you can configure static approvers using the User criteria.

Ensure that you have the following details:

-   Workplace Case table.
-   User fields to select an approver from.

Role required: sn\_wsd\_case.admin or sn\_wsd\_case.manager

## About this task

The ServiceNow® Workplace Case Management application provides the following default Approval options:

-   **Manager**
-   **Workplace location managed by**
-   **Workplace location managed by group**

## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Workplace Case Management - Setup** &gt; **Approval options**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the Approval option.|
    |Case table|Case table for the option. Select the Workplace Case \[sn\_wsd\_case\_workplace\_case\] table.|
    |User field|User or a user group to set as approver.|
    |Application|Application for the option. This field is automatically set. Make sure the application is set to **Workplace Case Management**.|
    |Active|Option to activate the approval option. Select this option.|

4.  Click **Submit**.


## Result

The Approval option is added and will be listed wherever approvals are configured.

**Parent Topic:**[Configuring Workplace Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-case-management/workplace-case-mgmt-setup.md)

**Related topics**  


[Install Workplace Case Management]()

[Create a Workplace case template]()

[Create a Workplace task template]()

[Smart Assessment for Workplace Case and Task]()

[Automating seat assignment for new hires]()

[Configure a Record producer]()

[Configuring a record producer for request edit]()

[Configuring a record producer for reservation]()

[Create an SLA Definition]()

[Create a Workplace service]()

[Add a workplace service item to a workplace service]()

[Create a workplace template configuration]()

[Create a workplace field mapping]()

[Configure an escalation rule]()

[Add Fulfillment instructions]()

[Group similar workplace cases under a parent case]()

