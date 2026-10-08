---
title: Add members to an identity group
description: Add existing members to an identity group to control which entities can access secrets through consumer grants.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/usg-add-members-identity-group.html
release: brazil
topic_type: task
last_updated: "2026-09-18"
reading_time_minutes: 1
keywords: [identity group members, member management, unified secrets gateway]
breadcrumb: [Configuring Unified Secrets Gateway, Unified Secrets Gateway, Encryption]
---

# Add members to an identity group

Add existing members to an identity group to control which entities can access secrets through consumer grants.

## Before you begin

An identity group must already be created. See [Create an identity group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/usg-create-identity-group.md).

Role required: admin or cryptographic\_manager

## Procedure

1.  Navigate to **All**, type **sys\_secret\_identity\_group\_member.list** into the search box and select **Enter**.

    **Note:** If existing MID Servers are configured, they are listed here.

2.  Select **New**.

3.  Complete the fields as shown in the following table.

    |Field|Value|
    |-----|-----|
    |Identity Group|Select the identity group to which you want to add members.|
    |Member Table|Select the table containing the members you want to add. Example: ecc\_agent for MID Servers.|
    |Member Record|Select the specific member record to add to the identity group. Example: a specific MID Server or service.|

4.  Select **Submit** to add the member.

5.  Repeat steps 2–4 to add additional members to the identity group.


## What to do next

The Unified Secrets Gateway configuration is complete. Use the APIs to retrieve secrets. See [Using Unified Secrets Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/usg-using.md).

**Parent Topic:**[Configuring Unified Secrets Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/usg-configuring.md)

