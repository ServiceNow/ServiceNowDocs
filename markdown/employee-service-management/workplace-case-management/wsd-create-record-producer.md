---
title: Configure a Record producer
description: Make a Workplace service available to employees as a self-service option. Configure a record producer to display the service as a catalog item in the Workplace Services catalog.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-case-management/wsd-create-record-producer.html
release: australia
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Configure a Record producer

Make a Workplace service available to employees as a self-service option. Configure a record producer to display the service as a catalog item in the Workplace Services catalog.

## Before you begin

Role required: sn\_wsd\_case.admin or sn\_wsd\_case.manager

## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Workplace Case Management - Setup** &gt; **Record producers**

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_ryz_lt3_smb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the record producer.

</td></tr><tr><td>

Table name

</td><td>

Workplace Case \(sn\_wsd\_case\_workplace\_case\) table that the record producer is associated with. **Note:** Make sure that the workplace case table for the record producer matches that of the associated workplace service.

</td></tr><tr><td>

Model

</td><td>

Product model table if relevant for the record producer.

</td></tr><tr><td>

Application

</td><td>

This field is already set to `Workplace Case Management`.

</td></tr><tr><td>

Active

</td><td>

Option to activate the record producer for use.

</td></tr><tr><td>

Preview link

</td><td>

Link to preview how the record producer appears to users in the Workplace Service Delivery catalog

</td></tr><tr><td>

Expand help for all questions

</td><td>

Select this option to enable users to expand help for all questions.

</td></tr></tbody>
</table>4.  Fill the following related lists fields appropriately:

    -   **What it will contain**
    -   **Accessibility**
    -   **Generated Record Data**
    -   **Portal Settings**
5.  In the **What it will contain** related list, provide the following script:

    ```
    new sn_wsd_case.WSDServiceUtils(current, gs).createCaseFromProducer(producer, cat_item.sys_id);
    ```

6.  In the **Variables** related list, configure the variables for the Workplace Services catalog item as appropriate.

    Variables collect information from the user, and are used to ask questions and map answers to fields. You can add as many variables as you need to the Workplace Services catalog item. Commonly used variables types include:

    -   Checkbox
    -   Multiple Choice
    -   Reference
    -   Select Box
    -   Single Line Text
    To learn more about the different types of variables and how to configure them, see [Types of service catalog variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/r_VariableTypes.md) Types of service catalog variables.

7.  Select **Submit**.


## Result

The record producer is created.

## What to do next

Link the record producer to the workplace service, see [Create a Workplace service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-case-management/create-workplace-service.md).

**Parent Topic:**[Configuring Workplace Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-case-management/workplace-case-mgmt-setup.md)

**Related topics**  


[Install Workplace Case Management]()

[Create a Workplace case template]()

[Create a Workplace task template]()

[Smart Assessment for Workplace Case and Task]()

[Automating seat assignment for new hires]()

[Configure Approval options]()

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

