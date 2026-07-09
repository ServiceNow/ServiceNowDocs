---
title: Intelligent approvals reference
description: Reference topics for intelligent approvals, including the user roles required to access the Intelligent Approvals homepage and create AI-generated approval policies.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-05-20"
reading_time_minutes: 1
keywords: [reference, intelligent approvals, Approver Agent, user roles, AI approval policies]
---

# Intelligent approvals reference

Reference topics for intelligent approvals, including the user roles required to access the Intelligent Approvals homepage and create AI-generated approval policies.

## User roles

The following roles control access to intelligent approvals features.

|Role|Description|Contains|
|----|-----------|--------|
|sn\_iap.policy\_admin|Has read, write, and delete access to all intelligent approval tables and artifacts.|sn\_iap.policy\_manager|
|sn\_iap.policy\_manager|Has access to the homepage, intelligent approvals, and execution details.|sn\_iap.policy\_reader, taas\_api\_write|
|sn\_iap.policy\_reader|Has read-only access to the homepage, intelligent approvals, and execution details.|taas\_api\_read|
|sn\_iap.policy\_runtime|Has access to runtime policy evaluation skills.|sn\_iap.policy\_reader|

Contact your system administrator to verify role assignments. For information about activating the Intelligent Approvals plugin and configuring role assignments, see [Configure intelligent approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/configure-intelligent-approvals.md).

