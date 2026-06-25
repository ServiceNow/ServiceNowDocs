---
title: Create Lookup Request for IoC Changes workflow
description: The Security Incident Response - Create Lookup Request for IoC Changes flow is triggered by a business rule to run automatically when an IoC is added or changed. Malware scans are triggered only when new data is entered and only the new data is scanned.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/t\_CreateScanRequestforIoCChanges.html
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
-   [Create IoC Lookup Request activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/r_CreateMalwareScanRequest.md)

\[Omitted image "ScanRequest4IoChangesWorkflow.png"\] Alt text: Security Incident Response - Create Lookup Request for IoC Changes workflow diagram

-   **[Create IoC Lookup Request activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/r_CreateMalwareScanRequest.md)**  
The **Create IoC Lookup Request** activity can be used with any workflow to create a malware lookup request for added or modified IoC fields.

**Parent Topic:**[Security Incident Response Orchestration workflows and activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/sec-inc-resp-orchestration-workflows.md)

**Related topics**  


[Security Incident Response- Get Network Statistics flow]()

[Security Incident Response - Get Running Services workflow]()

[Run procdump flow]()

[Security Incident - Evaluate response task outcome workflow]()

