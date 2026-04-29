---
title: Redirecting email to the instance POP3 account
description: Configure other mailboxes to forward email to the instance's POP3 account.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [References, Inbound email, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Redirecting email to the instance POP3 account

Configure other mailboxes to forward email to the instance's POP3 account.

By default, the **POP Reader** scheduled job checks for new email every two minutes. It connects to the mail server and account specified in email properties. The **POP Reader** downloads any email waiting on the mail server and creates **email.read** events. After the instance processes the events, the inbound email actions run.

The **POP Reader** shows the number of emails processed during the reader's last run. The message shows the number of emails the reader processed or `0 processed` if no emails were available. The reader resets the status each time it runs.

It is not possible to specify more than one POP3 account for an instance, but you can forward other mailboxes to the designated POP3 account. This script can be added to the Create Incident inbound email action to differentiate the content based on the original recipient, and then set an *assignment\_group* value.

There can be multiple active POP3 accounts with different email addresses but only one instance POP3 account.

```
if(email.direct.indexOf('facilities@anycorp.com')>-1)
current.assignment_group.setDisplayValue('Facilities Management');
```

**Parent Topic:**[References for Inbound email](../concept/references-inbound-email.md)

