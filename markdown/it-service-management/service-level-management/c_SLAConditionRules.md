---
title: SLA condition rules
description: SLA condition rules control how the different conditions you define in an SLA definition are combined to determine whether an SLA should attach, pause, complete, reattach, or cancel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/service-level-management/c\_SLAConditionRules.html
release: zurich
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Service Level Management, IT Service Management]
---

# SLA condition rules

SLA condition rules control how the different conditions you define in an SLA definition are combined to determine whether an SLA should attach, pause, complete, reattach, or cancel.

The way that the conditions in an SLA definition are interpreted, to control transitions in state, can be varied using SLA Condition Rules. SLA Condition Rules are defined globally, and can be overridden for specific SLA definitions.

**SLAConditionBase** is the default set of SLA condition rules.

Navigate to **Service Level Management** &gt; **Administration** &gt; **SLA Condition Rules** to see a list of SLA condition records.

-   **[SLAConditionBase script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/service-level-management/r_SLAConditionBase.md)**  
The SLAConditionBase script include implements the default SLA transitions.
-   **[SLAConditionSimple script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/service-level-management/r_SLAConditionSimple.md)**  
The SLAConditionSimple script include provides an example modification of default SLA condition processing.

**Parent Topic:**[Service Level Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/service-level-management/service-level-management-reference.md)

