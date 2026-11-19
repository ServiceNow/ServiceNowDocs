---
title: Create a Workplace task template
description: A Task template simplifies the process of creating tasks in Workplace Case Management by populating fields automatically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/workplace-case-management/wsd-task-template.html
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

**Note:** Administrators may use task assignment rules to control the automatic assignment of workplace tasks as long as the task template is not already assigning a person or group to the task. For more information on assignment rules, see [Define assignment rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/c_DefineAssignmentRules.md).

## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Workplace Case Management - Setup** &gt; **Task templates**.

2.  Create a template or modify an existing template.

    -   If you are creating a template, click **New**.
    -   If you are modifying an existing template, open that template.
    For information about the template form fields, see [Create a template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/t_CreateATemplateUsingTheTmplForm.md).

3.  In the **Table** field, select the **Workplace Task \[sn\_wsd\_core\_workplace\_task\]** table.

4.  Click **Submit**.


## Result

The task template is created. You can use this template for Workplace services.

**Parent Topic:**[Configure Workplace Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/workplace-case-management/workplace-case-mgmt-setup.md)

**Related topics**  


[Install Workplace Case Management]()

[Create a Workplace case template]()

[Configure Approval options]()

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

