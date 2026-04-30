---
title: Configure mobile re-authentication for single or multiple use
description: Define whether each mobile action requires re-authentication. Alternatively, define whether the user can perform multiple actions without the need to re-authenticate each time.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Re-authentication, System properties, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure mobile re-authentication for single or multiple use

Define whether each mobile action requires re-authentication. Alternatively, define whether the user can perform multiple actions without the need to re-authenticate each time.

## Before you begin

Role required: admin

## Procedure

1.  Type `sys_properties.list` in the filter navigator.

2.  Open the record for **glide.sg.reauthentication.single\_use\_token**.

3.  In the form, match the following values:

<table id="table_tgg_45x_xfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

**glide.sg.reauthentication.single\_use\_token**

</td></tr><tr><td>

Type

</td><td>

`true | false`

</td></tr><tr><td>

Value

</td><td>

`true` - Required to re-authenticate before every action. \(Default value\)`false` - Able to perform multiple actions without the need to re-authenticate each time.

</td></tr></tbody>
</table>
**Parent Topic:**[Configure mobile re-authentication system properties](../concept/mobile-reautentication-concept.md)

