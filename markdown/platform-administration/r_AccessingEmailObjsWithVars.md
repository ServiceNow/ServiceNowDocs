---
title: Accessing email object variables
description: An inbound email action script contains the email object to access various pieces of an inbound email through variables. You can use the global variable sys\_email with inbound email actions.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [References, Inbound email, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Accessing email object variables

An inbound email action script contains the email object to access various pieces of an inbound email through variables. You can use the global variable *sys\_email* with inbound email actions.

<table id="table_sbj_31q_n4"><thead><tr><th>

Variable

</th><th>

Contents

</th></tr></thead><tbody><tr><td>

*email.to*

</td><td>

Contains a comma-separated list of email addresses in the To: and Cc: boxes.

</td></tr><tr><td>

*email.direct*

</td><td>

Contains a comma-separated list of email addresses in the To: box.

</td></tr><tr><td>

*email.copied*

</td><td>

Contains a comma-separated list of email addresses in the Cc: box.

</td></tr><tr><td>

*email.body\_text*

</td><td>

Contains the body of the email as a plain text string.

</td></tr><tr><td>

*email.body\_html*

</td><td>

Contains the body of the email as an HTML string.

</td></tr><tr><td>

*email.from*

</td><td>

Contains an email address that depends on the following conditions:-   If the address listed in the email **Headers** field matches an existing user's **Email address**, this variable contains the user's email address.
-   If the address listed in the email **Headers** field does not match an existing user's **Email address**, this variable contains the address listed in the email **Headers** field.

</td></tr><tr><td>

*email.from\_sys\_id*

</td><td>

Contains the Sys ID of the user who sent the email to the instance.

</td></tr><tr><td>

*email.fromAddress*

</td><td>

If system property **glide.email.inbound\_action.extract\_from\_header** property is set to true, **origemail** is computed from the headers. The default value is false if the property does not exist.

</td></tr><tr><td>

*email.origemail*

</td><td>

Contains the address of the email sender as listed in the email **Headers** field.

</td></tr><tr><td>

*email.subject*

</td><td>

Contains the subject of the email as a plain text string.

</td></tr><tr><td>

*email.recipients*

</td><td>

Contains a comma-separated list of recipient addresses as a plain text string, in the To: box.

</td></tr><tr><td>

*email.recipients\_array*

</td><td>

Contains the recipient addresses as an array.

</td></tr><tr><td>

*email.content\_type*

</td><td>

Contains the MIME content type of the email \(for example,*text/plain; charset="us-ascii"* or *text/html; charset="us-ascii"*\).

</td></tr><tr><td>

*email.headers*

</td><td>

Contains details about the sender, route, and receiver as a plain text string in the format of the sending email client.

</td></tr><tr><td>

*email.importance*

</td><td>

Contains an indication from the sender about how important a message is. The value can be **High**, **Low**, or empty.

</td></tr></tbody>
</table>**Note:** The instance follows [RFC 2822](http://www.rfc-editor.org/info/rfc2822) \(Internet Message Format\), which requires multiple email addresses in a group to be separated by commas, not semicolons. The instance can set the values of the *email.to*, *email.direct*, and *email.copied* variables only if emails addressed to groups follow the expected RFC format.

## Inbound email.recipient variables

The recipients variables \(*email.recipients*, *email.recipients-array*\) allow processing of inbound email based on the email recipients. For example, you can create a script to process email based on the array values:

```
var rarray  = email.recipients_array ; for ( var i  = 0 ; i  < rarray.length ; i ++ ) { var recipient  = rarray [i ] ; // do something with it } 
```

## The sys\_email variable

This variable lets you access the received sys\_email record that triggered the inbound email action. It can be used to reference fields on the email record, such as **uid**, **sys\_id**, **content\_type**, and so on.

**Parent Topic:**[References for Inbound email](../concept/references-inbound-email.md)

