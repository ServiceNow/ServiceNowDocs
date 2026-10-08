---
title: Create an identity group
description: Create a custom identity group to manage access for a specific set of members.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/usg-create-identity-group.html
release: brazil
topic_type: task
last_updated: "2026-09-18"
reading_time_minutes: 1
keywords: [identity groups, member grouping, unified secrets gateway]
breadcrumb: [Configuring Unified Secrets Gateway, Unified Secrets Gateway, Encryption]
---

# Create an identity group

Create a custom identity group to manage access for a specific set of members.

## Before you begin

Role required: admin or cryptographic\_manager

**Note:** The system-managed mid-all identity group is automatically available for all MID Servers. Create a custom identity group only if you want to restrict access to a specific subset of members.

## Procedure

1.  Navigate to **All**, type **sys\_secret\_identity\_group.list** into the search box and select **Enter**.

    **Note:** The identity group that is included in the base system is mid-all.

2.  Select **New**.

3.  Fill out the fields as shown in the following table.

    |Field|Value|
    |-----|-----|
    |Name|Enter a descriptive name for this identity group. Example: prod-mid-servers or integration-services|
    |Managed By|Select manual if you're manually adding members to this group, or system if the group is automatically populated by USG.|

4.  Select **Submit**.


## What to do next

Create consumer grants to link your identity group to the alias group you created. See [Create consumer grants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/usg-create-consumer-grants.md).

**Parent Topic:**[Configuring Unified Secrets Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/usg-configuring.md)

