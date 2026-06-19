---
title: Pattern diagnostic agentic workflow
description: The Pattern diagnostic agentic workflow helps Discovery administrators investigate missing CI attributes. It identifies the gap, parses discovery logs, identifies the root cause, and suggests remediation — without manually navigating log files.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/now-assist-for-it-operations-management/pattern-diagnostic-agentic-workflow.html
release: zurich
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 2
keywords: [Discovery, agentic workflow, Now Assist, pattern diagnostic, missing attribute, CMDB, data quality]
breadcrumb: [Use agentic AI, Now Assist for ITOM, IT Operations Management]
---

# Pattern diagnostic agentic workflow

The Pattern diagnostic agentic workflow helps Discovery administrators investigate missing CI attributes. It identifies the gap, parses discovery logs, identifies the root cause, and suggests remediation — without manually navigating log files.

When Discovery runs, it populates CI attributes in the CMDB using both probe-based and pattern-based discovery. The Pattern diagnostic agentic workflow supports investigation into CIs discovered through pattern-based discovery. When an attribute is missing, identifying the cause requires navigating multiple tables and interpreting nested JSON in discovery logs. The Pattern diagnostic agentic workflow automates this investigation and suggests a remediation action, all from the Now Assist panel.

## Requirements

Now Assist for IT Operations Management \(ITOM\) must be installed on your instance. For more information, see [Install the Now Assist for IT Operations Management \(ITOM\) plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/install-now-assist-itom.md).

Role required: discovery\_admin.

## Pattern diagnostic agentic workflow overview

A Discovery administrator triggers the workflow by asking a natural-language question in the Now Assist panel. The workflow resolves the CI class and surfaces the attributes that Discovery is responsible for populating. The administrator selects the attribute to investigate. The workflow then identifies affected CI records with the selected attribute missing, parses the relevant discovery logs to identify the root cause, and suggests a remediation.

The workflow uses two agents:

-   Pattern diagnostic agent: Receives the administrator's query and runs script tools autonomously to investigate the missing attribute.
-   EF Remediation Agent: Receives the identified root cause and suggests a remediation.

## Scope

The workflow covers attribute coverage gaps for CI classes discovered through pattern-based Discovery. The following conditions apply:

-   Only CIs discovered through patterns are supported for analysis.
-   Analysis is based on the pattern metadata table \(sn\_disco\_ai\_pattern\_metadata\). This table contains metadata about the patterns populating a CI and its attributes. Only default pattern information is included; customizations made to patterns aren't considered.
-   Log analysis focuses on the first CI in the sample. If issues are found, the workflow reports them and stops. If no issues are found, it checks the next CI in the list, up to the sample limit of five.

## Examples

The following scenarios illustrate how the workflow handles different CI and pattern types.

-   **Scenario 1: Direct infrastructure \(Linux Server\)**

    The workflow investigates a missing `cpu_manufacturer` attribute on Linux Server CIs. The workflow resolves the CIs IP address and queries the discovery logs directly. It returns a full report with sample CIs investigated, link to CIs, root cause and remediation guidance.

-   **Scenario 2: Applicative pattern \(MySQL database\)**

    The workflow investigates a missing attribute on a MySQL database CI. MySQL CIs are discovered through their host servers. The workflow navigates the Runs on relationship to resolve the host server's IP address and queries the discovery logs on the host, not the MySQL instance. It returns a full report with sample CIs investigated, link to CIs, root cause and remediation guidance.

-   **Scenario 3: Cloud pattern \(AWS Auto Scaling Group\)**

    The workflow investigates a missing `cluster_connection` attribute on an AWS Auto Scaling Group CI. Cloud CIs use an SA-LDC identifier instead of a traditional IP address. The workflow navigates the Hosted on relationship to resolve the SA-LDC identifier and searches logs using the identifier and process ID. It returns a full report with sample CIs investigated, link to CIs, root cause and remediation guidance.


**Parent Topic:**[Use agentic AI in Now Assist for ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/now-assist-itom-ai-agent-workflows.md)

