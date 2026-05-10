---
title: Modify tracking changes in configuration files
description: Configure the system to collect information about changes in configuration files belonging to a configuration item \(CI\). Service Mapping uses this information to notify users that CI configuration files changed and to view actual changes to configuration files directly in the service instance maps.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 3
breadcrumb: [Configuration file tracking, Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Modify tracking changes in configuration files

Configure the system to collect information about changes in configuration files belonging to a configuration item \(CI\). Service Mapping uses this information to notify users that CI configuration files changed and to view actual changes to configuration files directly in the service instance maps.

## Before you begin

To enable tracking configuration files for a CI for which the system does track files, configure classification for the CI type to which this CI belongs:

-   For CI types representing applications, [create a Discovery process classification](t_CreateAProcessClassification.md) for the relevant pattern. Add the [Horizontal Pattern](../reference/r-HorizontalPatternProbe.md) probe in the **Probe** column, and then specify your pattern in the **Pattern** column.
-   For CI types representing SNMP devices, perform configuration as described in [Create a Discovery CI classification](create-discovery-ci-classification.md).

**Note:** There is no need to create CI classifications for hosts because these classifications are included in the base system.

Role required: cloud\_admin, service\_mapping\_admin, or admin

## About this task

The system tracks configuration files as part of horizontal discovery process of a CI to which these files belong. Configuration files contain CI settings and parameters. Service Mapping uses this information to notify users that CI configuration files changed and to view actual changes to configuration files directly in the service instance maps. To learn about how the system tracks configuration files, stores and updates information about these files, see [Configuration file tracking](../concept/tracked-config-files.md).

The system tracks configuration files for CI types with process classifiers that trigger patterns. The patterns contain tracked file definitions, which specify the CI type that the application belongs to and the path of the configuration file. Several patterns, such as the IIS pattern, provide tracked file definitions by default. You can use these default definitions or create your own for any pattern a process classifier triggers.

## Procedure

1.  Navigate to **All** &gt; **Pattern Designer** &gt; **Discovery Patterns**.

2.  Click the pattern for the relevant CI.

    **Important:** Enabling configuration file tracking does not modify the contents of a pattern.

3.  Click the **Tracked Files** tab.

    One or more tracked file definitions appear by default for Discovery [patterns that support configuration file tracking](../concept/tracked-config-files.md#patterns-for-file-tracking).

    If you do not see the Tracked Files tab, verify that the pattern is specified process classier. See [Add the Horizontal Pattern probe to a classifier](../concept/c-UsingPatternsForHorizontalDiscovery.md#) for instructions.

4.  Click **Edit** to modify an existing definition or click **New** to create a new one.

5.  Fill out or modify the form fields \(see table\):

    |Field|Description|
    |-----|-----------|
    |**CI Type**|Select either the primary or related CI type to which the configuration file belongs.|
    |**File Path**|Define the path of the configuration file to track. You can use pattern variables and wildcards. For example, for the following path: &lt;the folder with the "install\_directory" parameter&gt;/conf/&lt;any xml file&gt;, enter $install\_directory+"/conf/\*.xml"|
    |**Save Content**|Select this check box to make this file available for viewing and comparing directly the ServiceNow instance.|
    |**Active**|Select this check box to enable tracking of this configuration file.|

6.  Click **Done**.

7.  If necessary, set the tracked files deletion strategy as described in [Set the deletion strategy for tracked configuration files](set-config-file-deletion-strategy.md)


## What to do next

Run discovery on the hosts that are running the applications you want to discover with patterns, open the application CI record, and check the Tracked Configuration Files related list.

If you are using Service Mapping, verify that it started collecting information about changes to configuration files:

1.  Navigate to the service instance map containing the CIs.
2.  On the Changes tab, check that the list includes a record of the change you made. For example, that the configuration file was added, modified or deleted.

