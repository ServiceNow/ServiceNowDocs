---
title: Discover Java installation data using Agent Client Collector for Visibility Content File-Based Discovery
description: Discover file information in your system using Agent Client Collector for Visibility Content \(ACC-VC\) File-Based Discovery \(FBD\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/agent-client-collector/acc-file-based-discovery.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-10-27"
reading_time_minutes: 2
keywords: [Java installation using FBD, Java installation using Agent Client Collector for Visibility Content]
breadcrumb: [ACC Discovery, ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Discover Java installation data using Agent Client Collector for Visibility Content File-Based Discovery

Discover file information in your system using Agent Client Collector for Visibility Content \(ACC-VC\) File-Based Discovery \(FBD\).

## Before you begin

-   Install the latest version of Agent Client Collector for Visibility Content.
-   Install FBD.
-   Verify that a MID Server is installed in your environment.
-   Verify that the Oracle Global License Advisory Services \(GLAS\) plugin \(`com.sn_itom_oracleglas`\) is active.
-   If you want to collect GLAS hardware data, enable the Oracle GLAS hardware data collection policy.
-   Role required: discovery\_admin

## About this task

Both FBD and Process-Based Discovery \(PBD\) collect Oracle GLAS Java installation data. FBD uses the `java_glas` stream and the **File Based Discovery Policy - Java GLAS** policy. PBD uses the **Oracle GLAS Java Process Discovery** policy, which runs weekly. For details about the PBD process, see [Discover Java installation data using Agent Client Collector for Visibility Content Process-Based Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-process-based-discovery.md).

## Procedure

1.  Enable FBD.

    1.  Navigate to **All** &gt; **Discovery Definition** &gt; **Configuration Console**.

    2.  On the Discovery Configuration Console form, enable the **File Based Discovery** toggle.

        Enabling FBD also activates the **File Based Discovery Policy - Java GLAS** policy.

        **Important:** After you upgrade to a release that adds the **File Based Discovery Policy - Java GLAS** policy \(starting from Agent Client Collector for Visibility Content version 2.1.1\), verify that the policy is active under **All** &gt; **Agent Client Collector** &gt; **Policies**. If the policy isn't active, deactivate and activate FBD again.

2.  Enable the **File Based Discovery Background Policy** policy.

    1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Policies**.

    2.  Select **File Based Discovery Background Policy**.

    3.  Select **Activate**.

3.  Enable the Java Discovery property.

    This property is set to **true** by default, so you must complete this step only if the value was changed. The property takes effect only when the Oracle GLAS plugin \(`com.sn_itom_oracleglas`\) is active.

    1.  Locate the **sn\_acc\_vis\_content.file\_discovery.enable\_java\_discovery** property on the System Properties page \(**All** &gt; **System Properties** &gt; **All Properties**\).

    2.  Set the property value to **true**.

4.  Grant elevated permissions to the `acc` user, enabling access to your Java installation directories, for example:

    -   `/usr/lib/jvm/*/bin/java`
    -   `/usr/lib/jvm/*/*/bin/java`
    You can add additional Java directories during Java installation, as needed.

    -   In a Linux environment, grant elevated permissions in the `/etc/sudoers` file to enable access to the Java installation directories.
    -   In a Windows environment, grant elevated permissions \(read and execute\) via the system administrator to enable access to the Java installation directories.

## Result

When running Discovery for Java installation, data is discovered through and is stored in the `ora_java_audit` and `ora_java_evidence` tables. For details on the data stored in these tables, see [Data collected during Agent Client Collector for Visibility Content File-Based Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/data-collected-file-based-discovery.md).

Java discovery runs as its own FBD scan stream \(`java_glas`\), separate from the other FBD scans. The steps on this page cover Linux, Windows, and macOS environments.

**Parent Topic:**[Agent Client Collector Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-discovery.md)

**Related topics**  


[Discover Java installation data using Agent Client Collector for Visibility Content Process-Based Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-process-based-discovery.md)

