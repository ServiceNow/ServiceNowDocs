---
title: Set the system property for the OT Network Map
description: Set the Max CI Nodes per Site \(sn\_ot\_core.node\_map.max\_ci\_nodes\_per\_site\) system property to determine the maximum number of configuration item \(CI\) nodes shown per site on the OT Network Map.
locale: en-US
release: australia
product: Industrial Workspace
classification: industrial-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up the OT Network Map, Configure, Industrial Workspace, Operational Technology]
---

# Set the system property for the OT Network Map

Set the **Max CI Nodes per Site \(sn\_ot\_core.node\_map.max\_ci\_nodes\_per\_site\)** system property to determine the maximum number of configuration item \(CI\) nodes shown per site on the OT Network Map.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All**.

2.  Select the **sn\_ot\_core.node\_map.max\_ci\_nodes\_per\_site** system property record.

    To find this system property, you can set a filter by selecting the **Show / hide filter** ![](../../mftg-manufacturing-process-mgr/image/filter-list-icon.png) icon and applying a **\[Name\] \[is\] \[sn\_ot\_core.node\_map.max\_ci\_nodes\_per\_site\]** filter value.

3.  If needed, edit the **Value** field to change the number of CI nodes shown per site.

    **Note:** The default value is 10K. If a site has more than 10K CIs, then the additional CIs aren't considered in the network map calculations.

4.  Select **Update**.


**Parent Topic:**[Setting up the OT Network Map](../concept/setting-up-ot-network-map.md)

