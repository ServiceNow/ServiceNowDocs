---
title: Validate the MID Server
description: You must manually validate the MID Server after it is installed to enable it to execute automation tasks. You can invalidate a MID Server you suspect has been compromised to prevent it from accessing automation credentials in the instance or executing outbound ECC probes.
locale: en-US
release: xanadu
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Installing the MID Server, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Validate the MID Server

You must manually validate the MID Server after it is installed to enable it to execute automation tasks. You can invalidate a MID Server you suspect has been compromised to prevent it from accessing automation credentials in the instance or executing outbound ECC probes.

## Before you begin

Role required: agent\_admin, admin

<table id="table_nds_2s4_nhb"><tbody><tr><td>

![Set up indicator for installation phase](../image/ProgressBarInstall.png)

</td></tr></tbody>
</table>Make sure that the [MID Server version](../concept/mid-server-landing.md) is compatible with the instance.

## About this task

Validation restricts access to automation credentials to trusted MID servers only.

When you validate a MID Server, you specify the capabilities it can use, the applications that use it, and the IP ranges it is allowed to explore. You will be prompted to set the initial selection criteria when you validate MID Servers that do not already have capabilities, applications, or IP ranges already configured. You do not have to set the initial selection criteria to actually validate the MID Server. See [MID Server selection](../concept/c_MIDServerSelector.md) for more information on capabilities, applications, and IP ranges.

**Note:** When you upgrade, MID Servers that are already configured in your instance are automatically validated. This prevents the interruption of automation tasks that MID Servers might be performing. See [MID Server upgrades](../concept/c_UpgradeAndTestMIDServer.md) for more information.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Servers**.

2.  Open the new MID Server you created from the list of MID Servers.

3.  Under **Related Links** click **Validate**.

    The Set Initial Selection Criteria window appears if there are no records in the Supported Applications, IP Ranges, or Capabilities related lists.

4.  On the Set Initial Selection Criteria window, use the switches to enable or disable selection criteria for this MID Server:

    -   **Allow ALL capabilities**: Allow all capabilities for Orchestration and Event Management to use this MID Server.

        **Note:** Service Mapping and Event Management alert aggregation and RCA, which used capabilities in previous releases, rely on the application for MID Server selection.

    -   **Allow ALL applications**: Allow all applications that use MID Servers to use this MID Server.
    -   **Allow ALL IP ranges**: Make all IP ranges valid for this MID Server, meaning that it can target any IP address.
    ![Set initial selection criteria](../image/setInitialSelectionCriteria.png "Setting initial selection criteria")

    If you click **Cancel**, the validation continues but none of the capabilities, applications, or IP ranges are added.

5.  Click **OK**.

    The **Validated** field on the dashboard is set to **Validating**, and then set to **Yes** after the validation completes.

6.  To invalidate a MID Server, open the record for the MID Server you suspect has a security issue.

7.  Under **Related Links**, click **Invalidate**.

    Invalidating a MID Server forces it to clear its memory and restart. The MID Server generates a new keypair on restart.


## What to do next

[Test network connectivity](t_ValidateNetworkConnectivity.md) to ensure that the MID Server can upgrade automatically.

**Related topics**  


[Rekey a MID Server](t_RekeyAMIDServer.md)

