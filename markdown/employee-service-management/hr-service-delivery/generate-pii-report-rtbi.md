---
title: Generate Personally Identifiable Information \(PII\) report
description: As an HR agent, generate the PII report requested by the employee or alumni.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Personal Data Rights in HR Service Delivery, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Generate Personally Identifiable Information \(PII\) report

As an HR agent, generate the PII report requested by the employee or alumni.

## Before you begin

Role required: HR agent \(sn\_hr\_core.basic\)

PII in HR Core tables are manually identified and classified into categories called classes. For example, Contact information, Identification information, and so on. These classifications serve as a reference, you can also create your own classifications. For more information, see Data Classification.

**Note:** The classes are available in the data classification module which is auto-installed with HR Core. The classified dictionary entries under each class are included in the HR Core plugin's demo data.

## Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **All HR Cases**.

2.  Select **Assigned to me**.

3.  Select a case with Request Personal Information Report as the HR service and in Ready state.

    **Note:** If the employee in the HR case has a manager, the case must be approved by the manager before it is moved to the agent. The case is in the Awaiting approval status until the manager approves. If an approver is missing, agents can manually add the approver.

4.  Select the **Start work** button.

5.  Select the **Generate PII report** button.


## Result

The PII report is generated and is added as an attachment to the case.

**Note:** In case there are ACLs in place to hide information for some of the fields, those fields remain empty in the report and the fields information is displayed in the work notes.

