---
title: Discover java installation data using Agent Client Collector for Visibility - Content file-based discovery
description: Discovering java installation data using Agent Client Collector for Visibility - Content file-based discovery enables you to discover file information in your system.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Application patterns for the Agent Client Collector, ACC Discovery, ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Discover java installation data using Agent Client Collector for Visibility - Content file-based discovery

Discovering java installation data using Agent Client Collector for Visibility - Content file-based discovery enables you to discover file information in your system.

## Before you begin

-   Install the latest version of Agent Client Collector for Visibility - Content.
-   Install file-based discovery.
-   Enable the Oracle Global License Advisory Services \(GLAS\) hardware data collection policy.

Role required: discovery\_admin

## Procedure

1.  Enable file-based discovery.

    1.  Navigate to **All** &gt; **Discovery Definition** &gt; **Configuration Console**.

    2.  Enable the **File Discovery** entry.

2.  Enable the Java Discovery property.

    1.  Locate the **sn\_acc\_vis\_content.file\_discovery.enable\_java\_discovery** property on the System Properties page \(**All** &gt; **System Properties** &gt; **All Properties**\).

    2.  Set the property value to **true**.

3.  Grant elevated permissions to the `acc` user, enabling access to your java installation directories, for example:

    -   `/usr/lib/jvm/*/bin/java`
    -   `/usr/lib/jvm/*/*/bin/java`
    You can add additional java directories during java installation, as needed.

    -   In a Linux environment, grant elevated permissions in the `/etc/sudoers` file to enable access to the java installation directories.
    -   In a Windows environment, grant elevated permissions \(read and execute\) via the system administrator to enable access to the java installation directories.

## Result

When running Discovery for java installation, data is discovered through file-based discovery and is stored in the `ora_java_audit` table. For details on the data stored in this table, see [Data collected during Agent Client Collector for Visibility - Content file-based Discovery](../reference/data-collected-file-based-discovery.md).

**Parent Topic:**[Application patterns for the Agent Client Collector](../concept/application-patterns-acc.md)

