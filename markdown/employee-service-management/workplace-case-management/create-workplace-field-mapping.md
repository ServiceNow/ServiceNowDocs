---
title: Create a workplace field mapping
description: Create a field mapping record to copy the field information of a parent case to the child workplace service activities or to workplace item-related tasks. Skip the process of re-entering the same details of a parent case to a child case by using field mapping records.
locale: en-US
release: yokohama
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configure, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Create a workplace field mapping

Create a field mapping record to copy the field information of a parent case to the child workplace service activities or to workplace item-related tasks. Skip the process of re-entering the same details of a parent case to a child case by using field mapping records.

## Before you begin

Role required: sn\_wsd\_case.manager

## About this task

Save time from manually entering details in a child case or task triggered by a parent workplace case. The Workplace Service Activity Field Mapping or Workplace Service item Field Mapping enables you to copy the details specified in a parent case's field to its child cases and tasks. This option is available only for the workplace services of the type Workplace Service activity and for tasks or cases triggered by a Workplace Service item request. You must create individual field mapping records for each field mapping.

## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Workplace Case Management - Setup** &gt; **Workplace services**.

2.  Select the workplace service to which you want to apply the field mapping.

3.  On the form, scroll down to the related list section.

4.  Select the related list where you want to add a field mapping record.

    -   Workplace Service item: Select this related list to add a field mapping record to a workplace service item.
    -   Workplace Service Activities: Select this related list to add a field mapping record to a workplace service activity.
5.  Based on the select related list, select the Workplace service item or the Workplace Service Activity to which you want to add a field mapping.

6.  On the form, scroll down to the related lists section.

    If you selected Workplace service item, then the Workplace Service item Field Mapping related list appears. If you selected a workplace service activity, then the Workplace Service Activity Field Mapping related list appears.

7.  Select the relevant related list.

8.  Click **New**.

9.  On the form, fill in the fields.

    | | |
    |---|---|
    |Name|Name of the field mapping.|
    |From / Condition table|Table that is used to copy fields and build conditions.|
    |Map from field|Field from which the value must be mapped.|
    |Active|Option to activate the mapping.|
    |Map to table|Table to which the field details are copied.|
    |Map to field|Field to which the value is copied.|
    |Order|Order in which the field mapping must be performed when there are multiple field mappings.|
    |Condition|Conditions that must be matched to apply the field mapping. Click **New criteria** to add conditions.|

10. Click **Submit**.


## Result

The field mapping record is added.

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

[Create a workplace template configuration](create-workplace-template-confguration.md)

[Configure an escalation rule](configure-escalation-rule.md)

[Add Fulfillment instructions](add-fulfillment-instructions.md)

[Group similar workplace cases under a parent case](group-similar-workplace-cases.md)

