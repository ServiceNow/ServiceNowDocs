---
title: Pattern diagnostic agentic workflow
description: The Pattern diagnostic agentic workflow helps Discovery administrators investigate missing CI attributes. It identifies the gap, parses discovery logs, identifies the root cause, and suggests remediation — without manually navigating log files.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/pattern-diagnostic-agentic-workflow.html
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-09-01"
reading_time_minutes: 4
keywords: [Discovery, agentic workflow, Now Assist, pattern diagnostic, missing attribute, CMDB, data quality]
breadcrumb: [Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Pattern diagnostic agentic workflow

The Pattern diagnostic agentic workflow helps Discovery administrators investigate missing CI attributes. It identifies the gap, parses discovery logs, identifies the root cause, and suggests remediation — without manually navigating log files.

When Discovery runs, it populates CI attributes in the CMDB using both probe-based and pattern-based discovery. The Pattern diagnostic agentic workflow supports investigation into CIs discovered through pattern-based discovery. When an attribute is missing, identifying the cause requires navigating multiple tables and interpreting nested JSON in discovery logs. The Pattern diagnostic agentic workflow automates this investigation and suggests a remediation action, all from the ServiceNow Otto panel.

## Requirements

ServiceNow Otto for IT Operations Management \(ITOM\) must be installed on your instance. For more information, see [Install the ServiceNow Otto for IT Operations Management \(ITOM\) application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/install-now-assist-itom.md).

The Discovery and Service Mapping plugin \(com.snc.discovery\) must be active for this workflow to be available.

Role required: discovery\_admin.

**Note:**

AI Search must be enabled for the workflow to match natural language queries to CI tables. If AI Search is not enabled, you can still use the workflow by providing the direct table name in your query. To enable AI Search, navigate to **All** &gt; **AI Search** &gt; **Enable AI Search**. After enabling, verify that the search status is enabled to confirm indexing is complete.

**Note:**

The workflow is available as a pill in the ServiceNow Otto panel in Discovery Admin Workspace. The workflow can also be invoked by asking plain text questions in the ServiceNow Otto panel.

## Required property configuration

The **glide.discovery.save\_pattern\_log** property controls whether pattern logs are saved after successful pattern execution. By default, this property is set to true, which saves all pattern logs.

If this property is set to false, successful pattern logs are not saved. This can prevent the Pattern diagnostic agentic workflow from performing missing attribute analysis in cases where the attribute is not failing the pattern. Verify that this property is set to true to enable complete analysis. For information about configuring this property, see [Discovery properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/r_DiscoveryProperties.md).

## Pattern diagnostic agentic workflow overview

A Discovery administrator triggers the workflow by asking a natural-language question in the ServiceNow Otto panel. The workflow supports both exploratory investigation, where it surfaces available attributes for selection, and direct investigation, where the administrator specifies the CI class and attribute in the initial question. The workflow then identifies affected CI records with the selected attribute missing, parses the relevant discovery logs to identify the root cause and, when the root cause is classified, displays the corresponding error code, and suggests a remediation.

The workflow uses two agents:

-   Pattern diagnostic agent: Receives the administrator's query and runs script tools autonomously to investigate the missing attribute.
-   EF Remediation Agent: Receives the identified root cause and suggests a remediation.

The second agent runs only when the root cause is classified and logged to the Error Framework. If classification or logging doesn't succeed, the workflow ends after the diagnostic summary, which lists the affected CIs, the error messages from the discovery logs, and general troubleshooting guidance.

When the Error Framework plugin is active and remediations are mapped for the identified error, the workflow provides enhanced remediation suggestions.

## Scope

The workflow covers attribute coverage gaps for CI classes discovered through pattern-based Discovery. The following conditions apply:

-   Only CIs discovered through patterns are supported for analysis.
-   Analysis is based on the pattern metadata table \(sn\_disco\_ai\_pattern\_metadata\). This table contains metadata about the patterns populating a CI and its attributes. Only default pattern information is included; customizations made to patterns aren't considered. Metadata population is limited to an agreed set of CI classes.
-   Log analysis focuses on the first CI in the sample. If issues are found, the workflow reports them and stops. If no issues are found, it checks the next CI in the list, up to the sample limit of five.
-   Log analysis covers the last five days. If no results are found in that period, the search expands to 30 days.

## Examples

The following scenarios illustrate how the workflow handles different CI and pattern types.

-   **Scenario 1: Direct infrastructure \(Linux Server\)**

    The workflow investigates a missing `cpu_manufacturer` attribute on Linux Server CIs. The workflow resolves the CIs IP address and queries the discovery logs directly. It returns a full report with sample CIs investigated, link to CIs, root cause and remediation guidance.

-   **Scenario 2: Applicative pattern \(MySQL database\)**

    The workflow investigates a missing attribute on a MySQL database CI. MySQL CIs are discovered through their host servers. The workflow navigates the Runs on relationship to resolve the host server's IP address and queries the discovery logs on the host, not the MySQL instance. It returns a full report with sample CIs investigated, link to CIs, root cause and remediation guidance.

-   **Scenario 3: Cloud pattern \(AWS Auto Scaling Group\)**

    The workflow investigates a missing `cluster_connection` attribute on an AWS Auto Scaling Group CI. Cloud CIs use an SA-LDC identifier instead of a traditional IP address. The workflow navigates the Hosted on relationship to resolve the SA-LDC identifier and searches logs using the identifier and process ID. It returns a full report with sample CIs investigated, link to CIs, root cause and remediation guidance.


