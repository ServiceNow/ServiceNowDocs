---
title: Interaction wrap up scheduled job
description: The interaction wrap up feature includes a scheduled job to close any interactions in the Wrap Up state that were not closed either manually by an agent or automatically by the system.
locale: en-US
release: xanadu
product: Interaction Management
classification: interaction-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Interaction wrap up, Configuring Interaction Management, Interaction Management, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Interaction wrap up scheduled job

The interaction wrap up feature includes a scheduled job to close any interactions in the Wrap Up state that were not closed either manually by an agent or automatically by the system.

Ending the wrap up period is typically performed in the following ways:

-   Manually by the agent.
-   Automatically by the system, if the **Enforce wrap up duration** setting is enabled in the [interaction wrap up configuration](../task/create-interaction-wrap-up-config.md).
-   By closing the workspace tab.

While most interaction records are automatically closed when the configured wrap up period ends, the interaction wrap up feature also includes a scheduled job to close any remaining records. For example, if the **Enforce wrap up duration** setting is not enabled in the configuration and agents close interactions by closing the browser, these interactions can remain in the Wrap Up state.

The **Fallback Timeout for Interactions in Wrap Up** scheduled job functions as a fail-safe method for closing interaction records that remain in the Wrap Up state. This scheduled job:

-   Evaluates interaction records in the Wrap Up state.
-   Closes those records that have been in the Wrap Up state longer than the time specified in the Max Wrap Up system property.

The Max Wrap Up system property \(**com.glide.interaction.max\_wrapup\_duration**\) defines the length of time that an interaction record can be in the Wrap Up state. The default value for this property is 15 minutes.

The time value set in the Max Wrap Up system property must be greater than the time value set in the **Enforce wrap up duration** field on the Interaction Wrap Up Configuration form.

The default run interval for this scheduled job is five minutes. The system administrator can configure this time interval.

**Note:** This scheduled job is inactive by default.

**Parent Topic:**[Interaction wrap up](interaction-wrap-up-state.md)

