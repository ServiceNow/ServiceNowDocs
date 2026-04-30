---
title: Configure the status for rooted and jailbroken devices
description: Define whether jailbroken \(iOS\) and rooted \(Android\) devices are permitted on your mobile device. The default value is set to false to increase security and to minimize possible disruption to your system.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [System properties, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure the status for rooted and jailbroken devices

Define whether jailbroken \(iOS\) and rooted \(Android\) devices are permitted on your mobile device. The default value is set to `false` to increase security and to minimize possible disruption to your system.

## Before you begin

Role required: admin

## About this task

Configure settings to decide whether to allow jailbroken and rooted devices.

**Note:** If you select `true`, jailbroken and rooted devices can launch the ServiceNow application, however your device may be compromised and you are at risk of losing your ServiceNow data.

## Procedure

1.  Type `sys_properties.list` in the filter navigator.

2.  Open the record for **glide.sg.allow\_rooted\_jailbroken\_devices system**.

3.  In the form, match the following values:

<table id="table_tgg_45x_xfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

**glide.sg.allow\_rooted\_jailbroken\_devices system**

</td></tr><tr><td>

Type

</td><td>

`true | false`

</td></tr><tr><td>

Value

</td><td>

`true` - Rooted and jailbroken devices can be used when using ServiceNow® mobile apps.

 `false` - Rooted and jailbroken devices are not permitted when using ServiceNow® mobile apps. \(Default value\)

</td></tr></tbody>
</table>
**Parent Topic:**[Mobile system property configurations](../concept/additional-mobile-configuration.md)

