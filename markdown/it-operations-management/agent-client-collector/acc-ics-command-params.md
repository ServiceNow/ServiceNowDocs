---
title: Agent Client Collector MID-less installation command parameters
description: Description of the command line parameters used during MID-less Agent Client Collector installation.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Agent Client Collector, Agent Client Collector for Visibility, ACC for Visibility]
breadcrumb: [Agent Client Collector for Visibility reference, Agent Client Collector for Visibility, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector MID-less installation command parameters

Description of the command line parameters used during MID-less Agent Client Collector installation.

<table id="table_rrx_lzd_ndc"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CONNECT\_WITHOUT\_MID

</td><td>

Specify **true** to enable MID-less Agent Client Collector installation. If you don't specify a value, the regular MID Server websocket installation is invoked.

</td></tr><tr><td>

ACC\_CNC

</td><td>

Specify a public gateway endpoint for Agent Client Collector.

</td></tr><tr><td>

REGISTRATION\_KEY

</td><td>

Active and valid registration key for the agent to communicate with.

</td></tr><tr><td>

INSTANCE\_URL

</td><td>

ServiceNow instance that the agent is registered with.

</td></tr><tr><td>

ACC\_ALLOW\_LIST

</td><td>

Optional string; to disable the allow list, set **ACC\_ALLOW\_LIST=0**. By default, the allow list is enabled.**Note:** Disabling the allow list compromises your system's security and is intended as a temporary measure while you’re updating the allow list. After completing the update, enable the allow list by setting **ACC\_ALLOW\_LIST=1**.

</td></tr><tr><td>

ACC\_VALIDATE\_SIG

</td><td>

Optional string; to disable verification of the installer certification validation, set **ACC\_VALIDATE\_SIG=0** that you can add to disable the verification of the installer certification validation. By default, validation is enabled.**Note:** Disable the certification validation only when using non-standard signature validation tools.

</td></tr></tbody>
</table>**Related topics**  


[Configure the websocket server on the MID Server](../task/acc-configure-web-server.md)

