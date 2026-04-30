---
title: Inbound email action processing
description: The system determines which inbound actions to run by comparing the inbound email type and inbound action conditions to the incoming email message. Certain properties are available to set the reply and forwarding prefixes in the email subject lines that your instance recognizes when processing inbound emails.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Inbound email actions, Inbound email, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Inbound email action processing

The system determines which inbound actions to run by comparing the inbound email type and inbound action conditions to the incoming email message. Certain properties are available to set the reply and forwarding prefixes in the email subject lines that your instance recognizes when processing inbound emails.

**Note:** Inbound email flows take priority over inbound email actions. If you create flows with inbound email triggers, emails are first processed by the inbound email triggers before they are processed by inbound email actions.

The system follows this processing flow to determine whether to run an inbound action.

![](../image/inbound-action-processing.png "Inbound action processing work flow")

The system only runs an inbound action when:

-   The incoming email type matches the inbound action **Type**.
-   If present, the watermark or record number refers to a record in the **Target table**.
-   The inbound action **Conditions** evaluates to true.

If any of these criteria are not met, the system skips the current inbound action and evaluates the next active inbound action. The system processes inbound actions from the lowest to highest **Order** value. If the inbound action has **Stop processing** enabled, the system updates the **State** of the email record to **Processed** after running the inbound action **Script**.

The following video shows how an inbound action condition prevents an incident from being created.

Troubleshooting when inbound email isn't processed

## Prefixes recognized in email subject lines

-   **Email reply prefixes**

    When no watermark is present or the In-Reply-To email header is present, the instance recognizes email containing a prefix from the **glide.email.reply\_subject\_prefix** property as reply email. You can use this property to set non-standard reply prefixes in your email system.

<table id="table_yf2_kgg_dcb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.email.reply\_subject\_prefix

</td><td>

Specifies the comma-separated list of prefixes in the subject line that identify an email reply.-   Type: string
-   Default value: re:,aw:,r:,Accepted:,Tentative:,Declined:
 **Note:** The case of the reply prefix in the email, for example RE:, must exactly match the case of the prefixes defined in this property. If, for example, an email contains the Re: prefix and only RE: is defined in the property, the email will not be recognized as a reply. Therefore, it is a best practice to define multiple versions of the prefix, including mixed-case versions, such as RE:, Re:, and so on.

</td></tr></tbody>
</table>-   **Email forward prefixes**

    Emails with certain prefixes trigger the forward type of inbound email action. The instance recognizes any email whose subject line contains a prefix from the **glide.email.forward\_subject\_prefix** property as forwarded email. Emails with these prefixes trigger inbound email actions of the type forward. Use this property to set non-standard forward prefixes in your email system or you want email forwards to behave like replies. If the value of the system property is empty, then the system reverts to using the values **fw:** and **fwd:**.

<table id="table_bf1_jhg_dcb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.email.forward\_subject\_prefix**

</td><td>

Specifies the list of prefixes \(comma-separated\) in the subject line that identify a forwarded email.-   Type: string
-   Default value: fw:,fwd:
-   Location: Add to the System Properties \[sys\_properties\] table
 **Note:** Prefixes are case insensitive.

</td></tr></tbody>
</table>-   **Email forwards as replies**

    Properties are available to force inbound actions to process forwarded mail as replied mail. These properties control the subject prefix that the inbound actions use.

    |Property|Value needed|
    |--------|------------|
    |**glide.email.reply\_subject\_prefix**|re:,Re:,RE:,aw:,r:,fw:,fwd:,Fwd:,FWD:|
    |**glide.email.forward\_subject\_prefix**|\[any text that is not a forward prefix\]|

    These properties cause the Update Incident inbound action to process all forwarded and replied-to mail.

    **Note:** The **glide.email.forward\_subject\_prefix** property must contain some text so that the forwarded email can be processed as a Reply. It can be any text except a forward prefix \(that is, fw:,fwd:,Fwd:,FWD:\).


## Matching a sender email address to a user

The instance matches a senders email address to an active user in the User \[sys\_user\] table using inbound actions.

When processing an email, the instance sets the current user to the user whose email address matches **email.from**. Inbound actions can then reference that current user. For example, the base system inbound action Create Incident sets the **caller\_id** of the incident to the value returned by `gs.getUserID()`.

If multiple users have the same email address, the instance first searches for an active user with the email address. The instance does not match inactive users.

**Note:** Each user record must have a unique email address so that the instance can reliably match the email to the correct user.

If a unique email address for each user is not possible, assign a shared email address to only one active user so that the instance always matches incoming email from that address to the active user.

## Matching watermarks in the Subject line or Body

The following examples illustrate how the instance matches randomized watermarks in an email subject line or body.

**Note:** For instances upgraded from a release before Jakarta, the system can recognize both randomized and non-randomized watermarks during a watermark transition period.

|Subject Line or Body Contents|Matching Results|
|-----------------------------|----------------|
|Ref:MSG0000008\_ aLJc130zDhCVuh3spXmt|The instance recognizes this string as a watermark and searches the Email Watermarks \[sys\_watermark\] table for a record with the number MSG0000008\_ aLJc130zDhCVuh3spXmt. If this watermark exists, the instance matches the email to the associated record. If this watermark does not exist, the system processes inbound email messages as described in .|
|Ref:MSGWTR0000008\_wfLLz42IxCgUvG2JlYnh|The instance recognizes this string as a watermark and searches the Email Watermarks \[sys\_watermark\] table for a record with the number MSGWTR0000008\_wfLLz42IxCgUvG2JlYnh. If this watermark exists, the instance matches the email to the associated record. If this watermark does not exist, the system processes inbound email messages as described in .|

## Matching record numbers in the Subject line or Body

The following examples illustrate how the instance matches record numbers in the subject line of an email to an existing record when no watermark is present.

<table id="table_uc4_qjv_m4"><thead><tr><th>

Subject line contents

</th><th>

Matching results

</th></tr></thead><tbody><tr><td>

RE: Example INC0005574

</td><td>

The instance recognizes this subject line as a reply and recognizes the INC prefix as belonging to the Incident table. The instance searches the Incident table for an existing record `INC0005574`. If this incident exists, the email is associated with this incident. If this incident record does not exist, the instance uses the inbound action for new emails to create an incident and associates the new incident with the email.

</td></tr><tr><td>

RE: Example "INC0005574"

 RE: Example \*INC0005574

</td><td>

The instance recognizes this subject line as a reply but does not recognize the `"INC` prefix as belonging to the Incident table because of the quotation mark. The same error occurs for any character other than a space before the record number. The instance instead uses the inbound action for new emails to create an incident and associates the new incident with the email.

</td></tr><tr><td>

RE: "Example INC0005574"

 RE: Example INC0005574\*

</td><td>

The instance recognizes this subject line as a reply and recognizes the `INC` prefix as belonging to the Incident table. The instance searches the Incident table for an existing record `INC0005574"`, which it cannot find because of the quotation mark. The same error occurs for any character other than a space at the end of the record number. The instance instead uses the inbound action for new emails to create an incident and associates the new incident with the email.

</td></tr><tr><td>

RE: CHG0008593 and INC000576

</td><td>

The instance recognizes this subject line as a reply and recognizes one, but not both, of the number prefixes. There is no way to predict which prefix the instance matches first. Whichever prefix it matches, it searches the corresponding table for a matching record. If the record exists, the email is associated with the table. If the record does not exist, the instance uses the inbound action for new emails to create an incident and associates the new incident with the email.**Note:** The instance does not support processing email with multiple numbers in the subject line because there is no way to predict which record the instance matches first. For this reason, do not include more than one $number variable in your notifications.

</td></tr><tr><td>

FW: Example INC0005574

</td><td>

The instance recognizes this subject line as a forward because of the `FW:` prefix. It uses the inbound action for forwarded emails to create an incident and associates the new incident with the email.

</td></tr><tr><td>

Example INC0005574

</td><td>

The instance recognizes this subject as a new email because it does not contain a matching reply or forward prefix. It uses the inbound action for new emails to create an incident and associates the new incident with the email.

</td></tr></tbody>
</table>**Parent Topic:**[Inbound email actions](actions-inbound-email.md)

