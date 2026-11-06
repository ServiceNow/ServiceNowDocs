---
title: Configure sudo banner exclusion list
description: Add the appropriate commands to the sudo banner exclusion list so the system doesn't flag them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/configure-sudo-banner-exclusion-list.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [sudo banner, sudo banner exclusion list, exclude sudo commands, system properties]
breadcrumb: [Sudo banner validation, DEX advanced configuration, Configure, Digital End-User Experience, IT Operations Management]
---

# Configure sudo banner exclusion list

Add the appropriate commands to the sudo banner exclusion list so the system doesn't flag them.

## Before you begin

Role required: admin

## Procedure

1.  From your ServiceNow instance, navigate to **All** &gt; **All properties**.

2.  In the System Properties table, select the **sn\_dex.sudo\_banner\_excluded\_fields** property.

3.  Add the command to exclude in the **Value** field.

    You can find the list of available commands in the property description.

    You can add several commands, separated by a comma.

4.  Select **Save**.

    **Note:** The following two commands apply to Windows only: `Agent User` and `IsLocalSystem`.


**Parent Topic:**[Sudo banner validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/sudo-banner-validation.md)

