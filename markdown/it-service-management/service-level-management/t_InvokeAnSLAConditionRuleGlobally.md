---
title: Invoke an SLA condition rule globally
description: You can globally change the default set of SLA condition rules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-level-management/t\_InvokeAnSLAConditionRuleGlobally.html
release: australia
product: Service Level Management
classification: service-level-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Extend SLA condition rules, Configuring Service Level Management, Service Level Management, IT Service Management]
---

# Invoke an SLA condition rule globally

You can globally change the default set of SLA condition rules.

## Before you begin

Role required: admin

## About this task

By default, the SLAConditionBase is used for the SLA condition rules. This can be changed by doing the following:

## Procedure

1.  Navigate to **All** &gt; **Service Level Management** &gt; **SLA Properties**.

2.  Change the value of the **com.snc.sla.default\_conditionclass** [SLA property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-level-management/t_ConfigureSLAProperties.md) to the new condition rule name:

    \[Omitted image "SLAConditionsProperty.png"\] Alt text: SLAConditions Property

    **Note:** This is the default condition rule, if no condition rule is specified on an SLA definition.


**Parent Topic:**[Extend SLA condition rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-level-management/c_ExtendSLAConditionRules.md)

**Related topics**  


[SLA condition rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-level-management/c_SLAConditionRules.md)

