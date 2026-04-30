---
title: Email bounce management
description: Help prevent sending emails to addresses that are known to generate bounces by monitoring and filtering them out while sending emails.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Advanced email setup, Configure email administration, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Email bounce management

Help prevent sending emails to addresses that are known to generate bounces by monitoring and filtering them out while sending emails.

## Email bounce

An email bounce signifies the non-delivery of your email message according to [RFC3464](https://www.rfc-editor.org/rfc/rfc3464). When an email gets bounced, the sender receives a delivery status email with the reason for the bounce and the associated status code. For more information about these status codes, see [Status codes.](https://www.rfc-editor.org/rfc/rfc3463)

An email address is blocked after it reaches a certain threshold of bounced emails. The default count for blocking the bounced email addresses is 10.

To view the bounce email addresses, navigate to **All** &gt; **System Logs** &gt; **Bounce Email Addresses**.

**Important:** Disabling bounce management is not recommended as it may lead to slow delivery or blocking of emails by the email provider.

## Status code

The syntax of the status codes is defined as the following:

```
status-code = class "." subject "." detail

      class = "2"/"4"/"5"

      subject = 1*3digit

      detail = 1*3digit
```

The first subcode indicates whether the delivery attempt was successful. The second subcode indicates the probable source of any delivery anomalies. The third subcode indicates a precise error condition.

## Status codes

|Code|Summary|Description|
|----|-------|-----------|
|5.1.1|Bad destination mailbox address|The mailbox specified in the address doesn't exist. For email names, this means the address portion to the left of the "@" sign is invalid.|

The default status codes that are used for blocking bounced email addresses are 5.0.\*, 5.1.\* and 5.7.\*, where the asterisks \(\*\) could be any number in the series according to the status code specification.

![Example bounce email address status codes](../image/bounce-email-address-status.png)

**Note:** There is a possibility that some email providers may use non-standard RFC status codes, potentially leading to functional email addresses being blocked. Administrators action is required to unblock these status codes and email addresses.

To view the blocked status codes, navigate to **All** &gt; **System Mailboxes** &gt; **Administration** &gt; **Bounce Email Address Status**.

-   **[Configure bounce email address status](../task/config-email-address-status.md)**  
Configure a bounced email address status according to type, class, subject, and details.
-   **[Resend all blocked emails](../task/resend-all-blocked-emails.md)**  
Unblock the email address and resend all blocked emails.

**Parent Topic:**[Advanced email setup](../../reference-pages/concept/c_AlternateEmailConfigurations.md)

**Related topics**  


[Configure bounce email address status](../task/config-email-address-status.md)

[Check the status of bounced email addresses](../task/change-bounce-email-status.md)

