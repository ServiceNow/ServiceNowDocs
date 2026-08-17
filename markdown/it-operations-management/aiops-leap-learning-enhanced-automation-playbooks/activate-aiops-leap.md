---
title: Activate LEAP
description: Activate the LEAP skill after installing the application to assemble and categorize incidents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/activate-aiops-leap.html
release: zurich
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Learning Enhanced Automation Platform \(LEAP\), ServiceNow Otto for ITOM, IT Operations Management]
---

# Activate LEAP

Activate the LEAP skill after installing the application to assemble and categorize incidents.

## Before you begin

Role required: System admin or LEAP admin

and the application scope must be LEAP.

## Procedure

1.  Navigate to **Workspaces** &gt; **LEAP**.

2.  Select **Admin** &gt; **AI Admin Hub**.

3.  Select **AI Skills** &gt; **Platform** &gt; **LEAP**.

4.  On the LEAP Installer card, select **Activate**.

5.  In the LEAP installer input section, enter the details for LEAP to run scans on existing records, and select **Save and continue**.

    For details on installer fields, see [LEAP Installer fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/aiops-leap-installation-fields.md)

6.  In the Define access section, select the role to whom you want to provide access to LEAP skills.

7.  In the Select display section of LEAP installer, select the required display and select **Save and continue**.

8.  In the Review and activate section of LEAP installer,review the selections, and select **Activate**.

9.  Select **Return to LEAP** on the success message.

10. The grouping job starts and proceeds to group records into automation opportunities.\[Omitted image "grouping-job-run.png"\] Alt text: landing page with analysis data

    If errors are encountered, then LEAP provides links to knowledge base articles to understand the root cause and steps to resolve issues.


