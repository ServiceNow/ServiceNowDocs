---
title: Agent onboarding configuration settings
description: The settings you can customize when generating an Agent Onboarding installation plan. Toggle settings to activate and enable customization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/acc-onboarding-config-settings.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-05-27"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Framework reference, Agent Client Collector, IT Operations Management]
---

# Agent onboarding configuration settings

The settings you can customize when generating an Agent Onboarding installation plan. Toggle settings to activate and enable customization.

<table id="table-acc-onboarding-config-fields"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Options

</th></tr></thead><tbody><tr><td>

**Connection type**

</td><td>

Method the agent uses to connect to the instance.

</td><td>

-   **Use ICS \(MID-less\)**
-   **Use MID Server**

</td></tr><tr><td>

**MID Server**

</td><td>

MID Servers the agent sends data to. Up to three MID Servers can be selected.Appears only when the Connection type is set as **Use MID Server**.

</td><td>

Drop-down list of available MID Server instances.

</td></tr><tr><td>

**Registration key**

</td><td>

Authorization key for registering with the ServiceNow instance for ICS \(MID-less\) connection.Appears only when the Connection type is set as **Use ICS \(MID-less\)**.

</td><td>

Drop-down list of available registration keys.

</td></tr><tr><td>

**API key**

</td><td>

Authentication key for connecting to the MID Server. Enabled by default and can't be turned off.

</td><td>

Drop-down list of available API keys. Select **Add new** to create a new key.

</td></tr><tr><td>

**Log level/debug mode**

</td><td>

Controls the level of details that the agent logs. Keep at **Info** unless you're troubleshooting.

</td><td>

-   **Error**
-   **Warn**
-   **Info** \(default\)
-   **Debug**
-   **Trace**

</td></tr><tr><td>

**CPU thresholds**

</td><td>

Caps agent CPU usage to protect endpoint performance.Default: 20% for Digital End-User Experience \(DEX\), 5% for all others.

</td><td>

Enter an integer

</td></tr><tr><td>

**Enable PAC file configuration**

</td><td>

URL to be used when connecting the agent through a proxy server.

</td><td>

Enter the Proxy Auto-Configuration \(PAC\) file URL.

</td></tr><tr><td>

**API port**

</td><td>

REST API port on the agent.

</td><td>

Enter the port numberDefault port number: 3031

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Framework reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/agent-client-collector-reference.md)

