---
title: Enable uninstall validation during agent upgrade
description: Configure requiring a maintenance token to uninstall agents during agent upgrade. A maintenance token provides a layer of administrative control so that unauthorized personnel can't perform the uninstall.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/require-token-uninstall-upgrade.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-09-01"
reading_time_minutes: 1
breadcrumb: [Require a maintenance token for Windows uninstalls, ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Enable uninstall validation during agent upgrade

Configure requiring a maintenance token to uninstall agents during agent upgrade. A maintenance token provides a layer of administrative control so that unauthorized personnel can't perform the uninstall.

## Before you begin

Role required: sn\_agent.token\_admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Locate the **sn\_agent.upgrade\_enable\_uninstall\_validation** property and set its value to **true**.

    If the property does not exist, select **New** to create it.

    **Note:** If uninstall validation is enabled, setting the system property back to **false** disables the feature on the next version upgrade.


## Result

The property is invoked for both selective upgrade and high volume upgrade, and the uninstall feature is enabled on Windows agents.

