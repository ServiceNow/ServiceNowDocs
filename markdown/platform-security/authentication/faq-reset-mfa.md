---
title: MFA reset
description: FAQ related to MFA reset and why it’s important.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Frequently asked questions, MFA enforcement, Multi-factor authentication, Authentication, Access Management]
---

# MFA reset

FAQ related to MFA reset and why it’s important.

1.  Lost the authenticator app setup. How can I reset?

    It’s better if the users enroll in multiple factors so that they aren’t locked out due to MFA. For example, you can have the TOTP authenticator app, passkey, and email OTP-based MFA.

    In case users are unable to use any of the enrolled MFA factors the administrator can reset the MFA by following these steps.

    1.  Clearing the Authenticator app setup:
        -   Navigate to **All** &gt; **Multi-factor Authentication** &gt; **User Multi-factor Setup**.
        -   Search for the user in the table.
        -   Delete the record associated with the user
    2.  Clearing the FIDO2 authenticators and passkeys:
        -   Navigate to **All** &gt; **Multi-factor Authentication** &gt; **Web Authentication** &gt; **User Public Credentials**.
        -   Search for the user in the table
        -   Delete the records associated with the user
    3.  Clearing other multi-factor setups associated with the user
        -   Navigate to **All** &gt; **Multi-factor Authentication** &gt; **User Multi-factor Setup**.
        -   Search for the user in the table
        -   Delete the records associated with the user
    In case no one including the admin can access the instance. The admin can perform a self-service MFA reset using a catalog item available at [Now support](https://support.servicenow.com/now).

2.  How to avoid administrators from lockout due to MFA?

    The administrators enroll for multiple MFA factors so that they aren’t blocked from accessing the instance.

    In case no one including the admin can access the instance. The admin can perform a self-service MFA reset using a catalog item available at [Now support](https://support.servicenow.com/now).


