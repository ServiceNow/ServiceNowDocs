---
title: Create consumer grants
description: Create consumer grants to specify which identity groups can access which alias groups.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/usg-create-consumer-grants.html
release: brazil
topic_type: task
last_updated: "2026-09-18"
reading_time_minutes: 1
keywords: [consumer grants, access control configuration, unified secrets gateway]
breadcrumb: [Configuring Unified Secrets Gateway, Unified Secrets Gateway, Encryption]
---

# Create consumer grants

Create consumer grants to specify which identity groups can access which alias groups.

## Before you begin

Role required: admin or cryptographic\_manager

An alias group must already be created. See [Create an alias group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/usg-create-alias-group.md).

## Procedure

1.  Navigate to **All**, type `sys_secret_alias_consumer.list` into the search box and select Enter.

    **Note:** Two consumer grants are included in the base system: Default MID alias consumer and Outbound Security Alias Consumer.

2.  Select **New**.

3.  Complete the fields as shown in the following table.

    |Field|Description|
    |-----|-----------|
    |Alias Group|Select the alias group this consumer grant will apply to. This grant provides access only to secrets in the selected alias group.|
    |Consumer Type|Select identity\_group to grant access to a group of members or sys\_service to grant access to a specific service.|
    |Consumer Location|Select external for external callers \(such as MID Servers\) or glide for platform-internal access.|

4.  Select **Submit**.


## What to do next

If you created a custom identity group and have not yet added members to it, add members to complete your configuration. See [Add members to an identity group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/usg-add-members-identity-group.md).

**Parent Topic:**[Configuring Unified Secrets Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/usg-configuring.md)

