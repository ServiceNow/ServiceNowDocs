---
title: List of components compatible with latest version
description: Learn about the list of components that are executed in their latest versions in the RPA Desktop Design Studio and robots, irrespective of the version they were used during the automation design.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# List of components compatible with latest version

Learn about the list of components that are executed in their latest versions in the RPA Desktop Design Studio and robots, irrespective of the version they were used during the automation design.

## Backward compatibility of plugins overview

Robotic Process Automation \(RPA\) solution is built with backward compatibility of plugins.

An automation built using the earlier plugin versions are compatible with a latest version. For example, if an automation is built using an earlier version of a plugin, 1.0, the RPA Desktop Design Studio, Attended Robot, and Unattended Robot applications run the automation by loading the plugin version 1.0.

If any newer version of a component is no longer compatible with its older versions, they’re documented in the release notes. For more information, see RPA Hub release notes and [RPA Plugin Bundle release notes](https://servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/platform-app-engine/store-rn-plat-app-rpa-plugin-bundle.html).

Additionally, any automation component interacting with RPA Hub APIs are only compatible with its own RPA Hub version. For example, if the component is released as part of Utah 4.1, then it’s compatible only for that version.

During the infrastructure upgrade for every family or store release \(Vancouver, for example\), use the MSI packages corresponding to the respective releases.

The following table lists the matrix defining the backward compatibility. In this table, N depicts the latest release version of the software and N-2 depicts two versions prior to it.

|Plugins|Backward compatibility|Comments|
|-------|----------------------|--------|
|RPA Desktop Design Studio|N| |
|Unattended Robot|N| |
|Attended Robot|N| |
|Essential Toolkit|N-2|Except for RPA Hub components|
|Essential Connectors|N-2|Except for RPA Hub components|
|Windows|N-2| |
|Java|N-2| |
|Chromium \(Google and Edge\)|N-2| |
|Mainframe \(PCOMM\)|N-2| |
|FTP|N-2| |
|Barcode Reader|N-2| |
|Scripting|N-2| |
|Universal app connector|N-2| |

Few fundamental components that are essential to build the automation logic are excepted as these components are part of the RPA Desktop Design Studio.

## List of components

The following list of components are executed in their latest versions in the RPA Desktop Design Studio and robots, irrespective of the version they were used during the automation design.

|Category|Component|
|--------|---------|
|Conditions|Decision|
|Switch|
|Connectors|IdleTimer|
|System Events|
|Timer|
|General|Variable|
|Try Catch|
|Expression|
|Parallel|
|Terminate|
|MessageBox|
|Loops|Break|
|For Each|
|For Loop|
|While|
|RPA Hub|Log|
|Security|DPAPI|
|Utilities|Debug|
|Internal|ExecutionPoint|
|Start|
|End|
|UnknownComponent|
|RemoteActivity|
|VariableContainer|

**Parent Topic:**[Automation components](../concept/rpa-studio-automation-components.md)

