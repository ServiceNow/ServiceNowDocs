---
title: Restrict access to GlideSystemUserSession scriptable API \[Updated in Security Center 1.3 and 2.0\]
description: The client callable GlideSystemUserSessionSandbox scriptable API exposes GlideSystemUserSession's addErrorMessageNoSanitization and addInfoMessageNoSanitization methods to the JavaScript sandbox. This allows all users to call this method via script.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Restrict access to GlideSystemUserSession scriptable API \[Updated in Security Center 1.3 and 2.0\]

The client callable GlideSystemUserSessionSandbox scriptable API exposes GlideSystemUserSession's addErrorMessageNoSanitization and addInfoMessageNoSanitization methods to the JavaScript sandbox. This allows all users to call this method via script.

gs.addErrorMessageNoSanitizationMessaging\(\) and gs.addInfoMessageNoSanitization\(\) are used within the scripting environment for logging and notifications. Both of these are available in the sandbox if this property is not set to the recommended value of false. The sandbox is a low privileged scripting environment available to unauthenticated and no role users. Both of these methods can be used to display unsanitized input to a user. Displaying unsanitized input to the user is dangerous, as unsanitized input may contain dangerous code that runs in the user's browser. This can be utilized for traditional reflected XSS attacks. Reflected XSS attacks can be used in multiple scenarios, including session hijacking.

Set **glide.sandbox.usersession.allow\_unsanitized\_messages** system property to **false**. If there is not record of this property in the System Properties \[sys\_properties\] table, create one.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.sandbox.usersession.allow\_unsanitized\_messages**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Access control](sc-access-control.md)|
|Purpose|This property will restrict unsanitized informational or error messages from being called in a sandboxed user session.|
|Type|Boolean|
|Recommended value|false|
|Default value|true|
|Security risk rating|8.1|
|Functional impact|Set the property with the value false will result in no message creation or logging should those functions get called.|
|Security risk|\(High\) Without appropriate sanitization, potentially dangerous content may be accessed and the unsanitized error function is available to script.|
|References|[Access control](sc-access-control.md)|

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

