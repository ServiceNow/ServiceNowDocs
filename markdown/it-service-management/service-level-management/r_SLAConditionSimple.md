---
title: SLAConditionSimple script
description: The SLAConditionSimple script include provides an example modification of default SLA condition processing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-level-management/r\_SLAConditionSimple.html
release: australia
product: Service Level Management
classification: service-level-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SLA condition rules, Service Level Management reference, Service Level Management, IT Service Management]
---

# SLAConditionSimple script

The SLAConditionSimple script include provides an example modification of default SLA condition processing.

The SLAConditionSimple script include is one of the default supplied SLA condition rules. This shows an example of how you can modify and extend condition processing, by overriding the SLAConditionBase methods, with a 'simple' variation that interprets each condition to match a particular transition. For example, for an SLA to attach only the start condition is checked. This affects attach, reattach, and cancel.

To edit this script, navigate to **Service Level Management** &gt; **Administration** &gt; **SLA Condition Rules**, then click on the **SLAConditionSimple** entry to view or modify details. Click **Class name** field to open the script include that defines the condition processing.

The following diagram shows how the transitions work:

\[Omitted image "SLAConditionSimple.png"\] Alt text: Task SLA simple condition stage transition diagram

**Parent Topic:**[SLA condition rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-level-management/c_SLAConditionRules.md)

