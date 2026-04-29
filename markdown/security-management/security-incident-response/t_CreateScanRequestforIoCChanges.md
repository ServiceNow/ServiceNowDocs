---
title: Create Lookup Request for IoC Changes workflow
description: The Security Incident Response - Create Lookup Request for IoC Changes flow is triggered by a business rule to run automatically when an IoC is added or changed. Malware scans are triggered only when new data is entered and only the new data is scanned.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Incident Response Orchestration workflows and activities, Understand Security Incident Response Orchestration workflows and workflow templates, Security Incident Response Orchestration, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create Lookup Request for IoC Changes workflow

The **Security Incident Response - Create Lookup Request for IoC Changes** flow is triggered by a business rule to run automatically when an IoC is added or changed. Malware scans are triggered only when new data is entered and only the new data is scanned.

## Before you begin

Role required: sn\_si.basic

## About this task

If the IoC is empty, the workflow does not run. Historical scans are retained and viewable in the **Security Scan Requests** tab and worknotes of the security incident. The existing security incidents are automatically updated.

**Important:**

The **Security Incident Response - Create Lookup Request for IoC Changes** workflow is migrated to the Flow Designer. The flow gets triggered only when the sn\_ti\_scanner has at least one record.

The Flow Designer actions include:

-   Audit Log Enrichment
-   [Create IoC Lookup Request activity](../reference/r_CreateMalwareScanRequest.md)

![Security Incident Response - Create Lookup Request for IoC Changes workflow diagram](../image/ScanRequest4IoChangesWorkflow.png "IoC Changes workflow")

-   **[Create IoC Lookup Request activity](../reference/r_CreateMalwareScanRequest.md)**  
The **Create IoC Lookup Request** activity can be used with any workflow to create a malware lookup request for added or modified IoC fields.

**Parent Topic:**[Security Incident Response Orchestration workflows and activities](../concept/sec-inc-resp-orchestration-workflows.md)

**Related topics**  


[Security Incident Response- Get Network Statistics flow](obtain-network-statistics-workflow.md)

[Security Incident Response - Get Running Services workflow](get-running-services-workflow.md)

[Run procdump flow](../concept/invoke_procdump.md)

[Security Incident - Evaluate response task outcome workflow](si-evaluate-response-task-outcome-workflow.md)

