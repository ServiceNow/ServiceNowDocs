---
title: Remove members from an identity group
description: Remove a member from an identity group when that member no longer requires access to secrets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/usg-remove-members-identity-group.html
release: australia
topic_type: task
last_updated: "2026-10-08"
reading_time_minutes: 1
keywords: [identity group members, member removal, unified secrets gateway]
breadcrumb: [Configuring Unified Secrets Gateway, Unified Secrets Gateway, Encryption]
---

# Remove members from an identity group

Remove a member from an identity group when that member no longer requires access to secrets.

## Before you begin

Role required: admin or cryptographic\_manager

## Procedure

1.  Navigate to **All**, type **sys\_secret\_identity\_group\_member.list** into the search box and select **Enter**.

2.  Find the member record you want to remove from the identity group.

3.  Select the member record.

4.  Select **Delete**.

5.  Confirm the deletion when prompted.


## What to do next

The member no longer has access to secrets through this identity group. If the member needs access to different secrets, you can add them to a different identity group. See [Add members to an identity group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/usg-add-members-identity-group.md).

**Parent Topic:**[Configuring Unified Secrets Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/usg-configuring.md)

