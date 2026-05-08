---
title: Create process mining project for security incidents
description: Create a project in Process Mining Workspace using the pre-build process models definitions from the content pack to scan through audit logs of security incident records and identify inefficiencies in your security incident life cycle.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
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

    The **Step objectives** page opens.![Create a process mining project](../image/create-proc-min-proj-sir.png)

3.  Enter a process mining project name in **Name**.

4.  Add a short description about your project in **Short Description**.

5.  Select **Source Type** as Table.

6.  Select the `Security Incident (sn_si_incident)` in **Table**.

7.  Select the default template, and then select **Create project**.

    The project dashboard appears with all the configured settings.

8.  Select the edit \(![Edit icon](../image/icon-edit.png)\) icon corresponding to **Scope of the analysis** and configure the filters to set the number of records to mine.

    ![Process mining filter settings](../image/proc-min-filter-sir.png)

9.  Select **Select improvement opportunities** and configure the improvements for your security incidents.

    A list of improvement opportunities displays. For information about configuring improvement opportunities, see Setting improvement opportunities.

10. Select **Review and mine** and then select **Mine project**.

11. Select **Sample mine** or **Full mine**.

12. Select **Confirm &amp; Mine** to start the mining.

    The mining starts and the status of mining is displayed.


