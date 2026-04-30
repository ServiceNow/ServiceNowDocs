---
title: Syncing exception reasons
description: Exception reasons are automatically synchronized to the Production instance whenever they are created or updated, based on the instances specified in the My SN Instances table.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-11-18"
reading_time_minutes: 1
breadcrumb: [Exception reason integration, Scan Engine integrations, Scan Engine, Platform Health, Using Impact, Impact]
---

# Syncing exception reasons

Exception reasons are automatically synchronized to the Production instance whenever they are created or updated, based on the instances specified in the **My SN Instances** table.

If you selected **Enable approvals in production** on the **Exception reason** properties tab on the Production instance, then once the exception reason changes to the **Requested** state, approval requests trigger for the **Approval Group\(s\)** field. Once the exception reason is approved or rejected, the status syncs back to the Developer instance.

