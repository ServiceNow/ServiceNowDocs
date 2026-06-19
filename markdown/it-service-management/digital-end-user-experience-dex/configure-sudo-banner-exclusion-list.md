---
title: Configure sudo banner exclusion list
description: Add the appropriate commands to the sudo banner exclusion list so the system doesn't flag it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/configure-sudo-banner-exclusion-list.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-03-30"
reading_time_minutes: 1
breadcrumb: [Sudo banner validation, Advanced configuration, Configure, Digital End-User Experience, IT Service Management]
---

# Configure sudo banner exclusion list

Add the appropriate commands to the sudo banner exclusion list so the system doesn't flag it.

## Before you begin

Role required: admin

## Procedure

1.  From your ServiceNow instance, navigate to **All** &gt; **All properties**.

2.  In the System Properties table, select the sn\_dex.sudo\_banner\_excluded\_fields property.

3.  Add the command you want to exclude in the **Value** field.

    You can find the list of available commands in the property description.

    You can add several commands, separated by a comma.

4.  Select **Save**.

    **Note:** The following two commands apply to Windows only: `Agent User` and `IsLocalSystem`.


**Parent Topic:**[Sudo banner validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/sudo-banner-validation.md)

