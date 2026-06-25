---
title: Security Incident Response - Get Running Services workflow
description: The Security Incident Response - Get Running Services workflow retrieves a list of running services from Windows-based, ServiceNow, configuration items \(CIs\). This workflow is used for incident enrichment during investigations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/get-running-services-workflow.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Security Incident Response Orchestration workflows and activities, Understand Security Incident Response Orchestration workflows and workflow templates, Security Incident Response Orchestration, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Response - Get Running Services workflow

The **Security Incident Response - Get Running Services workflow** retrieves a list of running services from Windows-based, ServiceNow, configuration items \(CIs\). This workflow is used for incident enrichment during investigations.

## Before you begin

Role required: sn\_si.analyst

## About this task

The **Security Incident Response - Get Running Services workflow** runs automatically when you add a new configuration item to a Windows security incident after the state changes to **Analysis**. The information this workflow obtains appears on the **Show Enrichment Data** tabs for the security incident.

**Note:** If the security incident remains in the **Draft** state, the **Security Incident Response - Get Running Services workflow** workflow does not run.

Workflow activities include:

-   Audit Log Enrichment Script activity
-   [Get Configuration Item FQDN Flow Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/get-config-FQDN-activity.md)
-   [Determine Shell Script by OS activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/determine-shell-script-by-os-activity.md)
-   Is Execution via PowerShell activity
-   [Get Running Services - WMI Enrichment activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/get-running-services-via-pwrshell-activity.md)
-   [Create Enrichment Data records Flow Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/create-enrich-data-records.md)

## Procedure

1.  Open a security incident.

2.  Update the **State** to **Analysis**, if necessary.

3.  Add a Windows-based configuration item \(server, laptop, or similar\).

4.  Select **Update**.

    Security Incident Response provides running services information in the **Related Links** &gt; **Security Incident Enrichments**tab. For more information, see [Security Operations enrichment data mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/enrichment-data-mapping.md).


-   **[Determine Shell Script by OS activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/determine-shell-script-by-os-activity.md)**  
The Determine Shell Script by OS workflow activity determines which operating system to use in the workflow
-   **[Get Running Services - WMI Enrichment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/get-running-services-via-pwrshell-activity.md)**  
The **Security Incident Response - Get Running Services** workflow gathers running services on a configuration item added to a security incident.

**Parent Topic:**[Security Incident Response Orchestration workflows and activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/sec-inc-resp-orchestration-workflows.md)

**Related topics**  


[Create Lookup Request for IoC Changes workflow]()

[Security Incident Response- Get Network Statistics flow]()

[Run procdump flow]()

[Security Incident - Evaluate response task outcome workflow]()

