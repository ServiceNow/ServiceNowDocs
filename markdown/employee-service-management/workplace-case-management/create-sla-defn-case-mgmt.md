---
title: Create an SLA Definition
description: Configure SLAs to ensure that cases are resolved according to the expectations of customers. SLAs set up performance parameters, such as specifying minimum uptime or the amount of time that a task needs in order to reach a certain condition. 
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-case-management/create-sla-defn-case-mgmt.html
release: australia
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Create an SLA Definition

Configure SLAs to ensure that cases are resolved according to the expectations of customers. SLAs set up performance parameters, such as specifying minimum uptime or the amount of time that a task needs in order to reach a certain condition. 

## Before you begin

Role required: sn\_wsd\_case.admin or sn\_wsd\_case.manager

## About this task

Create an SLA definition and use it in Workplace cases. An SLA definition record defines the timings, conditions, workflows, and other information required to create and progress task SLAs. For more information, refer to [Service Level Agreement \(SLA\) definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/c_SLADefinitions.md).

## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Workplace Case Management - Setup** &gt; **SLA Definitions**.

2.  Create an SLA Definition or modify an existing one.

    -   If you are creating an SLA Definition, click **New**.
    -   If you are modifying an existing SLA Definition, open the desired SLA Definition.
    For information about the template form fields, see [Create an SLA Defintion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/t_CreateAnSLADefinition.md).

3.  In the **Table** field, select the **Workplace Case \[sn\_wsd\_case\_workplace\_case\]** table.

4.  In the **Flow** field, select **Default SLA flow**.

5.  In the Application field, ensure **Workplace Case Management** is selected.

6.  Click **Submit**.


## Result

The SLA Definition is created.

**Parent Topic:**[Configuring Workplace Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-case-management/workplace-case-mgmt-setup.md)

**Related topics**  


[Install Workplace Case Management]()

[Create a Workplace case template]()

[Create a Workplace task template]()

[Smart Assessment for Workplace Case and Task]()

[Automating seat assignment for new hires]()

[Configure Approval options]()

[Configure a Record producer]()

[Configuring a record producer for request edit]()

[Configuring a record producer for reservation]()

[Create a Workplace service]()

[Add a workplace service item to a workplace service]()

[Create a workplace template configuration]()

[Create a workplace field mapping]()

[Configure an escalation rule]()

[Add Fulfillment instructions]()

[Group similar workplace cases under a parent case]()

