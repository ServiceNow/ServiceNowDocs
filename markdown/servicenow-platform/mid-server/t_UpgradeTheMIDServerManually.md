---
title: Upgrade the MID Server manually
description: You can manually upgrade MID Servers at any time if you do not want to wait for the automatic upgrade.
locale: en-US
release: zurich
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [MID Server upgrades, MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Upgrade the MID Server manually

You can manually upgrade MID Servers at any time if you do not want to wait for the automatic upgrade.

## Before you begin

Role required: mid\_server or admin

For the upgrade to run, MID servers must be in the **Up** state and must be [validated](t_ValidateAMIDServer.md). The MID Server automatically runs the [pre-upgrade test](../reference/mid-server-pre-upgrade-check.md) before upgrading. Any errors encountered during this test must be resolved for the upgrade to proceed.

## About this task

The MID Server is upgraded to the version specified by build stamp on the instance, or by the [upgrade property](../reference/mid-server-version-selection.md) that you specify.

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **MID Servers** or **Orchestration** &gt; **MID Server Configuration** &gt; **MID Servers**.

2.  Open the record of the MID Server that you want to upgrade.

3.  Click **Upgrade MID** under **Related Links**.

4.  Confirm that you want to perform the upgrade.


**Parent Topic:**[MID Server upgrades](../concept/c_UpgradeAndTestMIDServer.md)

