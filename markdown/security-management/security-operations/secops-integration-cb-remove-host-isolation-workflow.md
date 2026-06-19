---
title: Security Operations Carbon Black Integration- Remove Host Isolation Flow
description: The Security Operations Carbon Black Integration - Remove Host Isolation flow unblocks communication with a specified host or endpoint in a Carbon Black system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-operations/secops-integration-cb-remove-host-isolation-workflow.html
release: australia
product: Security Operations
classification: security-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Operations Integration- Isolate Host capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Carbon Black Integration- Remove Host Isolation Flow

The **Security Operations Carbon Black Integration - Remove Host Isolation** flow unblocks communication with a specified host or endpoint in a Carbon Black system.

## Before you begin

Role required: sn\_si.analyst

## About this task

This flow is not part of a capability and needs a custom orchestration in order to run.

The flow process activities include:

-   [Get IP from CI activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/get-ip-from-ci-activity.md)
-   If successful- [Collect Carbon Black Configurations Flow Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/collect-cb-config-activity.md)
-   [Get Sensor ID Flow Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/get-sensor-id-activity.md)[Get Sensor ID](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/get-sensor-id-activity.md)
-   If- Device supports isolation- and device is not isolated to disabled.
-   [Update Sensor activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/update-sensor-activity.md)- returns Isolate Host result.

\[Omitted image "RemoveHostIsolationWorkflow.png"\] Alt text: Remove Host Isolation low diagram

**Parent Topic:**[Security Operations Integration- Isolate Host capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/isolate-host-capability.md)

