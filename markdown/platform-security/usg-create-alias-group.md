---
title: Create an alias group
description: Create an alias group to organize secrets and define where they are stored in ServiceNow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/usg-create-alias-group.html
release: brazil
topic_type: task
last_updated: "2026-09-18"
reading_time_minutes: 1
keywords: [alias group creation, secrets management configuration, unified secrets gateway setup]
breadcrumb: [Configuring Unified Secrets Gateway, Unified Secrets Gateway, Encryption]
---

# Create an alias group

Create an alias group to organize secrets and define where they are stored in ServiceNow.

## Before you begin

Role required: admin or cryptographic\_manager

## Procedure

1.  Navigate to **All**, type **sys\_secret\_alias\_group.list** into the search box and select Enter.

    **Note:** Two alias groups are included in the base system: mid-creds and outbound-security.

2.  Select **New**.

3.  Fill out the fields as shown in the following table.

    |Field|Value|
    |-----|-----|
    |Alias Field|Select the field used to identify individual secrets within the target table. Example: name or hostname|
    |Filter Mode|Select none \(default\) for instance-level access or mid\_scoped to restrict access to MID Servers only.|
    |Target Table|Select the physical table containing the secrets you want to manage. Example: discovery\_credentials.|
    |Glide Access Policy|Select configurable \(default\) to permit configured access or lockdown to deny all access to this alias group.|
    |Alias Group Name|Enter a logical group name for your alias group. This name is used when retrieving secrets through the APIs. Example: prod\_db\_credentials|
    |Value Field|Select the field containing the secret value from the dropdown. The asterisk option \(\*\) returns the full credential object. Available options are dynamic based on the target table selected.|

4.  Select **Submit**.


## What to do next

Create an identity group to define which members should have access to the alias group. See [Create an identity group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/usg-create-identity-group.md).

**Parent Topic:**[Configuring Unified Secrets Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/usg-configuring.md)

