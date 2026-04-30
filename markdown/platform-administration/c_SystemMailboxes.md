---
title: System mailboxes
description: Email messages can be seen in the System Mailboxes menu, which gives you access to the system Inbox, Outbox, and Sent mail box.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Email Administration, Notifications, Configure core features, Administer]
---

# System mailboxes

Email messages can be seen in the System Mailboxes menu, which gives you access to the system Inbox, Outbox, and Sent mail box.

Each provides a filtered view of emails to let you see only what you need to at any given time, including list fields applicable to each. The system mailboxes menu shows your current POP and SMTP status.

The System Mailbox is hosted by ServiceNow, who have sole access to the mailboxes. By default, once the instance pulls an email message, it is deleted from the mail server and stored in the application on the Email \[sys\_email\] table.

For information about the fields that are shown in the System Mailbox, see [System email log and mailboxes](../../time/reference/r_EmailLogs.md). You can configure the layout of a system mailbox to show any of the email log fields, not only the ones that are shown by default.

-   **Inbound emails**: All inbound mail is placed into the Inbox until it is processed. After it is cleared, the email moves to the Received state. If the email message matches the criteria in an inbound email action, the email is changed to Processed. If not, it is changed to Ready. If the system is restarted for any reason \(such as during a system upgrade\), all inbound mail waits on the external mail server until the system can request delivery.
-   **Outbound emails**: All outbound mail is placed into the Outbox until it is processed. Once cleared, it is moved to Sent \(if sent\) or Skipped \(not sent, as in the case of no valid recipients\). If the system is restarted for any reason \(such as during a system upgrade\), all outbound mail waits in the instance database until the system comes online, and the scheduler looks for mail to deliver.

