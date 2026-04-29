---
title: Require authentication by default for client-callable script includes
description: By default, client-callable script includes that do not explicitly set visibility, are public. If needed, add the glide.script.ccsi.ispublic property to enable privacy control over all client-callable script includes accessed by public pages.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Require authentication by default for client-callable script includes

By default, client-callable script includes that do not explicitly set visibility, are public. If needed, add the **glide.script.ccsi.ispublic** property to enable privacy control over all client-callable script includes accessed by public pages.

The **glide.script.ccsi.ispublic** system property makes sure that client-callable script-includes, also known as Ajax script includes, are not automatically made available to non-authenticated users. If **glide.script.ccsi.ispublic** is not set to the recommended value of **false**, then it allows script includes to be run as public scripts and allow unauthenticated users access to instance data.

Ensure that the property **glide.script.ccsi.ispublic** is set to **false**.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.script.ccsi.ispublic**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

 

</td></tr><tr><td>

Recommended value

</td><td>

false

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.5
-   CVSS rating: High
-   Security risk details: Sensitive business logic or data is potentially exposed, increasing the risk of unauthorized access to instance resources.

</td></tr><tr><td>

Functional impact

</td><td>

If the client-callable script includes are designated as public \(that is, this property is missing\), then unauthenticated users can execute client scripts. Add the property restricts the execution of scripts by a non-logged-in user.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

