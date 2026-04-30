---
title: Upgrade Kubernetes Visibility Agent Informers remotely
description: Upgrade Kubernetes Visibility Agent Informer pods in Kubernetes clusters remotely from the ServiceNow Instance to avoid dependence on your Kubernetes admin. You can upgrade a single Informer or multiple Informers together.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Agent Client Collector, Kubernetes, Visibility, Informer, upgrade, remote, Cloud Native Operations for Visibility, CNO for Visibility]
breadcrumb: [Install Kubernetes Visibility Agent \(KVA\), Configuring Kubernetes Visibility Agent, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Upgrade Kubernetes Visibility Agent Informers remotely

Upgrade Kubernetes Visibility Agent Informer pods in Kubernetes clusters remotely from the ServiceNow Instance to avoid dependence on your Kubernetes admin. You can upgrade a single Informer or multiple Informers together.

## Before you begin

Role required: discovery\_admin

## Procedure

1.  Navigate to **All** &gt; **Kubernetes Visibility Agent** &gt; **Properties**.

2.  In the **Kubernetes Visibility Agent Image** field, set the image to which you want to upgrade Informers that are currently running, and then select **Save**.

    Use the following format: repository:tag. For example: `servicenowdocker/informer:2.1.1`.

3.  Navigate to **All** &gt; **Kubernetes Visibility Agent** &gt; **Home**.

4.  In the Kubernetes Informers list, perform the relevant steps to upgrade one Informer or several Informers concurrently.

    **Note:** Only Informers with the value Upgrade Pending in the **Upgrade Status** field can be upgraded. The running status of the Informers must be either Up or Paused.

<table id="choicetable_l24_ctl_sbc"><thead><tr><th align="left" id="d74572e157">

Upgrade

</th><th align="left" id="d74572e160">

Steps

</th></tr></thead><tbody><tr><td id="d74572e166">

**One Informer**

</td><td>

1.  Select the Informer in the list to display its form.
2.  In the Related Links section of the form, select **Upgrade Informer**.


</td></tr><tr><td id="d74572e187">

**Multiple Informers**

</td><td>

1.  Select multiple Informers in the list.
2.  From the **Actions on selected rows...** list menu, select the **Upgrade Informers** menu item.


</td></tr></tbody>
</table>    The upgrade process begins, and the **Upgrade Status** field for each selected Informer displays the value Upgrading. The system downloads the new image and starts the new pod for each selected Informer.

    When an upgraded pod connects to the Instance, the **Informer Version** field displays the new version number. The **Upgrade Status** field displays Desired image in use.


**Parent Topic:**[Install Kubernetes Visibility Agent \(KVA\)](cnov-deploy-install.md)

