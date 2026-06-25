---
title: Configure an escalation rule
description: Escalate a workplace case to the relevant assignment group by using an escalation rule.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-case-management/configure-escalation-rule.html
release: australia
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Configure an escalation rule

Escalate a workplace case to the relevant assignment group by using an escalation rule.

## Before you begin

Role required: sn\_wsd\_case.admin or sn\_wsd\_case.manager

## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Workplace Case Management - Setup** &gt; **Escalation rules**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Escalate from|Assignment group from which you want to escalate the workplace case.|
    |Escalate to|Assignment group to which you want to escalate the workplace case.|
    |Domain|Domain of your application. This field is automatically set to your application domain.|

4.  Click **Submit**.


## Result

The escalation rule is created. The rule is displayed under the Related links of those workplace cases that have the assignment group \(specified in **Escalated from**\) for which the rule is created.

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

[Create a workplace template configuration]()

[Create a workplace field mapping]()

[Add Fulfillment instructions]()

[Group similar workplace cases under a parent case]()

