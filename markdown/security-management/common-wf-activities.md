---
title: Common Security Operations integration flows and orchestration activities
description: Many of the flows associated with third-party integrations include the same activities. For example, activities for beginning and completing processing.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Common Security Operations integration flows and orchestration activities

Many of the flows associated with third-party integrations include the same activities. For example, activities for beginning and completing processing.

-   **[Execution Tracking - Begin Flow Action](execution-tracking-begin.md)**  
The Execution Tracking - Begin flow action starts the auditing process for a Security Operations Integration flow that operates on observables.
-   **[Capability Execution Tracking - Complete Flow Action](capability-execution-tracking-complete.md)**  
The Capability Execution Tracking - Complete flow action updates the audit record when the flow is complete.
-   **[Capability Execution Tracking- Failure Flow Action](capability-execution-tracking-failure.md)**  
The Capability Execution Tracking - Failure flow action records a failure to the audit record.
-   **[Capability - Determine CIs activity](../../security-operations-integrations/reference/determine-cis-activity.md)**  
The Capability - Determine CIs workflow activity determines which configuration items \(CIs\) to include in the workflow.
-   **[Create Enrichment Data records Flow Action](create-enrich-data-records.md)**  
The **Create enrichment data records** flow action creates or updates enrichment records to use in the flow.
-   **[Get Configuration Item FQDN Flow Action](../../security-operations-orchestration/reference/get-config-FQDN-activity.md)**  
The **Security Common Orchestration** &gt; **Get Configuration Item FQDN** flow action retrieves the fully qualified domain name \(FQDN\) of a configuration item. This flow action can accelerate the investigation and remediation process.
-   **[Determine Observables activity](../../security-operations-integrations/reference/determine-observables-activity.md)**  
The **Determine Observables** workflow activity determines which observable to include in the workflow
-   **[Get Supported Security Capabilities action](../../security-operations-integrations/reference/get-supported-security-capabilities-activity.md)**  
The Get Supported Capabilities flow action retrieves the name and number of integrations that are active and support the requested capability.
-   **[Capability Execution Tracking- No Impls action](../../security-operations-integrations/reference/execution-tracking-noimpls-activity.md)**  
The Capability Execution Tracking - No Impls flow action creates an error record when no integration capability implementation is found.
-   **[Create Compliance Search Action](../../secops-integration-sir/secops-integration-ms-exchange-on-prem/reference/get-email-details-from-exch-server.md)**  
The Create Compliance Search action creates a compliance search for emails in the designated Exchange server\(s\) using the search queries defined and returns the name of compliance search created.
-   **[Get IP from CI activity](../../security-operations-orchestration/reference/get-IP-from-CI-activity.md)**  
This workflow activity determines the IPV4 address associated with a configuration item \(CI\).
-   **[Get Network Statistics via netstat Flow Action](../../security-operations-orchestration/reference/get-network-stats-netstat-activity.md)**  
The Security Common Orchestration - Get Network Statistics via netstat flow action retrieves the network statistics for an affected resource on a Windows-based system. This flow action can accelerate the investigation and remediation process.
-   **[Get running processes via WMI activity](../../security-operations-orchestration/reference/get-running-process-WMI-activity.md)**  
The**Get Running Processes** workflow activity retrieves the running processes of a configuration item on a Windows-based system. This activity can accelerate the investigation and remediation process.
-   **[Check Compliance Search Status Action](../../secops-integration-sir/secops-integration-ms-exchange-on-prem/reference/search-delete-email-threat-exchange.md)**  
The Check Compliance Search Status action check the status of created compliance search on exchange server and if the status is completed return the information regarding email search found for the compliance search.
-   **[Update Task Worknotes activity](../../security-operations-orchestration/reference/update-task-worknotes-activity.md)**  
The **Security Common Orchestration - Update Task Worknotes** workflow activity updates the **Activity** section \(work notes\) of a task record. This is useful for logging information.
-   **[Roll up lookup info to security incident activity](../../threat-intelligence-orchestration/reference/r_RollUpScanInfoSI.md)**  
The **Roll up lookup info to security incident** activity can be used with any workflow to gather information from a threat lookup and output a summary of the contents as well as the ID of the originating security incident in task work notes.
-   **[Update security incident with lookup results workflow](../../threat-intelligence-orchestration/task/t_UpdateSecIncScanResults.md)**  
The **Update security incident with lookup results** workflow updates existing security incidents with lookup results.
-   **[Filter Allowlisted Observables activity](../../security-operations-integrations/reference/filter-whitelisted-observables-activity.md)**  
The Filtered Allowlisted Observables workflow activity removes observables that can be ignored from the list of observables. This activity can accelerate the investigation and remediation process.
-   **[Write content to record as attachment activity](../../security-operations-orchestration/reference/write-content-record-attachment-activity.md)**  
This activity writes the content passed in from an input and creates a designated attachment to a given record.
-   **[Get IP from CI activity](../../security-operations-integrations/reference/get-ip-from-ci-activity.md)**  
The Get IP from CI flow activity gathers the IP address from configuration items \(CIs\) to use in the flow.

**Parent Topic:**[Security Operations Integration Reference](../../secops-integration-reference/concept/secops-integ-ref.md)

