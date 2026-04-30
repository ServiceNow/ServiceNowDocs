---
title: Disable the org chart
description: Disable your organizational chart either for a particular deployment channel or for the instance.
locale: en-US
release: zurich
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-11-14"
reading_time_minutes: 1
breadcrumb: [Configuring assistants overview, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Disable the org chart

Disable your organizational chart either for a particular deployment channel or for the instance.

## Before you begin

Role required: admin

## About this task

The org chart displays in the Virtual Agent's interactive view whenever you open a people citation's popover. You can disable the org chart so that it doesn’t display as an option in the people citation's popover.

## Procedure

1.  Decide whether you want to disable the interactive view's org chart at the deployment level or instance level.

2.  Choose one of the following scenario's and complete the steps.

<table id="choicetable_tpb_mgr_hhc"><thead><tr><th align="left" id="d48894e68">

Scenario

</th><th align="left" id="d48894e71">

Steps

</th></tr></thead><tbody><tr><td id="d48894e77">

**Disable the org chart at deployment channel level**

</td><td>

1.  Navigate to the M2M Canvas Configuration Deployment Channels table \[m2m\_canvas\_configuration\_deployment\_channel.list\].
2.  Select **New**.
3.  Search and select the relevant deployment channel in the **Deployment Channel** field.
4.  Set the **Canvas Configuration** field to `af3b113c3b0932102e3df80864e45a12`.
5.  Clear the **Active** check box.
6.  Select **Submit**.


</td></tr><tr><td id="d48894e126">

**Disable the org chart at the instance level**

</td><td>

1.  Navigate to the Now Canvas Configuration table \[sn\_now\_canvas\_configuration.list\].
2.  Find the row with canvas ID set to `sys_id=af3b113c3b0932102e3df80864e45a12`, and then change the Active column from `true` to `false`.


</td></tr></tbody>
</table>
