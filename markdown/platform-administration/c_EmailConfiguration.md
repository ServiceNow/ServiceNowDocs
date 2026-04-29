---
title: Email administration
description: All email notifications use the email properties that you define for your instance and the email accounts that you set up. Your email service can also affect the successful transmission of incoming and outgoing email.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Email administration

All email notifications use the email properties that you define for your instance and the email accounts that you set up. Your email service can also affect the successful transmission of incoming and outgoing email.

## Email accounts

Email administrators set up [email accounts](../../notification/concept/c_EmailAccounts.md) to allow the system to connect to external mail services such as POP3, SMTP, or IMAP servers. You can use the ServiceNow - provided email accounts or create your own accounts for your own email services.

## Email properties

Use [Email Properties](c_EmailProperties.md) to configure settings for inbound and outbound email. Email properties apply to all email accounts.

## Email service size restrictions

Your email service, whether you are using a standard ServiceNow email configuration or an alternate email configuration, determines the successful transmission of incoming or outgoing emails based on a maximum email size. An email configuration consists of your instance, email server, and email client.

-   [Standard email configurations](c_StandardEmailConfiguration.md) – For instances that use the standard email configuration, the ServiceNow mail servers cannot send or receive emails larger than approximately 50 MB \(before encoding\), including the email header, body text, and attachments. Email messages are encoded by an email client, which increases total email message size. The maximum ServiceNow mail server size restriction is 75 MB \(after encoding\). The maximum email size limit is enforced regardless of any configured attachment size limits.
-   [Alternate email configurations](c_AlternateEmailConfigurations.md) – If your email service uses a company-owned or third-party server, the approximate size restriction of 50 MB \(including the email header, body text, and attachments\) may still apply. However, your service might support different maximum total file sizes for inbound and outbound emails. Check with the email administrator of your email service to verify email size limits.

For details on how encoding can affect email message size and email transmission, see [KB0521772](https://support.servicenow.com/kb_view.do?sysparm_article=KB0521772).

## Email service availability

Email service is intentionally shut down on instance clones to prevent resending already delivered email. Upgrades no longer require an extended interruption of email service. Instances continue to process email during an upgrade. For a possible explanation for undelivered emails, see [this blog post](https://community.servicenow.com/community?id=community_blog&sys_id=4acd62e9dbd0dbc01dcaf3231f961958) by a ServiceNow Technical Support Engineer in the ServiceNow Community.

For instructions on creating and sending custom emails when events on the instance occur, see the tasks in [Email and SMS notifications](../../notification/concept/c_EmailNotifications.md).

## Instance-to-instance communication via email

Use [Web services](https://www.servicenow.com/docs/access?context=r_AvailableWebServices&version=australia&pubname=australia-api-reference&ft:locale=en-US) to communicate between two instances.

## Designate untrusted and trusted email domains

Using Instance Security Center, you can monitor the blocked and allowed incoming email metrics for your instance. For more information, see [Designate untrusted and trusted email domains](https://www.servicenow.com/docs/access?context=designate-untrusted-trusted-email-domains&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Next steps after enabling email

After enabling email on your instance, consider performing several of these important tasks.

-   Test the email configuration by routing all email to a single user \(set the **glide.email.test.user** property\).
-   Review the baseline notification categories, email notifications, and templates to determine if they meet your business needs.
-   Review the baseline inbound email actions to determine if they meet your business needs.
-   Determine if you want to use email layouts to add consistent content elements.
-   Determine if you want to use email filters to restrict the email the instance receives.
-   Determine if you want to implement a retention policy to archive and destroy email at certain intervals.
-   Determine what kind of watermarks outbound email uses to associate records with email messages.
-   Determine if you want to create users when the instance receives an email from an unrecognized user.
-   Set the precedence of outgoing mail. By default, the instance sends email with a precedence of bulk \(set the**glide.smtp.precedence\_bulk** property\).
-   Consider preventing untrusted users from triggering inbound actions to prevent unwanted email from affecting your instance.
-   Implement a spam filter to restrict unwanted messages sent to your custom email addresses.

