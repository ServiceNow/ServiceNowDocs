---
title: Agent Client Collector installation
description: You can install the Agent Client Collector on any supported host machine. The Agent Client Collector connects to a MID Server using the HTTP/S protocol, and the connection remains active after being established. One MID Server may handle several agents simultaneously, while a single agent works with one MID Server at a time and switches to a different MID Server when necessary to provide failover protection.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector installation

You can install the Agent Client Collector on any supported host machine. The Agent Client Collector connects to a MID Server using the HTTP/S protocol, and the connection remains active after being established. One MID Server may handle several agents simultaneously, while a single agent works with one MID Server at a time and switches to a different MID Server when necessary to provide failover protection.

When an agent's IP address changes, it selects a MID Server to connect to based on the agent's MID Server list.

The maximum number of agents that can be connected to a single MID Server is configurable in the **sn\_agent.mid.max\_allowed\_agents** MID Server property. The default value is 4,000.

For ACC-VC, a default 1 GiB MID Server can support 700 agents concurrently. An 8 GiB configuration for a MID Server can support 8,000 agents concurrently. You can also scale out. For example, 5 MID Servers with 8 GiB of heap size can handle up to 40k agents.

Agent Client Collector is installed with ruby version 3.3.2.

The default user account is a local user called **servicenow**. This user has basic level permissions.

The following table describes the permissions required to work with various features associated with the agent, per OS. An asterisk \(\*\) indicates that no special permissions are required.

<table id="table_w4y_x2d_kfc"><thead><tr><th>

Feature

</th><th>

Windows

</th><th>

Linux

</th><th>

macOS

</th></tr></thead><tbody><tr><td>

Basic inventory

</td><td>

\*

</td><td>

\*

</td><td>

\*

</td></tr><tr><td>

Serial number\(s\)

</td><td>

\*

</td><td>

sudo

 dmidecode

</td><td>

\*

</td></tr><tr><td>

Running processes

</td><td>

Debug programs

</td><td>

\*

</td><td>

\*

</td></tr><tr><td>

Mapping TCP connections to running processes

</td><td>

\*

</td><td>

sudo ss

</td><td>

\*

</td></tr><tr><td>

Storage devices

</td><td>

LOCAL SYSTEM

</td><td>

\*

</td><td>

\*

</td></tr><tr><td>

Logged-in users

</td><td>

LOCAL SYSTEM

</td><td>

\*

</td><td>

\*

</td></tr><tr><td>

Package self-upgrade

</td><td>

LOCAL SYSTEM

</td><td>

sudo rpm/dpkg

</td><td>

Not supported

</td></tr></tbody>
</table>If you completely reinstall the agent on a single host server, a second agent record registers on the instance. Delete the original agent on the **Agent Client Collectors** page \(**All** &gt; **Agent Client Collector** &gt; **Agents**\).

Agents whose **Status = Down** or **Disconnected** which haven't been deleted are deleted automatically after 30 days. You can modify this setting on the Autoflush form page \(see Autoflush form\).

Use the Manual Transport Layer Security protocol \(mTLS\) for secure authentication between your MID Web Server and the agent \(the client\). For details, see [Connect the agent to the MID Server using mTLS](../task/enable-tls-agent.md).

For details on using Agent Client Collector in an air-gapped environment, see the [Agent Client Collector Framework Air Gapped Configuration Item Management Solution \[KB1585753\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1585753) article in the Now Support Knowledge Base.

Golden image mode enables cloning of additional agents. Setting golden image mode is described in the installation procedure prerequisites for each OS. For information on the structure and modularity of the golden image plugin by operating system, see [Golden image structure and modularity](../reference/golden-image-structure-modularity.md).

Agent Client Collector supports domain separation. The domain of the agent and the CIs it creates is determined by the domain of the MID Server that the agent is connected to. The user's domain must be the lowest domain level \(known as a leaf domain\) to enable creating a Websocket endpoint extension for the MID Server.

**Related topics**  


[Agent Client Collector installation on a Linux OS system](acc-install-linux-concept.md)

[Install the Agent Client Collector on a Windows machine manually](../task/acc-install-windows.md)

[Agent Client Collector installation on a macOS system](acc-install-mac-os.md)

