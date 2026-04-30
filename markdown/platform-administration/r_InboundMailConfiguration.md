---
title: Inbound mail configuration
description: The Inbound Mail Configuration section of the Email Properties page contains properties to control inbound email.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Email properties, Configure email administration, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Inbound mail configuration

The **Inbound Mail Configuration** section of the Email Properties page contains properties to control inbound email.

<table id="table_bbt_1ry_bp"><thead><tr><th>

Property

</th><th>

Label

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.email.read.active**

</td><td>

Email receiving enabled

</td><td id="entry_EmailReceiptEnabled">

Specifies whether to enable or disable the inbound mail server.-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

**glide.email.reply\_subject\_prefix**

</td><td id="entry_EmailReplySubjectProperty">

Identify email as a reply by these subject prefixes

</td><td id="entry_EmailReplySubjectDesc">

Specifies the comma-separated list of prefixes in the subject line that identify an email reply.-   Type: string
-   Default value: re:,aw:,r:,Accepted:,Tentative:,Declined:

 **Note:** The case of the reply prefix in the email, for example RE:, must exactly match the case of the prefixes defined in this property. If, for example, an email contains the Re: prefix and only RE: is defined in the property, the email will not be recognized as a reply. Therefore, it is a best practice to define multiple versions of the prefix, including mixed-case versions, such as RE:, Re:, and so on.

</td></tr><tr><td>

**glide.email.forward\_subject\_prefix**

</td><td id="entry_EmailForwardSubjectProperty">

Identify email as a forward by these subject prefixes

</td><td id="entry_EmailForwardSubjectDesc">

Specifies the comma-separated list of prefixes in the subject line that identify a forwarded email.-   Type: string
-   Default value: fw:,fwd:

 **Note:** The case of the forward prefix in the email, for example fw:, must exactly match the case of the prefixes defined in this property. If, for example, an email contains the Fwd: prefix and only fwd: is defined in the property, the email will not be recognized as a forward. Therefore, it is a best practice to define multiple versions of the prefix, including mixed-case versions, such as FWD:, Fwd:, and so on.

</td></tr><tr><td>

**glide.pop3readerjob.create\_caller**

</td><td id="entry_AutoCreateUsersProperty">

Automatically create users for incoming emails from trusted domains

</td><td id="entry_AutoCreateUsersDesc">

Controls the behavior when an instance receives an email from an email address not associated with a user record. If this property is set to **true**, the instance creates a new user record for the email address and places that new user in the **Caller** field of any tickets created. If the property is set to **false**, the instance places **Guest** in the **Caller** field of any tickets created.-   Type: true \| false
-   Default value: false
-   Learn More:Enabling Automatic User Creation

</td></tr><tr><td>

**glide.user.default\_password**

</td><td id="entry_DefaultPasswordProperty">

Default password for users created from email sent from trusted domains. \(must reset upon login\)

</td><td id="entry_DefaultPasswordDesc">

Specifies the password for new users created from incoming email. Users must reset the password at first login.-   Type: string
-   Default value: password
-   Learn More:Enabling Automatic User Creation

</td></tr><tr><td>

**glide.user.trusted\_domain**

</td><td id="entry_TrustedDomainsProperty">

Trusted domains when creating users from incoming email.

</td><td id="entry_TrustedDomainsDesc">

Comma-separated list of trusted domains for which the instance automatically creates a user based on incoming emails. Use an asterisk \(\*\) to trust all domains. If an email is not from a trusted domain, the instance processes the inbound email as a "guest user" but it does not create a guest user in the instance. -   Type: string
-   Default value: servicenow.com
-   Learn More:Enabling Automatic User Creation

</td></tr></tbody>
</table>**Parent Topic:**[Email properties](../concept/c_EmailProperties.md)

**Related topics**  


[Outbound mail configuration](r_OutboundMailConfiguration.md)

[Email image filtering properties](../../notification/concept/email-image-filters.md)

[Email digest properties](../../notification/concept/email-digest-properties.md)

[Advanced email properties](r_AdditionalProperties.md)

