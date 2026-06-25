---
title: Run procdump flow
description: The Run procdump flow runs a process dump on a specified process and saves it to a file that can be targeted by security analysts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/invoke\_procdump.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Incident Response Orchestration workflows and activities, Understand Security Incident Response Orchestration workflows and workflow templates, Security Incident Response Orchestration, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Run procdump flow

The **Run procdump** flow runs a process dump on a specified process and saves it to a file that can be targeted by security analysts.

Role required: sn\_si.analyst

This flow is triggered when enriched processes are selected and a **Run procdump** UI action is executed.

\[Omitted image "run-procdump-flow.png"\] Alt text: Run Procdump Flow

Reasons the procdump can fail includes:

-   Invalid dump path
-   Invalid file share path
-   Unable to fetch the fully-qualified domin name of the Windows machine the procdump is running on
-   The process name is not specified
-   The PROCDUMP environment variable not found
-   A copy of the dump file fails to copy from the dump path to the file share path

-   **[Execute procdump action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/execute_procdump.md)**  
**Execute procdump** is a powershell action that runs the procdump on the selected processes, dumps the data into a file, and posts it to a shared site on an internal network. An analyst can then view a deny listed process, highlighted in red in a security incident, and perform additional analysis on the file.

**Parent Topic:**[Security Incident Response Orchestration workflows and activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/sec-inc-resp-orchestration-workflows.md)

**Related topics**  


[Create Lookup Request for IoC Changes workflow]()

[Security Incident Response- Get Network Statistics flow]()

[Security Incident Response - Get Running Services workflow]()

[Security Incident - Evaluate response task outcome workflow]()

