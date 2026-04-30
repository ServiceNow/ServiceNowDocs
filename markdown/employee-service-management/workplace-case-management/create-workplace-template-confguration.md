---
title: Create a workplace template configuration
description: Define a template that must be applied to fulfill a workplace case. Set conditions based on common employee responses for requests. The template will be applied to those workplace cases that match the conditions specified.
locale: en-US
release: yokohama
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Create a workplace template configuration

Define a template that must be applied to fulfill a workplace case. Set conditions based on common employee responses for requests. The template will be applied to those workplace cases that match the conditions specified.

## Before you begin

Role required: admin

## About this task

Create a template and configure the conditions that a workplace case must match so that the template is applied. If the conditions don't match, then the default template that is specified in the workplace service is applied.

A Workplace template configuration can be directly applied to a workplace service or a workplace service activity.

## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Workplace Case Management - Setup** &gt; **Workplace services**.

2.  Select the workplace service to which you want to add a Workplace template configuration.

3.  On the form, scroll down to the Workplace Template Configurations related list.

4.  Click **New**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Configuration table|Configuration table of the workplace service.|
    |Configuration document id|Configuration id of the workplace service.|
    |Template|Template that must be applied to the workplace service or the workplace service activity.|
    |Application|Application of the template. This field is automatically set. Ensure that **Workplace Case Management** is selected.|
    |Active|Option to activate the Workplace template configuration.|
    |Order|Order of the template.|
    |Table|Workplace case table that is used to apply the template.|
    |Condition|Conditions that must be met to apply the template. Use the **AND**, **OR**, and **New criteria** options to build conditions. After you create a condition, click **Preview** to preview the number of records that match the conditions.|

6.  Click **Submit**.


## Result

The Workplace template configuration is added. The template will be applied to those workplace services or workplace service activities that match the specified condition.

**Parent Topic:**[Configure Workplace Case Management](../concept/workplace-case-mgmt-setup.md)

**Related topics**  


[Install Workplace Case Management](install-workplace-case-mgmt.md)

[Create a Workplace case template](wsd-case-template.md)

[Create a Workplace task template](wsd-task-template.md)

[Configure Approval options](config-approval-optns.md)

[Configure a Record producer](wsd-create-record-producer.md)

[Configuring a record producer for request edit](../concept/config-case-edit-rp.md)

[Configuring a record producer for reservation](../concept/config-reservation-rp.md)

[Create an SLA Definition](create-sla-defn-case-mgmt.md)

[Create a Workplace service](create-workplace-service.md)

[Add a workplace service item to a workplace service](add-workplace-service-items.md)

[Create a workplace field mapping](create-workplace-field-mapping.md)

[Configure an escalation rule](configure-escalation-rule.md)

[Add Fulfillment instructions](add-fulfillment-instructions.md)

[Group similar workplace cases under a parent case](group-similar-workplace-cases.md)

