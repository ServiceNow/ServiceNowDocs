---
title: MSI installation parameters
description: The following table describes the MSI parameters used when preparing an agent to be installed on a gold image and used with a Virtual Desktop Infrastructure \(VDI\) machine.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/msi-installation-parameters.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-08-31"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Framework reference, Agent Client Collector, IT Operations Management]
---

# MSI installation parameters

The following table describes the MSI parameters used when preparing an agent to be installed on a gold image and used with a Virtual Desktop Infrastructure \(VDI\) machine.

<table id="table_lpn_byt_kkc"><thead><tr><th>

Parameter

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

NP\_VDI\_GOLD\_IMAGE

</td><td>

boolean

</td><td>

Indicates a gold image host is enabled for the NPVDI agent.Set to **true**.

</td></tr><tr><td>

INSTANCE\_URL

</td><td>

string

</td><td>

ServiceNow instance base URL for REST downloads.

</td></tr><tr><td>

INSTANCE\_REST\_API\_USER

</td><td>

string

</td><td>

Basic-auth username for `fetch_vdi_config` REST API.This is the user created in the [Prepare for agent deployment on a non-persistent virtual desktop infrastructure machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/npvdi-agent-instance-prep.md) procedure.

</td></tr><tr><td>

INSTANCE\_REST\_API\_PASS

</td><td>

string

</td><td>

Basic-auth password; passed to the agent as the `ACC_REG_KEY` environment variable.

</td></tr><tr><td>

REGISTRATION\_KEY

</td><td>

string

</td><td>

VDI light-registration key \(must have `light_registration=true` on the instance\). Passed to `acc` as the `ACC_REG_KEY` environment variable.

</td></tr><tr><td>

PAC\_FILE

</td><td>

string

</td><td>

PAC file for proxy auto-configuration during downloads. Takes precedence over `HTTPS_PROXY`.Optional.

</td></tr><tr><td>

HTTPS\_PROXY

</td><td>

string

</td><td>

Static HTTPS proxy URL for downloads \(ignored if `PAC_FILE` is set\). Applied to REST API calls only.Optional.

</td></tr><tr><td>

GOLD\_IMAGE\_SKIP\_PROXY

</td><td>

boolean

</td><td>

Set to **true** to bypass PAC/proxy during configuration downloads and connect directly.Optional.

</td></tr><tr><td>

CUSTOM\_PLUGIN\_CERT\_FOLDER

</td><td>

string

</td><td>

Directory containing custom plugin-signing certificates; copied into the agent config directory before download.Optional.

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Framework reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/agent-client-collector-reference.md)

