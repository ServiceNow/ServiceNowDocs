---
title: Run an attestation policy on-demand
description: Run an attestation policy in Service Graph Workspace or in CMDB Workspace, when needed, regardless of the policy recurring schedule. A manual, on-demand run doesn't interfere with the policy's specified schedule.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/configuration-management-database-cmdb/run-attestation-policy-ondemand.html
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-04-13"
reading_time_minutes: 1
breadcrumb: [CIs attestation, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Run an attestation policy on-demand

Run an attestation policy in Service Graph Workspace or in CMDB Workspace, when needed, regardless of the policy recurring schedule. A manual, on-demand run doesn't interfere with the policy's specified schedule.

## Before you begin

You can run on-demand only one policy at a time, and that policy, must not be actively running.

Role required: sn\_cmdb\_admin

## Procedure

1.  Navigate to either workspace:

    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**, and in the navigation panel select the Governance icon.
    -   Navigate to **Workspaces** &gt; **CMDB Workspace** and select **Management** in the CMDB Workspace menu bar.
2.  Select the **Data Manager** link in Management tools, in the Manage section.

3.  In the Data Manager navigation panel, select **Policies**.

4.  Run the policy using either of the following ways.

    -   In the Published policies tile, select the attestation policy that you want to run and then select **Run Policy**.
    -   In the Published policies tile, select the attestation policy that you want to run and then, on the policy details page, select **Run Policy**.
5.  In the Run Policy dialog box, select **Run**.


