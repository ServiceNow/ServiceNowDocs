---
title: Digital End-User Experience properties and settings
description: You can update the following Digital End-User Experience properties and settings to fit your needs. You must have the admin role to update these settings and properties.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Digital End-User Experience, IT Service Management]
---

# Digital End-User Experience properties and settings

You can update the following Digital End-User Experience properties and settings to fit your needs. You must have the admin role to update these settings and properties.

<table id="table_uh2_f5s_rdc"><thead><tr><th>

Property or setting

</th><th>

Value

</th><th>

Type

</th><th>

Application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_dex.administration\_tab\_doc\_link

</td><td>

\[url\]

</td><td>

string

</td><td>

Application and Device Health

</td><td>

Link to the DEX Administration card documentation

</td></tr><tr><td>

sn\_dex.alert.correlation\_rule.device.period

</td><td>

300

</td><td>

integer

</td><td>

Application and Device Health

</td><td>

The period in seconds for correlating similar DEX device alerts based on the message\_keyUse zero to disable the rule.

</td></tr><tr><td>

sn\_dex.alert.delete\_delay\_period

</td><td>

15

</td><td>

integer

</td><td>

Application and Device Health

</td><td>

The delay period in minutes after which a closed alert is deletedFor example, if an alert associated with dex\_alert\_metadata is closed it isn’t deleted for this period. The default is 15 min.

</td></tr><tr><td>

sn\_dex.dex\_user\_ref\_mapping

</td><td>

\[JSON\]

</td><td>

string

</td><td>

Application and Device Health

</td><td>

Used to map the sys\_user.user\_id column to a custom\_user\_id column when customizedSuffix and prefix help in providing transformation between the values.

For example, \{"prefix": "dex-`blah`", "device\_user\_id\_column": “custom\_user\_id", "suffix": "dex-`blah`”\}

</td></tr><tr><td>

sn\_dex.enable\_dex\_action\_playbook

</td><td>

true

</td><td>

true \| false

</td><td>

Application and Device Health

</td><td>

Enables the playbook use when the correct plugins are enabledUse for hiding or showing the playbook in the options on the device details page.

</td></tr><tr><td>

sn\_dex.extension.push\_metrics\_interval

</td><td>

300

</td><td>

integer

</td><td>

Application and Device Health

</td><td>

The interval in seconds that the browser extension uses to push metrics to the agentThe default is 5 min.

</td></tr><tr><td>

sn\_dex.extension.session\_timeout

</td><td>

240

</td><td>

integer

</td><td>

Application and Device Health

</td><td>

The period in minutes that an open session is timed out using the tab.lastAccessed time The default is 4 hours. Entering 0 turns off this feature.

</td></tr><tr><td>

sn\_dex.network\_performance\_metrics\_duration

</td><td>

7200

</td><td>

integer

</td><td>

Application and Device Health

</td><td>

Duration of network performance metrics in seconds

</td></tr><tr><td>

sn\_dex.set\_location

</td><td>

true

</td><td>

true \| false

</td><td>

Application and Device Health

</td><td>

If set to true, table cmn\_location is updated by DEX when valid location isn’t found and a new location record is created

</td></tr><tr><td>

sn\_dex\_content.enable.content.log

</td><td>

false

</td><td>

true \| false

</td><td>

DEX Content Playbook

</td><td>

Enables or disables storing of the check execution details in the table dex\_content\_log

</td></tr><tr><td>

sn\_dex\_desktop.app\_snapshot\_version

</td><td>

2.0.0

</td><td>

string

</td><td>

Desktop Assistant

</td><td>

Desktop Assistant electron snapshot app version numberYou can use this property during app development.

</td></tr><tr><td>

sn\_dex\_desktop.app\_version

</td><td>

2.5.0

</td><td>

string

</td><td>

Desktop Assistant

</td><td>

Desktop Assistant electron app version number

</td></tr><tr><td>

sn\_dex\_desktop.enable\_notification

</td><td>

false

</td><td>

string

</td><td>

Desktop Assistant

</td><td>

Determines if the notifications should be sent

</td></tr><tr><td>

sn\_dex\_desktop.mac\_min\_version

</td><td>

2.6.0

</td><td>

string

</td><td>

Desktop Assistant

</td><td>

Minimum compatible version for desktop application on macOS

</td></tr><tr><td>

sn\_dex\_desktop.sn\_desktop\_assistant.notification\_time\_to\_live

</td><td>

7

</td><td>

string

</td><td>

Desktop Assistant

</td><td>

Time to live value of notifications to be sent to the Desktop AssistantThis value is the number of days for which the notification is active and any notification older than this value is discarded.

**Note:** The Time-to-Live \(TTL\) value can be set to a maximum of seven days.

</td></tr><tr><td>

sn\_dex\_desktop.va\_portal\_param

</td><td>

esc

</td><td>

string

</td><td>

Desktop Assistant

</td><td>

Property that specifies the default esc portalIf you use a portal other than esc for ITSM Virtual Agent, you can specify that portal for integration between Desktop Assistant and ITSM Virtual Agent.

</td></tr><tr><td>

sn\_dex\_desktop.win\_min\_version

</td><td>

2.6.0

</td><td>

string

</td><td>

Desktop Assistant

</td><td>

Minimum compatible version for desktop application on Windows

</td></tr></tbody>
</table>**Parent Topic:**[Digital End-User Experience reference](../concept/dex-reference.md)

