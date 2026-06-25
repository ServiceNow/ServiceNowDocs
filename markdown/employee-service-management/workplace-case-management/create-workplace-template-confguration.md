---
title: Create a workplace template configuration
description: Define a template that must be applied to fulfill a workplace case. Set conditions based on common employee responses for requests. The template will be applied to those workplace cases that match the conditions specified.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-case-management/create-workplace-template-confguration.html
release: australia
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
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

[Create an SLA Definition]()

[Create a Workplace service]()

[Add a workplace service item to a workplace service]()

[Create a workplace field mapping]()

[Configure an escalation rule]()

[Add Fulfillment instructions]()

[Group similar workplace cases under a parent case]()

