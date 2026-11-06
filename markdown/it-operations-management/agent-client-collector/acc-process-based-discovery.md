---
title: Discover Java installation data using Agent Client Collector for Visibility Content Process-Based Discovery
description: Discover Java installation information in your system using Agent Client Collector for Visibility Content Process-Based Discovery \(PBD\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/agent-client-collector/acc-process-based-discovery.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-10-27"
reading_time_minutes: 2
keywords: [Java installation using PBD, Java installation using Agent Client Collector for Visibility Content]
breadcrumb: [ACC Discovery, ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Discover Java installation data using Agent Client Collector for Visibility Content Process-Based Discovery

Discover Java installation information in your system using Agent Client Collector for Visibility Content Process-Based Discovery \(PBD\).

## Before you begin

-   Install the latest version of Agent Client Collector for Visibility Content.
-   Install the Data Collection for Oracle Global Licensing and Advisory Services \(GLAS\) store app \(`sn_itom_oracleglas`\). Policy activation is blocked without this app.
-   If you want to collect GLAS hardware data, enable the GLAS hardware data collection policy. This data collection is controlled by the **sn\_acc\_vis\_content.file\_discovery.enable\_glas\_hw\_collection** property.
-   Role required: discovery\_admin

## About this task

Both File-Based Discovery \(FBD\) and PBD collect Oracle GLAS Java installation data and are supported in Linux, Windows, and macOS environments. PBD uses the **Oracle GLAS Java Process Discovery** policy, which runs weekly. FBD uses the `java_glas` stream and the **File Based Discovery Policy - Java GLAS** policy. For details about the FBD process, see [Discover Java installation data using Agent Client Collector for Visibility Content File-Based Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-file-based-discovery.md).

**Note:** The **Oracle GLAS Java Process Discovery** is available starting from Agent Client Collector for Visibility Content version 2.0.4.

## Procedure

1.  Activate the process-based discovery policy.

    1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Policies**.

    2.  Select **Oracle GLAS Java Process Discovery**.

    3.  Select **Activate**.

2.  Grant elevated permissions to the `acc` user, enabling access to your Java installation directories, for example:

    -   `/usr/lib/jvm/*/bin/java`
    -   `/usr/lib/jvm/*/*/bin/java`
    -   `/usr/lib/jvm/*/bin/jcmd`
    -   `/usr/lib/jvm/*/*/bin/jcmd`
    -   `/var/cache/servicenow/agent-client-collector/osquery/bin/osqueryi`
    You can add additional Java directories during Java installation, as needed.

    -   In a Linux environment, grant elevated permissions in the `/etc/sudoers` file to access the Java installation directories.
    -   In a Windows environment, grant elevated permissions \(read and execute\) via the system administrator to access the Java installation directories.

## Result

When you run Discovery for Java installation, process-based discovery stores the data in the `ora_java_audit` and `ora_java_evidence` tables. For details on the data stored in these tables, see [Data collected during Agent Client Collector for Visibility Content File-Based Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/data-collected-file-based-discovery.md).

**Parent Topic:**[Agent Client Collector Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-discovery.md)

**Related topics**  


[Discover Java installation data using Agent Client Collector for Visibility Content File-Based Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-file-based-discovery.md)

