---
title: Onboard Argo CD to DevOps Change Velocity — Classic
description: Connect your Argo CD instance using the Classic UI in DevOps Change Velocity.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Argo CD, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Argo CD to DevOps Change Velocity — Classic

Connect your Argo CD instance using the Classic UI in DevOps Change Velocity.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **DevOps &gt; Tools &gt; Create New \(legacy\)** and create a record.

2.  Enter a **Tool Name** and fill in the tool details.

<table id="table_jfq_lwn_2tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tool integration

</td><td>

Tool to integrate. In this case, select **Argo CD**.

</td></tr><tr><td>

Tool URL

</td><td>

URL of the existing Argo CD instance to integrate.

For example:

https://argocd.k8s.sndevops.xyz/

</td></tr><tr><td>

Tool username

</td><td>

Username of your Argo CD instance.

</td></tr><tr><td>

Tool password

</td><td>

Password of your Argo CD instance.

</td></tr></tbody>
</table>3.  Select **MID Server** for an on-premises tool that is attached to a MID Server.

    Application is automatically set to DevOps and capability is set to REST.

4.  Select **Submit**.

    The tool is automatically Connected Successfully using a connection alias, and HTTP tool connection \(basic authentication credential\).


**Parent Topic:**[Argo CD integration with DevOps Change Velocity](../concept/argo-cd-integration-with-devops-change-velocity.md)

