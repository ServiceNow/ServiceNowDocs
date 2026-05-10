---
title: Create an OpenFrame configuration
description: This configuration specifies the OpenFrame window settings as well as the URL to be launched within OpenFrame.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Phone channel, Enable communication channels, Configure, Customer Service Management]
---

# Create an OpenFrame configuration

This configuration specifies the OpenFrame window settings as well as the URL to be launched within OpenFrame.

## Before you begin

Role required: admin

## About this task

As part of the OpenFrame configuration, users with the admin role can select one or more user groups. Access to the configuration is limited to the users that have the openframe user role and that belong to the selected groups.

## Procedure

1.  Navigate to **All** &gt; **OpenFrame** &gt; **Configurations** to display the OpenFrame Configurations list.

2.  Click **New**.

3.  Fill in the fields, as appropriate.

<table id="table_ctq_1706_ae"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the OpenFrame configuration.

</td></tr><tr><td>

Title

</td><td>

The title that appears in the OpenFrame window header.

</td></tr><tr><td>

Subtitle

</td><td>

The subtitle that appears in the OpenFrame window header.

</td></tr><tr><td>

Order

</td><td>

The order number for the configuration.If users have multiple OpenFrame configurations, they can only access the configuration with the lowest order number.

**Note:** When upgrading, the **Order** field for the existing default OpenFrame configuration is set to 1.

</td></tr><tr><td>

Enable collapsed view

</td><td>

Enables the expand and collapse capability for the OpenFrame window. When collapsed, users can still access call control actions. The default setting is **False**.

</td></tr><tr><td>

Show presence indicator

</td><td>

Enables the indicator that displays agent availability.

</td></tr><tr><td>

User Group

</td><td>

The user groups selected for this configuration. Access to this configuration is limited to the users that have the openframe user role and that belong to the selected groups.**Note:** If you do not select any groups, the configuration is available to all users with the openframe user role.

</td></tr><tr><td>

URL

</td><td>

The URL to be launched within OpenFrame. This URL can be an absolute path or a path that is relative to the ServiceNow instance.

</td></tr><tr><td>

Active

</td><td>

Denotes this configuration as active.

</td></tr><tr><td>

Width

</td><td>

The width of the OpenFrame window.

</td></tr><tr><td>

Height

</td><td>

The height of the OpenFrame window, not including the OpenFrame header height.

</td></tr><tr><td>

Icon Class

</td><td>

The class of icons used for the OpenFrame window \(retina-icons.css\). Only supports icon-phone and icon-video values.

</td></tr><tr><td>

Title Icon

</td><td>

The icon displayed on the OpenFrame window header.

</td></tr><tr><td>

Configuration

</td><td>

Can be used to store any JSON encoded string.

</td></tr></tbody>
</table>    **Note:** Several fields on the OpenFrame Configuration form can also be set by using the OpenFrame API. These fields include: **Title**, **Subtitle**, **Width**, **Height**, and **Title Icon**.

4.  Click **Submit**.


**Related topics**  


[openFrameAPI - Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/c_openFrameAPI.md)

