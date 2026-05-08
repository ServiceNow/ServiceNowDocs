---
title: Perform high-volume Agent Client Collector upgrade
description: Perform high-volume upgrade of your Agent Client Collector agents when you want to upgrade all of your agents at one time.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [ACC installation, ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Perform high-volume Agent Client Collector upgrade

Perform high-volume upgrade of your Agent Client Collector agents when you want to upgrade all of your agents at one time.

## Before you begin

Configure the Agent Client Collector web server. For details, see [Configure the websocket server on the MID Server](acc-configure-web-server.md).

Ensure that the MID Server, MID Web Server, and the MID Server websocket server are running.

Select the version to which you want to upgrade your agent.

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.
2.  Select **New**.
3.  Assign the following values:
    -   Name = **sn\_agent.agent\_upgrade\_version**
    -   Type = **string**
    -   Value = The version number to be upgraded to, in the format &lt;major\_version.minor\_version.patch\_version&gt;. For example: **4.3.2**
4.  Select **Submit**.

If you do not select a version, the agent automatically upgrades to the current Agent Client Collector Framework scoped app version.

Roles required: agent\_client\_collector\_admin

-   In a Windows environment: Local SYSTEM account
-   In a Linux environment: sudo rpm/dpkg
-   In a macOS environment: sudo pkg

## About this task

High-volume upgrade is supported only in a Windows or Linux environment.

High-volume upgrade does not support Agent Client Collector to MID Server communication via mTLS.

When performing high-volume upgrade, all agents that aren't using the most up-to-date version are upgraded. No upgrade is performed on agents already using the upgraded version.

No upgrade is performed on agents that are outside the application scope. For more information, see Application scope.

An agent is excluded from high-volume upgrade when you reach the failed upgrade limit for an agent. The failed upgrade limit is specified in the **sn\_agent.auto\_upgrade.retry\_limit** system property. The default value for this property is 3.

-   This property applies to both high-volume and selective upgrades that have failed.
-   When an agent reaches the failed upgrade limit, an Agent Client Collector administrator can still run selective upgrade on the agent.
-   You can manually reset the failed upgrade limit by selecting the **Reset failed upgrade attempts** option on the agent page \(select **All** &gt; **Agent Client Collector** &gt; **Agents** and select an agent\).
-   After a successful upgrade, the upgraded agent is considered to have zero failed upgrades \(for future upgrades\).

## Procedure

1.  Verify that the version number you want to upgrade to is available.

    1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

    2.  Locate the **sn\_agent.agent\_version** property.

        Verify that the version number displayed is a valid agent version, representing the version that the agent will be upgraded to. If the version number is not valid, the version updates to the **sn\_agent.agent\_version** number.

2.  Enable the property on the System Properties table \(**All** &gt; **System Properties** &gt; **All Properties**\) to activate the upgrade.

    1.  Locate the **sn\_agent.auto\_upgrade.enabled** property.

    2.  Set the property value to **true**.

        Upgrading starts within one minute of enabling the property.


## Result

-   For agents connected to a MID Server: The scheduled job upgrades 50 agents on each MID Server per hour. The maximum number of agents that can be upgraded at a time for all MID Servers is 1,000.
-   For MID-less agents: The scheduled job upgrades up to 1,000 agents per hour by default.
-   For both MID Server and MID-less agents: To modify the number of agents being upgraded at a time, update the value of the **sn\_agent.auto\_upgrade.max\_upgrades\_per\_handler\_per\_hour** property \(**All** &gt; **System Properties** &gt; **All Properties**\). The default value is 1,000.

    **Note:** Modifying this value can negatively impact system performance.


To modify the frequency of the upgrade, update the value of the Repeat Interval in the **Upgrade Agents Incrementally** scheduled job \(**All** &gt; **System Definition** &gt; **Scheduled Jobs**\).

