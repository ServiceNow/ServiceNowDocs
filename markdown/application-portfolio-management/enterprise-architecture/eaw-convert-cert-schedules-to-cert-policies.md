---
title: Import certification schedules in to Data Manager
description: To convert the existing certification schedules to certification policies, you must import the certification schedules into Data Manager.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-portfolio-management/enterprise-architecture/eaw-convert-cert-schedules-to-cert-policies.html
release: xanadu
product: Enterprise Architecture
classification: enterprise-architecture
topic_type: task
last_updated: "2025-04-18"
reading_time_minutes: 1
breadcrumb: [Configure certification policies, Work with the Setup page in the Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Import certification schedules in to Data Manager

To convert the existing certification schedules to certification policies, you must import the certification schedules into Data Manager.

## Before you begin

Role required: system administrator

## About this task

This process converts the certification schedules into draft certification policies and you can then publish these policies to activate them.

**Note:** If you upgraded your EA Workspace from a previous version to the 4.0.0 version, you might see that your certification data is still fetched from the Certification Schedules \(cert\_schedule\) table. Follow these instructions to import your data certification schedules to certification policies.

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **CMDB Workspace**.

2.  Select **Management** in the CMDB Workspace menu bar.

3.  Select the Data Manager link in Management tools, in the Manage section.

    \[Omitted image "cmdb-datamangement.png"\] Alt text:

4.  On the Data Manager overview page, select **Import** on the banner at the top of the page.

    **Note:** If all the certification schedules are already imported, the Import banner doesn’t appear. You can see the imported policies in the Draft policies tab \(refer to step 6\).

5.  In the Confirm import of certification schedule into draft policies, select **Import into draft policies**.

    \[Omitted image "cmdb-import-cert-schedules.png"\] Alt text:

6.  In the Import summary modal, select **View draft policies**.

    The converted policies appear in the Data Manager policies page, under the Draft policies tab.\[Omitted image "cmdb-draft-policies.png"\] Alt text:

7.  Publish the draft policies to activate them.

    For more information, see [Publish a draft Data Manager policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-portfolio-management/enterprise-architecture/eaw-publish-a-draft-policy.md).


**Parent Topic:**[Configure certification policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-portfolio-management/enterprise-architecture/eaw-config-cert-schedules.md)

