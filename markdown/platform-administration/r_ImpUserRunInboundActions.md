---
title: User impersonations and inbound actions
description: When the instance receives an email, it can take a variety of actions by impersonating the sender.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [References, Inbound email, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# User impersonations and inbound actions

When the instance receives an email, it can take a variety of actions by impersonating the sender.

If the sender of an incoming email matches an existing user, the instance impersonates the matching user to complete any inbound email actions. If the sender does not match an existing user, the instance impersonates the Guest user to complete any inbound email actions. If the impersonated user is locked out, the inbound email action fails.

**Note:** If inbound email comes from an untrusted domain, the instance impersonates the Guest user unless you explicitly prevent users from untrusted domains from triggering inbound actions. For more information on filtering domains, see Designate untrusted and trusted email domains.

**Parent Topic:**[References for Inbound email](../concept/references-inbound-email.md)

