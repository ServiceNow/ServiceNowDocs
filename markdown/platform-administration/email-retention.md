---
title: Email retention
description: You can archive and eventually destroy email messages that you no longer need or if your Email table is excessively large.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Email retention

You can archive and eventually destroy email messages that you no longer need or if your Email table is excessively large.

Email retention is available starting with the Helsinki release.

## Email archive and destruction plugins

The email archiving and destruction feature uses the [Data archiving](../../database-rotation/concept/c_ArchiveData.md) and [Email Retention](../task/t_ActivateTheEmailRetentionPlugin.md) plugins. The Data Archiving plugin must be active to archive and destroy email records. The Email Retention plugin provides a set of rules that specify when the system archives and destroys email records.

**Note:** The Email Retention plugin also prevents the system from deleting watermarks, which are required for inbound email actions to continue to function.

The Email Retention plugin and associated archive and destroy rules are active by default on new instances. On upgraded instances, you must manually activate both the plugin and the archive and destroy rules. ServiceNow recommends that you review and approve these rules before activating them.

If your instance already has a process to manage email records, you do not need to activate the Email Retention plugin. If you want to replace your current process with Email Retention, be sure to deactivate the current process before activating the archive and destroy rules.

## Archiving and destroying email records

Archiving means moving records from the Email \[sys\_email\] table to the Archive Email \[ar\_sys\_email\] table when they exceed the archive rule time limit. Destroying means deleting records in the Archive Email table when they exceed the destroy rule time limit.

**Note:** When a destroy rule deletes email records, associated watermarks are not deleted. They are preserved to ensure that your inbound email actions continue to function.

## Default archive and destroy rules

Email Retention provides this email archive rule:

**Email - Over a year old or Ignored**: archives email message records that were created more than 365 days prior to the current date and are of type **received-ignored** or **sent-ignored**.

Email Retention also provides this email destroy rule:

**Email Archive - Over a year old:** destroys email records that have been archived for more than 365 days prior to the current date.

With these default settings, your email messages are kept on the instance for a total of two years: one year in the Email table, and one year in the Email archive table. At the end of this period, the system deletes the expired email records from the Email archive table.

**Note:** By default these rules are active on new instances and inactive on upgrades. The system runs archive and destroy rules when you activate them.

## Compatibility with other record management implementations

If you are already using another method to manage email records, such as table cleaners, you do not have to use the Email Retention feature. To prevent unexpected record deletion, ServiceNow recommends that you avoid using multiple email management processes on the same instance at the same time.

**Note:** For assistance replacing your existing record management implementation with Email Retention, contact your professional services or sales representative.

## Effects of archiving and deleting email records

Inbound email actions copy the body of an email to the work notes of the related record. If the inbound email record is later deleted, Email Received section is no longer visible in the work notes though it still contain a text copy of the email.

When the system sends an email message about a record, the activity formatter displays a **Sent Email** section with a link to the email message. If the system archives the email message, the activity formatter removes **Sent Email** section. When the system deletes the email message, it is no longer visible in the activity formatter nor the work notes.

**Note:** Set the archive time length long enough so your users can access sent emails though the activity formatter.

Archiving email records changes the methods available to the system to identify inbound email as a reply. After archiving an email record, the system can no longer use the **In-Reply-To** field to match an incoming email to an email record. However, the system can still match incoming email to an existing record from a record number or watermark.

