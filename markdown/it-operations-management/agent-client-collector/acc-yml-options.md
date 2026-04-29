---
title: Configuration file options
description: Options available in the acc.yml configuration file.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [ACC-F reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# Configuration file options

Options available in the `acc.yml` configuration file.

<table id="table_w45_t4x_dxb"><thead><tr><th>

Option

</th><th>

Type

</th><th>

Default

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

name

</td><td>

String

</td><td>

Agent\_&lt;value of the **hostname** command&gt;

</td><td>

Agent name registered on the SN instance can be specified by the user. The result of the 'hostname' command is used as the default.

</td><td>

`name: <name of agent>`

</td></tr><tr><td>

backend-url

</td><td>

List

</td><td>

`wss://127.0.0.1:8800/ws/events`

</td><td>

List of MID Webserver endpoint URLs to communicate with. If communication cannot be configured with the first URL, the system moves to the ensuing URLs until it establishes a connection. Works when `enable-auto-mid-selection=true`

</td><td>

`backend-url: <mid server ip>:<websocket port>`

</td></tr><tr><td>

api-key

</td><td>

String

</td><td>

&lt;None&gt;

</td><td>

API key used by the MID Server to authenticate incoming agent connections. Value is encrypted on initial agent startup.

</td><td>

`api-key: <mid web server api key>`

</td></tr><tr><td>

user

</td><td>

String

</td><td>

admin

</td><td>

Username used for basic authentication.If this parameter is empty, the agent does not start.

</td><td>

`user: "agent-01"`

</td></tr><tr><td>

password

</td><td>

String

</td><td>

admin

</td><td>

Password used for basic authentication. Value is encrypted on initial agent startup.If this parameter is empty, the agent does not start.

</td><td>

`password: <secure-password>`

</td></tr><tr><td>

log-level

</td><td>

String

</td><td>

Info

</td><td>

Amount of logging to appear in the acc.log file. Values:-   Panic
-   Fatal
-   Error
-   Warn
-   Info
-   Debug

</td><td>

`log-level: debug`

</td></tr><tr><td>

allow-list

</td><td>

String

</td><td>

/etc/servicenow/agent-client-collector/check-allow-list.json

</td><td>

Path to the JSON file that contains the list of check commands the agent can execute. Comment out this parameter to disable the allow-list.If this parameter is empty, the allow-list is disabled.

</td><td>

`allow-list: /etc/agent/check-allow-list.json`

</td></tr><tr><td>

appl\_classification\_behavior

</td><td>

List

</td><td>

simple

</td><td>

Indicates whether to enable shell CI creation on the agent.Possible values are:

-   simple: Indicates that shell CI creation is enabled.
-   off: Indicates that no shell CIs are created for the application.
-   full: Indicates that complete Discovery of the application CIs is performed using patterns.

</td><td>

`appl_classification_behavior: off`

</td></tr></tbody>
</table><table id="table_hcj_gtx_dxb"><thead><tr><th>

Option

</th><th>

Type

</th><th>

Default

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

verify-plugin-signature

</td><td>

Boolean

</td><td>

True

</td><td>

Verifies the plugin signature prior to execution. Disable when using self-signed or developmental plugins.

</td><td>

`verify-plugin-signature: true`

</td></tr><tr><td>

insecure-skip-tls-verify

</td><td>

Boolean

</td><td>

True

</td><td>

Determines whether the verify the certificate when connecting to the MID Server.

</td><td>

`insecure-skip-tls-verify: true`

</td></tr><tr><td>

enable-auto-mid-selection

</td><td>

Boolean

</td><td>

True

</td><td>

Controls the Auto MID Selection feature to connect to the optimal MID Web Server provided by the instance.

</td><td>

`enable-auto-mid-selection: true`

</td></tr><tr><td>

check-command-prefer-installed

</td><td>

Boolean

</td><td>

False

</td><td>

Indicates the preference of executables provided within ACC plugins or executables available in the host system’s PATH variable.-   false = ACC plugins
-   true = Executables in the host system's PATH variable

</td><td>

`check-command-prefer-installed: false`

</td></tr><tr><td>

powershell\_installed

</td><td>

Boolean

</td><td>

False

</td><td>

Disables powershell command execution on agents.

</td><td>

`powershell-installed: true`

</td></tr><tr><td>

allow-list-global-only

</td><td>

Boolean

</td><td>

False

</td><td>

Set to **true** to enhance security by relying only on the allow list defined in the **allow-list** parameter you specify during configuration, ignoring allow lists bundled with ACC plugins.

</td><td>

`allow-list-global-only: false`

</td></tr><tr><td>

disable-assets

</td><td>

Boolean

</td><td>

false

</td><td>

Indicates whether a check running with an asset \(plugin\) dependency fetches ACC plugins from the ServiceNow® instance, or uses a copy of the plugins in its cache folder.When set to **false**, additional assets can be downloaded during check execution.

Set to **true** to enhance security and ensure that no new plugins are downloaded during check execution.

</td><td>

`disable-assets: false`

</td></tr><tr><td>

agent-upgrade-url-path

</td><td>

String

</td><td>

`https://install.service-now.com/glide/distribution/builds/package/app-signed/`

</td><td>

Indicates an alternate web server URL endpoint for downloading ACC installer packages when performing selective upgrade.

</td><td>

`agent-upgrade-url-path: https://<ip address>:<port>/acc_installers`

</td></tr><tr><td>

certificate-rotation-days-out

</td><td>

Integer

</td><td>

28

</td><td>

Indicates the number of days before certificate expiration that an agent attempts to rotate its certificate.

</td><td>

`certificate-rotation-days-out=28`

</td></tr><tr><td>

enable-patterns-on-agent

</td><td>

Boolean

</td><td>

false

</td><td>

Enables gathering details on the applications which run on the Agent Client Collector.This parameter is required only when using the Agent Client Collector for pattern execution.

</td><td>

`enable-patterns-on-agent: true`

</td></tr><tr><td>

keepalive-filter-nics

</td><td>

Boolean

</td><td>

true

</td><td>

Indicates whether Network Interface Controllers \(NICs\) are filtered on the agent \(**true**\) or the MID Server \(**false**\) during keepalive action.

</td><td>

`keepalive-filter-nics: true`

</td></tr><tr><td>

keepalive-number\_nics\_per\_ip\_type

</td><td>

Integer

</td><td>

1

</td><td>

Indicates the maximum number of Network Interface Controllers \(NICs\) per IP type \(IP4, IP6\) sent with a keepalive action. The indicated number is sent for each IP type.For example, if the value is 1, a maximum of 2 NICs are sent \(0-1 each for IP4 and IP6\). If the value is 4, a maximum of 8 NICs are sent \(0-4 each for IP4 and IP6\).

</td><td>

`keepalive-number_nics_per_ip_type: 4`

</td></tr></tbody>
</table><table id="table_mw3_cy3_vfc"><thead><tr><th>

Option

</th><th>

Type

</th><th>

Default

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

pac-file

</td><td>

String\(Required\)

</td><td>

"" \(empty\)

</td><td>

Specifies the location of the PAC file to use for proxy configuration. Can be either:-   A local file path \(such as: `file:///etc/proxy/proxy.pac`\)
-   A remote URL \(such as: `https://proxy.company.com/proxy.pac`\)

</td><td>

`pac-file: "https://proxy.company.com/proxy.pac"`

</td></tr><tr><td>

pac-cache-ttl

</td><td>

Duration\(Optional\)

</td><td>

30m \(30 minutes\)

</td><td>

Determines how long proxy rules from the PAC file are cached in memory.Setting this to 0 disables caching.

</td><td>

`pac-cache-ttl: "1h" # Cache for 1 hour`

</td></tr><tr><td>

pac-refresh-interval

</td><td>

Duration\(Optional\)

</td><td>

30m \(30 minutes\)

</td><td>

Specifies how often the agent is to check for updates to the PAC file.Useful when the PAC file is hosted remotely and may be updated periodically.

</td><td>

`pac-refresh-interval: "15m" # Check for updates every 15 minutes`

</td></tr><tr><td>

pac-dial-timeout

</td><td>

Duration\(Optional\)

</td><td>

30s \(30 seconds\)

</td><td>

Indicates the amount of time to wait when establishing a connection through a proxy server before timing out.

</td><td>

`pac-dial-timeout: "10s" # 10 second timeout`

</td></tr><tr><td>

pac-reset-on-connect-failure

</td><td>

Boolean\(Optional\)

</td><td>

true

</td><td>

When set to true, the agent clears the PAC cache and attempts to refresh the PAC file if a proxy connection proxy fails. This helps recover from proxy configuration changes or temporary proxy issues.

</td><td>

`pac-reset-on-connect-failure: true`

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Framework reference](agent-client-collector-reference.md)

