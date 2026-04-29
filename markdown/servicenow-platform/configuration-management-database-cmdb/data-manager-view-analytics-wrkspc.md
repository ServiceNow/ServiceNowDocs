---
title: View CMDB Data Manager analytics
description: The CMDB Data Manager in CMDB Workspace and in Service Graph Workspace, provides charts and counts that show the overall state of Data Manager policies in the organization. Review these details to track progress and to identify any problems that require your attention.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administer CMDB Data Manager, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View CMDB Data Manager analytics

The CMDB Data Manager in CMDB Workspaceand in Service Graph Workspace, provides charts and counts that show the overall state of Data Manager policies in the organization. Review these details to track progress and to identify any problems that require your attention.

## Before you begin

Role required: data\_manager\_admin or sn\_cmdb\_admin

## Procedure

1.  Open either workspace:

    -   Navigate to **Workspaces** &gt; **CMDB Workspace** and then select the **Data Manager** quick link on the Home view.
    -   Navigate to **Workspaces** &gt; **Service Graph Workspace** and in the navigation panel, select the Governance icon. Then, in the Governance navigation pane, select **Data Manager overview**.
2.  Select **Analytics** in the left-side bar.

    The Data Manager analytics page provides the following charts:

    -   **CIs processed by lifecycle policies**

        Counts of CIs processed by each type of life-cycle policy type such as Delete and Archive, over the past six months.

    -   **Average time to close tasks**

        Average number of days it took to close tasks, by general policy type such as life-cycle and attestation, over the past six months.

    -   **Closed complete vs closed incomplete tasks**

        Number of tasks per month that were closed complete and incomplete over the past year.

    -   **Policy execution time**

        Number of policies per day, broken by the length of execution time, over the past month.


