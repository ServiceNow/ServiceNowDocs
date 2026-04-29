---
title: Configure adaptive authentication properties
description: After activating adaptive authentication, configure adaptive authentication properties according to your security requirements.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Adaptive authentication, Authentication, Access Management]
---

# Configure adaptive authentication properties

After activating adaptive authentication, configure adaptive authentication properties according to your security requirements.

## Before you begin

Role required: adaptive\_auth\_admin

## Procedure

1.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Authentication Policies** &gt; **Properties**.

2.  Configure these properties:

<table id="table_rrw_sgb_xnb"><thead><tr><th>

Property

</th><th>

Description

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Enable Authentication Policy \(glide.authenticate.auth.policy.enabled\)

</td><td>

Option to enable the authentication policy.

</td><td>

Yes \| No

</td></tr><tr><td>

Enable debug logging for authentication policies \(glide.authenticate.policy.debug\)

</td><td>

Option to enable debug logging for the authentication policies.

</td><td>

Yes \| No

</td></tr><tr><td>

HTTP error code to be displayed to the user when access is blocked by Global Blocking Policy \(glide.authenticate.global.blocking\_policy.error\_code\)

</td><td>

HTTP error code that displays during login when the Global Blocking Policy blocks a user login.

</td><td>

Select from:-   Forbidden\(403\)
-   Not Found\(404\)


</td></tr><tr><td>

Error message to be displayed to the user when access is blocked by Global Blocking Policy \(only applicable when Forbidden\(403\) HTTP error code is selected\) \(glide.authenticate.global.blocking\_policy.error\_message\)

</td><td>

Error message that displays when the Global Blocking Policy blocks access.

</td><td>

Text field

</td></tr><tr><td>

Enable Device Trust Flow \(glide.authenticate.preauth.allow.trusted.device\)

</td><td>

Option to enable the trusted device flow.

</td><td>

Yes \| No

</td></tr><tr><td>

Maximum number of trusted device a user can register \(glide.trusted.device.max.count\)

</td><td>

It is the maximum number of trusted device a user can register.

</td><td>

Text field

</td></tr><tr><td>

Skip the device registration for device trust flow if the user is from the trusted network \(glide.authenticate.preauth.skip.user.registration\)

</td><td>

Option to skip registration if the user is trying to register from the trusted network

</td><td>

Yes \| No

</td></tr><tr><td>

Property to enable the Session Validation feature. Set this to true after activating the Session Validation Context's Policy and setting up your desired filters and conditions \(session.validation.enabled\)

</td><td>

Option to enable the Session Validation feature. Set this to true after activating the Session Validation Context's Policy and setting up your desired filters and conditions.

</td><td>

Yes \| No

</td></tr></tbody>
</table>
