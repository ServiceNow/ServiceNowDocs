---
title: Create a Workplace task template
description: A Task template simplifies the process of creating tasks in Workplace Case Management by populating fields automatically.
locale: en-US
release: yokohama
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Create a Workplace task template

A Task template simplifies the process of creating tasks in Workplace Case Management by populating fields automatically.

## Before you begin

Role required: sn\_wsd\_case.admin or sn\_wsd\_case.manager

## About this task

Create a task template for use when creating a workplace service.

**Note:** Administrators may use task assignment rules to control the automatic assignment of workplace tasks as long as the task template is not already assigning a person or group to the task. For more information on assignment rules, see [Define assignment rules](https://www.servicenow.com/docs/access?context=c_DefineAssignmentRules&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Workplace Case Management - Setup** &gt; **Task templates**.

2.  Create a template or modify an existing template.

    -   If you are creating a template, click **New**.
    -   If you are modifying an existing template, open that template.
    For information about the template form fields, see [Create a template](https://www.servicenow.com/docs/access?context=t_CreateATemplateUsingTheTmplForm&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

3.  In the **Table** field, select the **Workplace Task \[sn\_wsd\_core\_workplace\_task\]** table.

4.  Click **Submit**.


## Result

The task template is created. You can use this template for Workplace services.

**Parent Topic:**[Configure Workplace Case Management](../concept/workplace-case-mgmt-setup.md)

**Related topics**  


[Install Workplace Case Management](install-workplace-case-mgmt.md)

[Create a Workplace case template](wsd-case-template.md)

[Configure Approval options](config-approval-optns.md)

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

