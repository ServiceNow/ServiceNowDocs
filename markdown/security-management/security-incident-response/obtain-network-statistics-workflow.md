---
title: Security Incident Response- Get Network Statistics flow
description: The Security Incident Response Get Network Statistics flow retrieves the network statistics for an affected Windows-based resource when added to a security incident in the Analysis state.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/obtain-network-statistics-workflow.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Security Incident Response Orchestration workflows and activities, Understand Security Incident Response Orchestration workflows and workflow templates, Security Incident Response Orchestration, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Response- Get Network Statistics flow

The **Security Incident Response** &gt; **Get Network Statistics** flow retrieves the network statistics for an affected Windows-based resource when added to a security incident in the **Analysis** state.

## Before you begin

Role required: sn\_si.analyst

## About this task

For new security incidents that contain configuration items, the flow runs automatically when the state changes to **Analysis**.

Existing security incidents are automatically updated when you are in the **Analysis** state and you add a new configuration item.

\[Omitted image "get-network-statistics-flow.png"\] Alt text: Get Network Statistics flow

The flow process actions include:

-   [Get Configuration Item FQDN Flow Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/get-config-FQDN-activity.md)
-   Determine Shell Script by OS
-   If statement is executed by Powershell
-   [Execution Tracking - Begin Flow Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/execution-tracking-begin.md)
-   [Get Network Statistics via netstat Flow Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/get-network-stats-netstat-activity.md)
-   [Capability Execution Tracking- Failure Flow Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/capability-execution-tracking-failure.md)
-   [Create Enrichment Data records Flow Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/create-enrich-data-records.md)
-   [Capability Execution Tracking- Failure Flow Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/capability-execution-tracking-failure.md) - Returns enrichment ID.
-   [Capability Execution Tracking - Complete Flow Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/capability-execution-tracking-complete.md)

## Procedure

1.  Open a security incident.

2.  Update the **State** to **Analysis**, if necessary.

3.  Add a configuration item \(computer, server, or similar\).

4.  Click **Update**.

    Security Incident Response Orchestration provides network statistics information in the **Related Links** &gt; **Security Incident Enrichments** tab. For more information see, [Security Operations enrichment data mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/enrichment-data-mapping.md).

    Actions specific to this flow are described here. For more information on other actions, see [Common Security Operations integration flows and orchestration activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/common-wf-activities.md).


**Parent Topic:**[Security Incident Response Orchestration workflows and activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/sec-inc-resp-orchestration-workflows.md)

**Parent Topic:**[Security Operations Integration- Get Network Statistics capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/get-network-statistics-capability.md)

**Related topics**  


[Create Lookup Request for IoC Changes workflow]()

[Security Incident Response - Get Running Services workflow]()

[Run procdump flow]()

[Security Incident - Evaluate response task outcome workflow]()

