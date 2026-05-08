---
title: Security Incident Response Orchestration workflows and activities
description: Several workflows and activities are included with Security Incident Response Orchestration.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Understand Security Incident Response Orchestration workflows and workflow templates, Security Incident Response Orchestration, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Response Orchestration workflows and activities

Several workflows and activities are included with Security Incident Response Orchestration.

Only users with the sn\_sec\_cmn.admin role can Workflow editor.

-   **[Create Lookup Request for IoC Changes workflow](../task/t_CreateScanRequestforIoCChanges.md)**  
The **Security Incident Response - Create Lookup Request for IoC Changes** flow is triggered by a business rule to run automatically when an IoC is added or changed. Malware scans are triggered only when new data is entered and only the new data is scanned.
-   **[Security Incident Response- Get Network Statistics flow](../task/obtain-network-statistics-workflow.md)**  
The **Security Incident Response** &gt; **Get Network Statistics** flow retrieves the network statistics for an affected Windows-based resource when added to a security incident in the **Analysis** state.
-   **[Security Incident Response - Get Running Services workflow](../task/get-running-services-workflow.md)**  
The **Security Incident Response - Get Running Services workflow** retrieves a list of running services from Windows-based, ServiceNow, configuration items \(CIs\). This workflow is used for incident enrichment during investigations.
-   **[Run procdump flow](invoke_procdump.md)**  
The **Run procdump** flow runs a process dump on a specified process and saves it to a file that can be targeted by security analysts.
-   **[Security Incident - Evaluate response task outcome workflow](../task/si-evaluate-response-task-outcome-workflow.md)**  
Security Incident - Evaluate Response task outcome workflow determines the task to use, invokes a chosen workflow and evaluation script based on the outcome evaluator record provided as input to the chosen workflow.

**Parent Topic:**[Understand Security Incident Response Orchestration workflows and workflow templates](../../../administer/workflow/task/view-wf-templates.md)

