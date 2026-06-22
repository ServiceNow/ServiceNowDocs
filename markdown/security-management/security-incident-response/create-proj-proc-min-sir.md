---
title: Create process mining project for security incidents
description: Create a project in Process Mining Workspace using the pre-build process models definitions from the content pack to scan through audit logs of security incident records and identify inefficiencies in your security incident life cycle.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-incident-response/create-proj-proc-min-sir.html
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Process Mining Workspace for Security Incident Response, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create process mining project for security incidents

Create a project in Process Mining Workspace using the pre-build process models definitions from the content pack to scan through audit logs of security incident records and identify inefficiencies in your security incident life cycle.

## Before you begin

Role required: sn\_process\_optimization\_analyst and sn\_si\_read

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Process Mining Workspace**.

2.  Select **Create New Project**.

    The **Step objectives** page opens.\[Omitted image "create-proc-min-proj-sir.png"\] Alt text: Create a process mining project

3.  Enter a process mining project name in **Name**.

4.  Add a short description about your project in **Short Description**.

5.  Select **Source Type** as Table.

6.  Select the `Security Incident (sn_si_incident)` in **Table**.

7.  Select the default template, and then select **Create project**.

    The project dashboard appears with all the configured settings.

8.  Select the edit \(\[Omitted image "icon-edit.png"\] Alt text: Edit icon\) icon corresponding to **Scope of the analysis** and configure the filters to set the number of records to mine.

    \[Omitted image "proc-min-filter-sir.png"\] Alt text: Process mining filter settings

9.  Select **Select improvement opportunities** and configure the improvements for your security incidents.

    A list of improvement opportunities displays. For information about configuring improvement opportunities, see [Working with improvement opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/process-mining/working-with-imp-opp.md).

10. Select **Review and mine** and then select **Mine project**.

11. Select **Sample mine** or **Full mine**.

12. Select **Confirm &amp; Mine** to start the mining.

    The mining starts and the status of mining is displayed.


