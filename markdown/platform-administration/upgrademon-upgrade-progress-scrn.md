---
title: Upgrade Progress
description: When an upgrade is underway, Upgrade Progress displays progress bars and other information to help monitor the process.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Monitor an upgrade to an instance, Upgrade Monitor module: Upgrade an individual instance, Upgrades and conversions, Upgrade, Administer the ServiceNow AI Platform]
---

# Upgrade Progress

When an upgrade is underway, Upgrade Progress displays progress bars and other information to help monitor the process.

![Upgrade progress screen](../image/upgrade-progress-01-small.png "Upgrade Progress")

<table><thead><tr><th>

Screen element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Upgrade Progress

</td><td>

A progress bar depicting where the upgrade is in the overall process. The length of a section in the bar does not indicate the relative duration of that process.

</td></tr><tr><td>

Upgrade Progress: Upgrading Platform

</td><td>

The system is applying upgrades to elements that form the foundation of the platform.

</td></tr><tr><td>

Upgrade Progress: Updating Schema

</td><td>

The system is scanning the plugins to create a list of tables that require upgrading. This prevents the system from upgrading the same table multiple times.

</td></tr><tr><td>

Upgrade Progress: Loading Plugins

</td><td>

The system is loading both core and optional plugins. Some features require more than one plugin, so the number of plugins listed may not match the number of optional features installed.

</td></tr><tr><td>

Upgrade Progress: Completing

</td><td>

The system is upgrading components that need to be completed after the previous three stages are done. **Note:** After the system finishes the Completing phase, it displays a separate screen showing Finalizing. The system tracks in update sets the changes made during the Upgrading Platform, Updating Schema, Loading Plugins, and Completing phases. It does not track changes made during Finalizing.

</td></tr><tr><td>

Details

</td><td>

Shows the current activity, a progress bar for the current activity, and the file currently being updated.

</td></tr><tr id="phd_1pz_dx"><td>

Node Upgrades

</td><td>

The color of the icons represents the status of each node during this upgrade: Pending, Running, Successful, Failed, or Down.

</td></tr><tr id="l3d_1pz_dx"><td>

Node

</td><td>

The selected node indicated by the arrow. To change the selection, position the mouse cursor over the icon for the node to select.

</td></tr><tr id="cjd_1pz_dx"><td>

Running time

</td><td>

How long the selected node \(indicated by the arrow\) has been running. If the selected node is offline, this value stops updating and shows how long a node was online before going offline.

</td></tr><tr id="qjd_1pz_dx"><td>

Version

</td><td>

The current build for the selected node \(indicated by the arrow\).

</td></tr><tr id="ekd_1pz_dx"><td>

Successful upgrade

</td><td>

When the selected node is online, shows how long the node has been online. If the selected node is offline, shows how long the node has been offline.

</td></tr></tbody>
</table>**Parent Topic:**[Monitor an upgrade to an instance](../task/monitor-upgrade-apply-upgrade.md)

