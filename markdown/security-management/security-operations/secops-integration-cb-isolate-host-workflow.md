---
title: Security Operations Carbon Black Integration - Isolate Host Flow
description: The Security Operations Carbon Black Integration - Isolate Host is the implementation for the Carbon Black integration launched by the Security Operations Integration - Isolate Host flow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-operations/secops-integration-cb-isolate-host-workflow.html
release: zurich
product: Security Operations
classification: security-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Security Operations Integration- Isolate Host capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Carbon Black Integration - Isolate Host Flow

The Security Operations Carbon Black Integration - Isolate Host is the implementation for the Carbon Black integration launched by the Security Operations Integration - Isolate Host flow.

## Before you begin

Role required: sn\_si.analyst

## About this task

The flow process activities include:

-   [Execution Tracking - Begin \(CIs\) Flow Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/execution-tracking-begins-cis-activity.md)
-   [Get IP from CI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/get-ip-from-ci-activity.md)
-   [Collect Carbon Black configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/collect-cb-config-activity.md)
-   [Capability Execution Tracking- Failure Flow Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/capability-execution-tracking-failure.md)
-   [Get Sensor ID](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/get-sensor-id-activity.md)
-   [Set Network Isolation Enabled activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown)
-   [Update Sensor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/update-sensor-activity.md) - returns Isolate Host result.
-   [Capability Execution Tracking - Complete Flow Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/capability-execution-tracking-complete.md)

\[Omitted image "carbon-black-integration-isolate-host-flow-v1.png"\] Alt text: Flow designer for Security Operations Carbon Black Integration - Isolate Host\[Omitted image "carbon-black-integration-isolate-host-flow-v1-2.png"\] Alt text: Flow designer for Security Operations Carbon Black Integration - Isolate Host

Activities specific to this flow are described here. For more information on other activities, see [Common Security Operations integration flows and orchestration activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/common-wf-activities.md).

-   **[Get Sensor ID Flow Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/get-sensor-id-activity.md)**  
The Get Sensor ID flow action gathers sensor identifiers to use in the flow.
-   **[Set Network Isolation Enabled activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown)**  
The Set Network Isolation Enabled workflow activity enables network isolation.
-   **[Update Sensor activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/update-sensor-activity.md)**  
The Update Sensor workflow activity updates the sensor to isolate hosts or endpoints.

**Parent Topic:**[Security Operations Integration- Isolate Host capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/isolate-host-capability.md)

