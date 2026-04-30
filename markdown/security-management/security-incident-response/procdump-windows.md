---
title: Invoke a process dump for an enriched process in Windows
description: A security analyst can run a process dump on a specific process, dump it into a file, and post it to a shared site on an internal network. An analyst can then view a deny listed process, highlighted in red in a security incident, and perform additional analysis.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Invoke a process dump for an enriched process in Windows

A security analyst can run a process dump on a specific process, dump it into a file, and post it to a shared site on an internal network. An analyst can then view a deny listed process, highlighted in red in a security incident, and perform additional analysis.

## Before you begin

The following are required:

-   A client running Windows Vista or higher, or a server running Windows Server 2008 or higher.
-   The ProcDump command-line utility installed, with a system environment variable that points to the procdump executable file path. The name of the variable must be PROCDUMP. This name is used in a powershell script.

Role required: sn\_si.analyst

## Procedure

1.  Navigate to the security incident with the enriched process on which you want to invoke a procdump by clicking **All** &gt; **Security Incident** &gt; **Show Open Incidents**, and open a security incident.

2.  Click the **Enrichment Data** tab.

3.  Click the **Retrieve Running Processes** enrichment record.

4.  Select the check boxes for the running processes you want to perform a procdump for, click the Actions on selected rows drop-down list at the bottom of the list, and click **Run Procdump**.

    An **Initiated prodump workflow for selected process** message appears at the top of the list, and the **Security Incident Response - Run procdump** workflow executes.


