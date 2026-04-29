---
title: Configure Approval options
description: Add approvers to approve cases created through Workplace services.
locale: en-US
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

**Parent Topic:**[Configuring Workplace Case Management](../concept/workplace-case-mgmt-setup.md)

**Related topics**  


[Install Workplace Case Management](install-workplace-case-mgmt.md)

[Create a Workplace case template](wsd-case-template.md)

[Create a Workplace task template](wsd-task-template.md)

[Smart Assessment for Workplace Case and Task](smart-assessment-for-workplace-case-and-task.md)

[Automating seat assignment for new hires](../concept/auto-assign-new-hires.md)

[Configure a Record producer](wsd-create-record-producer.md)

[Configuring a record producer for request edit](../concept/config-case-edit-rp.md)

[Configuring a record producer for reservation](../concept/config-reservation-rp.md)

[Create an SLA Definition](create-sla-defn-case-mgmt.md)

[Create a Workplace service](create-workplace-service.md)

[Add a workplace service item to a workplace service](add-workplace-service-items.md)

[Create a workplace template configuration](create-workplace-template-confguration.md)

[Create a workplace field mapping](create-workplace-field-mapping.md)

[Configure an escalation rule](configure-escalation-rule.md)

[Add Fulfillment instructions](add-fulfillment-instructions.md)

[Group similar workplace cases under a parent case](group-similar-workplace-cases.md)

