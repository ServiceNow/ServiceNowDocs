---
title: Restrict access to GlideSystemUserSession scriptable API
description: The client callable GlideSystemUserSessionSandbox scriptable API exposes GlideSystemUserSession's addErrorMessageNoSanitization and addInfoMessageNoSanitization methods to the JavaScript sandbox. This allows all users to call this method via script.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Restrict access to GlideSystemUserSession scriptable API

The client callable GlideSystemUserSessionSandbox scriptable API exposes GlideSystemUserSession's addErrorMessageNoSanitization and addInfoMessageNoSanitization methods to the JavaScript sandbox. This allows all users to call this method via script.

The methods gs.addErrorMessageNoSanitizationMessaging\(\) and gs.addInfoMessageNoSanitization\(\) are used within the scripting environment for logging and notifications. Both of these are available in the sandbox if this property is not set to the recommended value of **false**. The sandbox is a low privileged scripting environment available to unauthenticated and no role users. Both of these methods can be used to display unsanitized input to a user.

Ensure that the **glide.sandbox.usersession.allow\_unsanitized\_messages** system property is set to **false**. If this property does not exist on the System Properties \[sys\_properties\] table, create the property.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.sandbox.usersession.allow\_unsanitized\_messages**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Boolean

</td></tr><tr><td>

Recommended value

</td><td>

false

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Fallback value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 8.1
-   CVSS rating: High
-   Security risk details: Displaying unsanitized input to the user is dangerous, as unsanitized input may contain dangerous code that runs in the user's browser. This can be utilized for traditional reflected XSS attacks. Reflected XSS attacks can be used in multiple scenarios, including session hijacking.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

