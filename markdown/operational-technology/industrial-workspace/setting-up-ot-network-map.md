---
title: Setting up the OT Network Map
description: Set up the Operational Technology \(OT\) Network Map so that you can access the map in the in the Industrial Workspace.
locale: en-US
release: zurich
product: Industrial Workspace
classification: industrial-workspace
topic_type: concept
last_updated: "2026-02-12"
reading_time_minutes: 1
breadcrumb: [Configure, Industrial Workspace, Operational Technology]
---

# Setting up the OT Network Map

Set up the Operational Technology \(OT\) Network Map so that you can access the map in the in the Industrial Workspace.

The following table lists the setup tasks for the OT Network Map. The admin role is required.

|Task|Purpose|
|----|-------|
|[Run the OT Network Map Cache Handler scheduled job](../task/run-ot-network-map-cache-handler-scheduled-job.md)|Configure this scheduled job to run after your Service Graph Connectors to populate the latest data to show in Node Map.|
|[Set the system property for the OT Network Map](../task/set-the-system-property-ot-network-map.md)|Set the **Max CI Nodes per Site \(sn\_ot\_core.node\_map.max\_ci\_nodes\_per\_site\)** system property to determine the maximum number of CI nodes shown per site on the network map.|

-   **[Run the OT Network Map Cache Handler scheduled job](../task/run-ot-network-map-cache-handler-scheduled-job.md)**  
Configure this scheduled job to run after your Service Graph Connectors to populate the latest data to show in the OT Network Map.
-   **[Set the system property for the OT Network Map](../task/set-the-system-property-ot-network-map.md)**  
Set the **Max CI Nodes per Site \(sn\_ot\_core.node\_map.max\_ci\_nodes\_per\_site\)** system property to determine the maximum number of configuration item \(CI\) nodes shown per site on the OT Network Map.

**Parent Topic:**[Configuring the Industrial Workspace](../../operational-technology-management/concept/configuring-industrial-workspace.md)

