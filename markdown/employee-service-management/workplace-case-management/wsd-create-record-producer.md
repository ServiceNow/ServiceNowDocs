---
title: Configure a Record producer
description: Make a Workplace service available to employees as a self-service option. Configure a record producer to display the service as a catalog item in the Workplace Services catalog.
locale: en-US
release: zurich
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2025-07-31"
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
    To learn more about the different types of variables and how to configure them, see [Types of service catalog variables](https://www.servicenow.com/docs/access?context=r_VariableTypes&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) Types of service catalog variables.

7.  Select **Submit**.


## Result

The record producer is created.

## What to do next

Link the record producer to the workplace service, see [Create a Workplace service](create-workplace-service.md).

**Parent Topic:**[Configuring Workplace Case Management](../concept/workplace-case-mgmt-setup.md)

**Related topics**  


[Install Workplace Case Management](install-workplace-case-mgmt.md)

[Create a Workplace case template](wsd-case-template.md)

[Create a Workplace task template](wsd-task-template.md)

[Smart Assessment for Workplace Case and Task](smart-assessment-for-workplace-case-and-task.md)

[Automating seat assignment for new hires](../concept/auto-assign-new-hires.md)

[Configure Approval options](config-approval-optns.md)

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

