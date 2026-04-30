---
title: Virtual Agent URL parameters
description: Virtual Agent provides various system parameters that admins can add to an instance URL to control how page content is rendered.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-05-31"
reading_time_minutes: 2
keywords: [Virtual Agent, URL, parameters]
breadcrumb: [Virtual Agent technical reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent URL parameters

Virtual Agent provides various system parameters that admins can add to an instance URL to control how page content is rendered.

## Virtual Agent URL structure

You can control the page rendered for an instance by adding URL parameters to the instance URL, which is `https://<instancename>.service-now.com`.

## System parameters for Virtual Agent chat widget

The Virtual Agent chat widget is supported for use in portals or embedded in third-party pages. The following system parameters control the conversation content rendered in the Virtual Agent chat widget.

<table id="table_qf4_djq_yqb"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

sysparm\_branding\_key

</td><td>

Applies a chat branding configuration to the web chat client.

 Value: branding key for the configuration

</td><td>

-   Apply the branding configuration to a destination page:`https://<instance_name>.service-now.com/$sn-va-web-client-app.do?sysparm_branding_key=<branding_key>`
-   Apply the branding configuration to an embedded chat widget: `https://<instance_name>.service-now.com/$sn-va-web-client-app._embed.do?sysparm_branding_key=<branding_key>`

</td></tr><tr><td>

sysparm\_default\_topic

</td><td>

Sets the default topic on launch via topic `sys_ID`.

</td><td>

`https://<instance_name>.service-now.com/$sn-va-web-client-app.do?sysparm_default_topic=<topic_sys_id>`

</td></tr><tr><td>

sysparm\_domain\_id

</td><td>

Restricts the chat to the specified sys ID for a domain.

</td><td>

`https://<instance_name>.service-now.com/$sn-va-web-client-app.do?sysparm_domain_id=<domain_sys_id>`

</td></tr><tr><td>

sysparm\_live\_agent\_only

</td><td>

Takes user directly to a live agent, if available.

</td><td>

`https://<instance_name>.service-now.com/$sn-va-web-client-app._embed.do?sysparm_live_agent_only=true`

</td></tr><tr><td>

sysparm\_load\_active\_only

</td><td>

Loads the current active conversation.Values:

-   true: Loads only the active conversation
-   false: Doesn't load active conversations

**Note:** If the sysparm\_skip\_load\_history and sysparm\_load\_active\_only parameters are both set to true, the existing sysparm\_skip\_load\_history parameter takes precedence.

</td><td>

`https://<instance_name>.service-now.com/$sn-va-web-client-app.do?sysparm_load_active_only=true`

</td></tr><tr><td>

sysparm\_search\_text

</td><td>

Sets the search text for the conversation.

</td><td>

`https://<instance_name>.service-now.com/$sn-va-web-client-app.do?sysparm_search_text=<search_text>`For example, &lt;search\_text&gt; is request&amp;laptop.

</td></tr><tr><td>

sysparm\_skip\_load\_history

</td><td>

Skips the previous message history and starts a new conversation.Values:

-   true: Doesn’t load message history
-   false: Loads message history

**Note:** If the sysparm\_skip\_load\_history parameter is set to false and the sysparm\_load\_active\_only is set to true, the sysparm\_load\_active\_only loads the current active conversation.

</td><td>

`https://<instance_name>.service-now.com/$sn-va-web-client-app.do?sysparm_skip_load_history=true`

</td></tr><tr><td>

sysparm\_ preview\_mode

</td><td>

Displays the conversation in test mode.

</td><td>

`https://<instance_name>.service-now.com/$sn-va-web-client-app.do?sysparm_preview_mode=true`

</td></tr><tr><td>

sysparm\_requester\_session\_language

</td><td>

Specifies the requester's language for the conversation session when Dynamic Translation for Virtual Agent is installed and configured.

</td><td>

`https://<instance_name>.service-now.com/$sn-va-web-client-app.do?sysparm_requester_session_language=<two-letter language code>`

</td></tr></tbody>
</table>**Parent Topic:**[Virtual Agent technical reference](../concept/va-advanced-technical-reference.md)

**Related topics**  


[Domain separation and Virtual Agent](../concept/domain-separation-virtual-agent.md)

[Virtual Agent interaction records](../concept/va-interactions.md)

[Virtual Agent scripts](../concept/virtual-agent-scripts.md)

[Input data types in Virtual Agent topics](va-data-types.md)

[NLU system entities](nlu-system-entities.md)

[Latency feedback in Virtual Agent](latency-feedback.md)

