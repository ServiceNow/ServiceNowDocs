---
title: Security Incident Response - Get Running Services Flow
description: The Security Incident Response - Get Running Services Flow retrieves a list of running services from Windows-based, ServiceNow, configuration items \(CIs\). This flow is used for incident enrichment during investigations.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Security Incident Response Orchestration flows and actions, Understand Security Incident Response Orchestration workflows and workflow templates, Security Incident Response Orchestration, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Response - Get Running Services Flow

The **Security Incident Response - Get Running Services Flow** retrieves a list of running services from Windows-based, ServiceNow, configuration items \(CIs\). This flow is used for incident enrichment during investigations.

## Before you begin

Role required: sn\_si.analyst

## About this task

The **Security Incident Response - Get Running Services Flow** runs automatically when you add a new configuration item to a Windows security incident after the state changes to **Analysis**. The information this flow obtains appears on the **Show Enrichment Data** tabs for the security incident.

**Note:** If the security incident remains in the **Draft** state, the **Security Incident Response - Get Running Services Flow** does not run.

The flow activities include:

-   Audit Log Enrichment Script flow action
-   [Get Configuration Item FQDN Flow Action](../../security-operations-orchestration/reference/get-config-FQDN-activity.md)
-   [Determine Shell Script by OS Flow Action](../../security-operations-integrations/reference/determine-shell-script-by-os-activity.md)
-   Is Execution via PowerShell flow action
-   [Get Running Services - WMI Enrichment activity](../../security-operations-integrations/reference/get-running-services-via-pwrshell-activity.md)
-   [Create Enrichment Data records Flow Action](../../security-operations-common/concept/create-enrich-data-records.md)

![Security Incident Response - Get Running Services flow diagram](../image/get-running-service.png "Get Running Services")

## Procedure

1.  Open a security incident.

2.  Update the **State** to **Analysis**, if necessary.

3.  Add a Windows-based configuration item \(server, laptop, or similar\).

4.  Click **Update**.

    Security Incident Response provides running services information in the **Related Links** &gt; **Security Incident Enrichments**tab. For more information, see [Security Operations enrichment data mapping](../../security-operations-common/concept/enrichment-data-mapping.md).


-   **[Determine Shell Script by OS Flow Action](../../security-operations-integrations/reference/determine-shell-script-by-os-activity.md)**  
The Determine Shell Script by OS flow action determines which operating system to use in the flow.
-   **[Get Running Services - WMI Enrichment](../../security-operations-integrations/reference/get-running-services-via-pwrshell-activity.md)**  
The **Security Incident Response - Get Running Services** flow gathers running services on a configuration item added to a security incident.

**Parent Topic:**[Security Incident Response Orchestration flows and actions](../concept/sec-inc-resp-orchestration-workflows.md)

**Related topics**  


[Create Lookup Request for IoC Changes Flow](t_CreateScanRequestforIoCChanges.md)

[Security Incident Response- Get Network Statistics Flow](obtain-network-statistics-workflow.md)

[Run procdump flow](../concept/invoke_procdump.md)

[Security Incident - Evaluate response task outcome workflow](si-evaluate-response-task-outcome-workflow.md)

