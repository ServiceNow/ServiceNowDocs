---
title: Discover java installation data using Agent Client Collector for Visibility Content process-based discovery
description: Discovering java installation data using Agent Client Collector for Visibility Content process-based discovery enables you to discover java installation information in your system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-operations-management/agent-client-collector/acc-process-based-discovery.html
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-07-22"
reading_time_minutes: 1
breadcrumb: [Application patterns for the Agent Client Collector, Using Agent Client Collector for Visibility Content, Agent Client Collector for Visibility Content, Agent Client Collector, IT Operations Management]
---

# Discover java installation data using Agent Client Collector for Visibility Content process-based discovery

Discovering java installation data using Agent Client Collector for Visibility Content process-based discovery enables you to discover java installation information in your system.

## Before you begin

-   Install the latest version of Agent Client Collector for Visibility Content.
-   Enable the Oracle Global License Advisory Services \(GLAS\) hardware data collection policy.

Role required: discovery\_admin

## Procedure

1.  Enable the process-based discovery check definitions.

    1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Check Definitions**.

    2.  Locate the **Oracle GLAS Java Process Discovery** and **Oracle GLAS HW data collection** entries.

    3.  Locate the **Active** column for each entry, select the value and choose **true**.

2.  Grant elevated permissions to the `acc` user, enabling access to your java installation directories, for example:

    -   `/usr/lib/jvm/*/bin/java`
    -   `/usr/lib/jvm/*/*/bin/java`
    -   `/usr/lib/jvm/*/bin/jcmd`
    -   `/usr/lib/jvm/*/*/bin/jcmd`
    -   `/var/cache/servicenow/agent-client-collector/osquery/bin/osqueryi`
    You can add additional java directories during java installation, as needed.

    -   In a Linux environment, grant elevated permissions in the `/etc/sudoers` file to access the java installation directories.
    -   In a Windows environment, grant elevated permissions \(read and execute\) via the system administrator to access the java installation directories.

**Parent Topic:**[Application patterns for the Agent Client Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/agent-client-collector/application-patterns-acc.md)

