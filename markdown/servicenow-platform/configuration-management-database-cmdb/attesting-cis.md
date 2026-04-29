---
title: CIs attestation
description: Verify the existence of actual IT infrastructure and applications that you own, systematically and in bulk. As CIs are continuously ingested into the CMDB from various data sources, ensure the integrity of the CMDB. Remove any stale CIs that are associated with IT infrastructure or applications that no longer exists.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CIs attestation

Verify the existence of actual IT infrastructure and applications that you own, systematically and in bulk. As CIs are continuously ingested into the CMDB from various data sources, ensure the integrity of the CMDB. Remove any stale CIs that are associated with IT infrastructure or applications that no longer exists.

Use the [CMDB Data Manager in CMDB Workspaceand in Service Graph Workspace](data-mgr-exp-cmdb-workspace.md) to [create an Attestation policy](../task/data-manager-create-policy-wrkspc.md), specifying CIs that need to be attested and the attestation frequency. Assign Attestation tasks to users that are familiar with or that manage the CIs, and who can attest or reject the IT infrastructure or applications that those CIs represent. Rejected CIs that are no longer needed can then be retired, archived, or deleted from the CMDB.

Users can go to the [My Work view in CMDB Workspace](cmdb-workspace-govern-view.md) or to the [Tasks view in Service Graph Workspace](sg-workspace-tasks-view.md) to see their assigned attestation tasks, and then [review and process the tasks](../task/review-data-manager-attes-task.md).

## Smart detection and auto-attestation

Smart detection streamlines and simplifies CI attestation. With smart detection you can auto-attest CIs that are automatically detected by discovery programs, based only on recent discovery results.

The following conditions must be met to enable smart detection:

-   [Discovery](https://www.servicenow.com/docs/access?context=r-discovery&version=australia&pubname=australia-it-operations-management&ft:locale=en-US) is enabled in your organization or [Getting started with Service Graph Connectors](cmdb-sgc-intro.md) are implemented.
-   The system property **sn\_cmdb\_ws.attestation.smart\_detection.disabled** is set to **false** \(default value\).

In addition, smart detection uses the following system properties as filters when creating a list of CIs that are candidates for auto-attestation. To be included as candidates for auto-attestation, CIs must be discovered:

-   Within the discovery time window specified by the **sn\_cmdb\_ws.attestation.smart\_detection.discovery\_window** system property \(for example, within the last 30 days\)
-   By any discovery source that isn't excluded by the **sn\_cmdb\_ws.attestation.smart\_detection.discovery\_source.exclusion** system property

Then, when you [review those candidate CIs](../task/review-data-manager-attes-task.md), you can choose to auto-attest them.

## Properties associated with Attestation

<table id="table_cny_5y4_ts"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_cmdb\_ws.attestation.smart\_detection.disabled

</td><td>

Disables smart detection.

 -   Type: true \| false
-   Default value: false
-   Values:
    -   **true**: Disable smart detection.
    -   **false**: Enable smart detection.
-   Location: [Add to System Properties \[sys\_properties\]](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) table.
-   Learn more: [Review CMDB Data Manager attestation tasks in CMDB Workspace or in Service Graph Workspace](../task/review-data-manager-attes-task.md)

</td></tr><tr><td>

sn\_cmdb\_ws.attestation.smart\_detection.discovery\_source.exclusion

</td><td>

Comma-separated list of discovery sources that are excluded in smart detection processing. For example, a data source that is unreliable in detecting CIs.

 CIs discovered by discovery sources in the list, can't be candidates for auto-attestation.

 -   Type: string
-   Default value: Manual Entry
-   Location: System property
-   Learn more: [Review CMDB Data Manager attestation tasks in CMDB Workspace or in Service Graph Workspace](../task/review-data-manager-attes-task.md)

</td></tr><tr><td>

sn\_cmdb\_ws.attestation.smart\_detection.discovery\_window

</td><td>

Number of days \(discovery window\) that smart detection uses to determine whether a CI is a candidate for auto-attestation. Only CIs that were discovered within this discovery window can be candidates for auto-attestation.

 -   Type: integer
-   Default value: 30
-   Location: System property
-   Learn more: [Review CMDB Data Manager attestation tasks in CMDB Workspace or in Service Graph Workspace](../task/review-data-manager-attes-task.md)

</td></tr></tbody>
</table>