---
title: Customize email address internationalization
description: Customize email address internationalization to turn off processing of inbound and outbound emails, disable support for inbound emails or to add email address format for decoding international email addresses.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Email address internationalization, Configure email client, Email client, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Customize email address internationalization

Customize email address internationalization to turn off processing of inbound and outbound emails, disable support for inbound emails or to add email address format for decoding international email addresses.

## Before you begin

Role required: admin

## Procedure

1.  Turn off processing of inbound and outbound emails from or to RFC 6530 email addresses.

    1.  In the navigation filter, enter `sys_properties.list`.

    2.  Select **New** to create the **glide.email\_address.inbound.rfc6530** property.

    3.  On the form, fill in the details.

<table id="table_cqv_gz5_xbc"><thead><tr><th>

Fields

</th><th>

Input

</th></tr></thead><tbody><tr><td>

Name

</td><td>

**glide.email\_address.inbound.rfc6530**

</td></tr><tr><td>

Description

</td><td>

This property turns off processing of emails from RFC 6530 email addresses.

</td></tr><tr><td>

Type

</td><td>

true\|false

</td></tr><tr><td>

Value

</td><td>

false

</td></tr><tr><td>

Ignore cache

</td><td>

Select the check box.**Note:** When Ignore cache check box is selected, the system flushes the server cache when the parameter is changed.

</td></tr><tr><td>

Read roles

</td><td>

Define the roles that have read access to this property.

</td></tr><tr><td>

Write roles

</td><td>

Defines the roles that have write access to this property.

</td></tr></tbody>
</table>    4.  Select **Submit**.

2.  Disable support for processing inbound emails received from encoded email addresses.

    1.  In the navigation filter, enter `sys_properties.list`.

    2.  Select **New** to create **glide.inbound.rfc6530.support.encoded.from.address** property.

    3.  On the form, fill in the details.

<table id="table_v3y_j1v_xbc"><thead><tr><th>

Fields

</th><th>

Input

</th></tr></thead><tbody><tr><td>

Name

</td><td>

**glide.inbound.rfc6530.support.encoded.from.address**

</td></tr><tr><td>

Description

</td><td>

This property disables support for processing emails received from encoded email addresses.

</td></tr><tr><td>

Type

</td><td>

String

</td></tr><tr><td>

Value

</td><td>

false

</td></tr><tr><td>

Ignore cache

</td><td>

Select the check box.**Note:** When Ignore the cache check box is selected, the system flushes the server cache when the parameter is changed.

</td></tr><tr><td>

Read roles

</td><td>

Define the roles that have read access to this property.

</td></tr><tr><td>

Write roles

</td><td>

Define the roles that have write access to this property.

</td></tr></tbody>
</table>    4.  Select **Submit**.

        The encoded email addresses are received-ignored.

3.  Add email address format for decoding international email addresses if the format isn’t ISO-8859-1, ISO-8859-8, or ISO-8859-15.

    1.  In the navigation filter, enter `sys_properties.list`.

    2.  Open the **glide.inbound.rfc6530.supported.encoding.formats** system property.

    3.  Add the required format to the value field, for multiple formats use comma-separated list.

    4.  Select **Update**.


**Parent Topic:**[Email address internationalization](../concept/email-address-internationalization.md)

