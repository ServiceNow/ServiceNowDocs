---
title: Require authentication by default for client-callable script includes \[Updated in Security Center 1.3\]
description: By default, client-callable script includes that do not explicitly set visibility, are public. If needed, add the glide.script.ccsi.ispublic property to enable privacy control over all client-callable script includes accessed by public pages.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Require authentication by default for client-callable script includes \[Updated in Security Center 1.3\]

By default, client-callable script includes that do not explicitly set visibility, are public. If needed, add the **glide.script.ccsi.ispublic** property to enable privacy control over all client-callable script includes accessed by public pages.

When you add this property, you must set its value to **false**, which designates that all client-callable script includes are private, and changes their visibility in public pages.

**Note:** You cannot add the property with a value of **true**, or change its value from **false** to **true**. If you attempt to do so, an error message appears.

If needed, you can change the privacy setting for an individual client-callable script include by adding the `isPublic()` function.

-   The `isPublic()` setting takes precedence over the **glide.script.ccsi.ispublic** property.
-   For example, if you set `isPublic()` to **true** in an individual script, it makes it public, which overrides the **glide.script.ccsi.ispublic** property that makes all other client-callable script includes private.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.script.ccsi.ispublic**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Purpose

</td><td>

Making client-callable script includes private means that guests who access public pages can't access the client-callable script include. A non-logged-in user can't execute a private script.

</td></tr><tr><td>

Recommended value

</td><td>

false

</td></tr><tr><td>

Default value

</td><td>

false

</td></tr><tr><td>

Security risk rating

</td><td>

7.5

</td></tr><tr><td>

Functional impact

</td><td>

If the client-callable script includes are designated as public \(that is, this property is missing\), then unauthenticated users can execute client scripts. Add the property restricts the execution of scripts by a non-logged-in user.

</td></tr><tr><td>

Security risk

</td><td>

\(High\) If you do not add this property, client-side script includes circumvent ACLs, which may result in unintended public functionality. If the client script provides confidential information, it could have an adverse potential security risk.

</td></tr><tr><td>

Workaround

</td><td>

Setting the **glide.script.ccsi.ispublic** property to **false** makes all client-callable script includes private.

 You can change the privacy setting for an individual client-callable script include by adding the `isPublic()` function. The `isPublic` function takes precedence over the **glide.script.ccsi.ispublic** property. Add the following syntax to the script include:

 `isPublic:function(){return[true/false];},`

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

