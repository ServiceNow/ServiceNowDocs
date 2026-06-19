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
breadcrumb: [Configuring LEAP, Learning Enhanced Automation Platform \(LEAP\), Now Assist for ITOM, IT Operations Management]
---

# Activate LEAP

Activate the LEAP skill after installing the application to assemble and categorize incidents.

## Before you begin

Role required: System admin or LEAP admin

and the application scope must be LEAP.

## Procedure

1.  Activate **LEAP** with one of the following options.

<table id="choicetable_bng_jxt_q2c"><thead><tr><th align="left" id="d206993e95">

Options

</th><th align="left" id="d206993e100">

Steps

</th></tr></thead><tbody><tr><td id="d206993e107">

**Workspaces**

</td><td>

1.  Navigate to **Workspaces** &gt; **LEAP**.
2.  Select **Now Assist Admin Workspace**.
3.  On the LEAP installer card, select **Activate skill**.


</td></tr><tr><td id="d206993e149">

**Now Assist Admin**

</td><td>

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.
2.  In the workflow list under Technology, select **ITOM**.
3.  On the LEAP installer card, select **Activate skill**.


</td></tr></tbody>
</table>2.  In the LEAP installer input section, enter the details for LEAP to run scans on existing records, and select **Save and continue**.

    For details on installer fields, see [LEAP Installer fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/aiops-leap-installation-fields.md)

3.  In the Define access section, select the role to whom you want to provide access to LEAP skills.

4.  In the Select display section of LEAP installer, select the required display and select **Save and continue**.

5.  In the Review and activate section of LEAP installer,review the selections, and select **Activate**.

6.  Select **Return to ITOM** on the success message.

7.  The grouping job starts and proceeds to group records into automation opportunities.\[Omitted image "grouping-job-run.png"\] Alt text: landing page with analysis data

    If errors are encountered, then LEAP provides links to knowledge base articles to understand the root cause and steps to resolve issues.


