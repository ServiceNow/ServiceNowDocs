---
title: AI Gateway roles and system properties
description: Roles control who can manage AI Gateway, and system properties control AI Gateway behavior on your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-gw-roles-properties.html
release: australia
topic_type: reference
last_updated: "2026-10-22"
reading_time_minutes: 1
keywords: [AI Gateway roles, AI Gateway system properties]
breadcrumb: [Reference, AI Gateway, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# AI Gateway roles and system properties

Roles control who can manage AI Gateway, and system properties control AI Gateway behavior on your instance.

## Roles

|Role|What it allows|
|----|--------------|
|sn\_ai\_governance.ai\_steward|Use the AI Gateway settings page and the **AI Gateway** tab of MCP server records: register clients, manage tools, apply the Data Sensitivity Check, turn access management on or off, and create, edit, and delete client access policies.|
|admin|Use the AI Gateway settings page.|
|aig\_admin|Turn on client access control for the instance with the **sn\_awh\_config.gateway\_access\_control\_enabled** property.|
|sn\_aia.admin|Add MCP servers in AI Agent Studio and configure agents to connect through AI Gateway.|

## System properties

<table id="table_ai-gw-roles-properties-2"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_awh\_config.awh\_enabled

</td><td>

Controls whether governance policies are included in the policy configuration that AI Gateway enforces.

 Type: true \| false

 Default value: true

</td></tr><tr><td>

sn\_awh\_config.pii\_enabled

</td><td>

Turns the Data Sensitivity Check on or off for all servers. The global toggle on the **Policies** tab of the AI Gateway settings page sets this property.

 Type: true \| false

 Default value: true

</td></tr><tr><td>

sn\_awh\_config.auto\_enable\_new\_tools

</td><td>

Controls whether tools that AI Gateway fetches after an MCP server is approved are activated automatically. The **Automatically activate new tools** setting on the **Tools** tab of the AI Gateway settings page sets this property.

 Type: true \| false

 Default value: true

</td></tr><tr><td>

sn\_awh\_config.auto\_update\_tools\_on\_scan

</td><td>

Controls whether tools that the security scan finds vulnerable are deactivated automatically. The **Automatically deactivate vulnerable tools** setting on the **Tools** tab of the AI Gateway settings page sets this property.

 Type: true \| false

 Default value: true

</td></tr><tr><td>

sn\_awh\_config.gateway\_access\_control\_enabled

</td><td>

Turns client access control on or off for the instance. When it's on, AI stewards can turn on access management for each MCP server and create client access policies. When it's set to false, access management is turned off for every MCP server.

 Type: true \| false

 Default value: false

</td></tr></tbody>
</table>For the properties that control tool scanning, see [System properties for AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-reference-system-properties.md).

