---
title: Upgrade the MID Server manually
description: MID Servers automatically upgrade to match the instance build the next time they communicate with the instance after an instance upgrade. Use this procedure only if you want to upgrade a MID Server immediately or retry the upgrade after an Upgrade failed status.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/mid-server/t\_UpgradeTheMIDServerManually.html
release: australia
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [MID Server upgrades, MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Upgrade the MID Server manually

MID Servers automatically upgrade to match the instance build the next time they communicate with the instance after an instance upgrade. Use this procedure only if you want to upgrade a MID Server immediately or retry the upgrade after an Upgrade failed status.

## Before you begin

Role required: agent\_admin or admin

For the upgrade to run, MID servers must be in the **Up** state and [validated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_ValidateAMIDServer.md), or in the **Upgrade failed** state. The MID Server automatically runs the [pre-upgrade test](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-pre-upgrade-check.md) before upgrading. Any errors encountered during this test must be resolved for the upgrade to proceed.

**Warning:** If the MID Server version is significantly behind the instance version \(for example, multiple releases behind\), the automatic upgrade mechanism may fail. In this case, perform a fresh MID Server installation instead of an upgrade. See the [Windows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-install-prereqs.md) or [Linux](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_InstallAMIDServerOnLinux.md) installation tasks. Do not uninstall the MID Server until the new version is validated.

## About this task

The MID Server is upgraded to the version specified by build stamp on the instance, or by the [upgrade property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-version-selection.md) that you specify.

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **MID Servers** or **Orchestration** &gt; **MID Server Configuration** &gt; **MID Servers**.

    If **Discovery** or **Orchestration** is not active, enter `ecc_agent.list` in the navigation filter to view the list of MID Servers.

2.  Open the record of the MID Server that you want to upgrade.

3.  Click **Upgrade MID** under **Related Links**.

    If **Upgrade MID** does not appear under **Related Links**, verify that the MID Server is **Up** and validated, or that the MID Server is in the **Upgrade failed** state.

4.  Confirm that you want to perform the upgrade.


**Parent Topic:**[MID Server upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/c_UpgradeAndTestMIDServer.md)

