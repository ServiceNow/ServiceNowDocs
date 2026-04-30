---
title: Agent Client Collector Framework configuration properties
description: Description of the properties that determine the behavior of Agent Client Collector Framework configuration.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Agent Client Collector Framework reference, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector Framework configuration properties

Description of the properties that determine the behavior of Agent Client Collector Framework configuration.

<table id="table_w1r_qgs_xyb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_agent.agent\_static\_import\_char\_read\_limit**

</td><td>

The character read limit for a given payload item. Relates only to the configuration item being processed and not the total attachment size.Default: 1000000

</td></tr><tr><td>

**sn\_agent.agent\_upgrade\_wait\_time**

</td><td>

Maximum number of minutes for an agent to successfully upgrade before entering **Warning** status.Default: 30

</td></tr><tr><td>

**sn\_agent.agent\_version**

</td><td>

The current ACC-F release version installed on the instance.Type: String

</td></tr><tr><td>

**sn\_agent.appl\_classification\_behavior**

</td><td>

The characteristics and behaviors for applications during Agent Discovery. When set to **simple**, creates a shell CI. Default: simple

</td></tr><tr><td>

**sn\_agent.auto\_upgrade.enabled**

</td><td>

When set to true, the instance automatically upgrades existing Agent Client Collector installations to the version set in the sn\_agent.agent\_version property, if the agent version is lower than the property's version.Type: Boolean

Default: false

</td></tr><tr><td>

**sn\_agent.auto\_upgrade.max\_upgrades\_per\_handler\_per\_hour**

</td><td>

The maximum number of Agent Client Collector upgrades possible per MID Server every hour.Type: Integer

Default: 50

**Note:** Modifying this value may negatively affect system performance.

</td></tr><tr><td>

**sn\_agent.auto\_upgrade.max\_upgrades\_per\_hour**

</td><td>

The maximum number of Agent Client Collector upgrades possible for all agents on all MID Servers.Type: Integer

Default: 1000

**Note:** Modifying this value may negatively affect system performance.

</td></tr><tr><td>

**sn\_agent.config\_publish.max\_payload\_size**

</td><td>

The size, in bytes, that the config\_publish\_payload can reach on the MonitoringProbe ECC queue topic before an error is logged and the payload is skipped.Default: 15000000

</td></tr><tr><td>

**sn\_agent.ecc\_queue.max\_payload\_size**

</td><td>

The maximum allowable payload size for an ECC queue record to be processed by the agent.Default: 5000000

</td></tr><tr><td>

**sn\_agent.enable\_auto\_mid\_selection**

</td><td>

When set to **true**, the instance sends a list of MID Servers to the agents. To enable automatic selection of a MID Server from the list, set the **auto-mid-selection** property to true in the agents’ acc.yml file. Automatic selection of MID Servers ensures that each agent uses the most efficient available MID Server.Default: false

**Note:** This property determines only whether a list of MID Servers is sent to the agent.

-   If this property was previously set to **true** and is then set to **false**, automatic MID selection is performed on the previously sent MID Server list if the **auto-mid-selection** property is set to **true** in the acc.yml file.
-   If this property is set to **true** and the **auto-mid-selection** property in the acc.yml file is set to **false**, no automatic MID Server selection is performed.

</td></tr><tr><td>

**sn\_agent.installer\_max\_endpoints**

</td><td>

Maximum number of MID Web Server endpoint URLs to be selected during agent single line installation.Default: 3

</td></tr><tr><td>

**sn\_agent.keep\_alive.alive\_duration**

</td><td>

The amount of time, in seconds, within which the agent's last\_refreshed timestamp must be updated. After this time period, the agent status moves from **Up** to **Warning**. If the indicated time period passes again, the status moves from **Warning** to **Down**.Default: 120

</td></tr><tr><td>

**sn\_agent.keep\_alive.disconnected\_duration**

</td><td>

The amount of time, in seconds, within which the last\_keepalive timestamp must be updated. After this time period, the agent status changes from **Up** to **Disconnected**. Default: 600

</td></tr><tr><td>

**sn\_agent.logging.verbosity**

</td><td>

The minimum level of messages that are logged for Agent Client Collector Framework. Messages with the indicated status and anything more severe are logged.Options:

-   error
-   warn
-   info
-   debug

Default: info

</td></tr><tr><td>

**sn\_agent.max\_sys\_ids\_in\_query**

</td><td>

The maximum number of sys IDs to return during GlideRecord queries.Default: 400000

</td></tr><tr><td>

**sn\_agent.maximum\_mids\_to\_select**

</td><td>

The maximum number of MID Servers that can be selected for agent setup.Default: 20

</td></tr><tr><td>

**sn\_agent.min\_upgrade\_history\_per\_agent**

</td><td>

The minimum number of upgrades saved per agent.Default: 2

</td></tr><tr><td>

**sn\_agent.registration\_key\_validity.days**

</td><td>

The number of days after creation of a registration key that the key is valid before it is deleted.Default: 90

</td></tr><tr><td>

**sn\_agent.registration\_key\_notification.days**

</td><td>

The number of days before registration key deletion that an email notification is sent to the key's ownership group, informing of pending deletion.Default: 14

</td></tr><tr><td>

**sn\_agent.sync\_filters\_interval\_min**

</td><td>

The number of minutes after which CMDB changes are detected and then synched to the MID Server.Default: 10

</td></tr><tr><td>

**sn\_agent.time\_ago\_in\_seconds\_to\_query\_ecc\_queue**

</td><td>

When processing ecc\_queues, only query those created within the indicated time \(in seconds\).Default: 43200 \(12 hours\)

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Framework reference](agent-client-collector-reference.md)

