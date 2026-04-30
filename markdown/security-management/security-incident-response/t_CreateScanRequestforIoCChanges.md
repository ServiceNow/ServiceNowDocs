---
title: Create Lookup Request for IoC Changes Flow
description: The Security Incident Response - Create Lookup Request for IoC Changes flow is triggered by a business rule to run automatically when an IoC is added or changed. Malware scans are triggered only when new data is entered and only the new data is scanned.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Security Incident Response Orchestration flows and actions, Understand Security Incident Response Orchestration workflows and workflow templates, Security Incident Response Orchestration, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create Lookup Request for IoC Changes Flow

The **Security Incident Response - Create Lookup Request for IoC Changes** flow is triggered by a business rule to run automatically when an IoC is added or changed. Malware scans are triggered only when new data is entered and only the new data is scanned.

## Before you begin

Role required: sn\_si.basic

## About this task

If the IoC is empty, the flow does not run. Historical scans are retained and viewable in the **Security Scan Requests** tab and worknotes of the security incident. The existing security incidents are automatically updated.

**Important:**

The **Security Incident Response - Create Lookup Request for IoC Changes** workflow is migrated to the Flow Designer. The flow gets triggered only when the sn\_ti\_scanner has at least one record.

The Flow Designer actions include:

-   Audit Log Enrichment
-   [Create IoC Lookup Request Flow Action](../reference/r_CreateMalwareScanRequest.md)

![Security Incident Response - Create Lookup Request for IoC Changes flow diagram](../image/ScanRequest4IoChangesWorkflow.png "IoC Changes flow")

-   **[Create IoC Lookup Request Flow Action](../reference/r_CreateMalwareScanRequest.md)**  
The **Create IoC Lookup Request** flow action can be used with any flow to create a malware lookup request for added or modified IoC fields.

**Parent Topic:**[Security Incident Response Orchestration flows and actions](../concept/sec-inc-resp-orchestration-workflows.md)

**Related topics**  


[Security Incident Response- Get Network Statistics Flow](obtain-network-statistics-workflow.md)

[Security Incident Response - Get Running Services Flow](get-running-services-workflow.md)

[Run procdump flow](../concept/invoke_procdump.md)

[Security Incident - Evaluate response task outcome workflow](si-evaluate-response-task-outcome-workflow.md)

