---
title: Security Operations Carbon Black Integration - Isolate Host Flow
description: The Security Operations Carbon Black Integration - Isolate Host is the implementation for the Carbon Black integration launched by the Security Operations Integration - Isolate Host flow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/security-management/secops-integration-cb-isolate-host-workflow.html
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Security Operations Integration- Isolate Host capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Carbon Black Integration - Isolate Host Flow

The Security Operations Carbon Black Integration - Isolate Host is the implementation for the Carbon Black integration launched by the Security Operations Integration - Isolate Host flow.

## Before you begin

Role required: sn\_si.analyst

## About this task

The flow process flow action include:

-   [Execution Tracking - Begin \(CIs\) Flow Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/execution-tracking-begins-cis-activity.md)
-   [Get IP from CI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/get-ip-from-ci-activity.md)
-   [Collect Carbon Black configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/collect-cb-config-activity.md)
-   [Capability Execution Tracking- Failure Flow Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/capability-execution-tracking-failure.md)
-   [Get Sensor ID](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/get-sensor-id-activity.md)
-   [Set Network Isolation Enabled Flow Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown)
-   [Update Sensor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/update-sensor-activity.md) - returns Isolate Host result.

\[Omitted image "carbon-black-integration-isolate-host-flow-v1.png"\] Alt text: Flow designer for Security Operations Carbon Black Integration - Isolate Host\[Omitted image "carbon-black-integration-isolate-host-flow-v1-2.png"\] Alt text: Flow designer for Security Operations Carbon Black Integration - Isolate Host

-   **[Get Sensor ID Flow Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/get-sensor-id-activity.md)**  
The Get Sensor ID flow action gathers sensor identifiers to use in the flow.
-   **[Set Network Isolation Enabled Flow Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown)**  
The Set Network Isolation Enabled flow action enables network isolation.
-   **[Update Sensor Flow Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/update-sensor-activity.md)**  
The Update Sensor flow action updates the sensor to isolate hosts or endpoints.

**Parent Topic:**[Security Operations Integration- Isolate Host capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/isolate-host-capability.md)

