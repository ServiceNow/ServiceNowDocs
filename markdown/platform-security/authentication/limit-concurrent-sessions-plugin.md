---
title: Activating and configuring limit concurrent sessions plugin
description: You can activate the Limit Concurrent Sessions plugin \(com.glide.limit.concurrent.sessions\) if you have the admin role.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Limit concurrent sessions, Authentication, Access Management]
---

# Activating and configuring limit concurrent sessions plugin

You can activate the Limit Concurrent Sessions plugin \(com.glide.limit.concurrent.sessions\) if you have the admin role.

## Before you begin

Role required: admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Find and click the Limit Concurrent Sessions plugin.

3.  On the System Plugin form, review the plugin details and then click the **Activate/Upgrade** related link.

4.  Click **Activate**.

5.  To enable this feature and set a maximum limit of concurrent sessions, go to the **Plugin Files** tab, find the following properties, and change the setting values.

<table id="choicetable_dhn_fnq_hz"><tbody><tr><td id="d214796e95">

**glide.authenticate.limit.concurrent.interactive.sessions**

</td><td>

You can enable the ability to limit concurrent sessions by setting the value to **True**. By default, this property is set to **False**, which means there is no limit on the number of interactive sessions a user can have active.**Note:** To disable this feature, set this property back to **False**.

</td></tr><tr><td id="d214796e116">

**glide.authenticate.max.concurrent.interactive.sessions**

</td><td>

You can set the maximum number of concurrent active interactive sessions a user can have on the instance across all nodes.

</td></tr></tbody>
</table>6.  You can also amend the following properties, if necessary.

<table id="choicetable_upr_nc5_3z"><tbody><tr><td id="d214796e135">

**glide.authenticate.session.types.to.limit.concurrency**

</td><td>

This property limits session types. By default, only the web browser sessions have a limit. Session types include: -   Web Browser \(1\)
-   Mobile Browser \(2\)
-   ServiceNow Mobile App \(3\)
-   Non-interactive \(10\)
You can configure and set the value to '1' for web browser, '2' for mobile browser, or '1,2' for both.**Note:** Only web and mobile browser sessions can have a limit. There are no limits for sessions that originate from the ServiceNow mobile app or non-interactive sessions.

</td></tr><tr><td id="d214796e167">

**glide.authenticate.limit.concurrent.sessions.across.all.nodes**

</td><td>

This property restricts the limit of concurrent sessions per node instead of restricting them across all nodes of a ServiceNow instance. By default, the value is set to true, which limits user sessions across all nodes. If the property is set to false, only the sessions on that node and not the ones on the other nodes are subject to the limit.

</td></tr></tbody>
</table>7.  Click **Update** to have the settings take effect.


## What to do next

[Setting a concurrent session limit by user or role](set-session-limit-user-role.md).

**Related topics**  


[List of plugins \(Yokohama\)](https://www.servicenow.com/docs/access?context=list-of-plugins&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

