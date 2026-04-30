---
title: Configure access to the compose email feature
description: Configure the role required to access the compose email feature that enables you to send emails directly from a supplier case or supplier task in the Source-to-Pay Workspace.
locale: en-US
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Composing emails with predefined content from the Source-to-Pay Workspace, Using Source-to-Pay Workspace, Using Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Configure access to the compose email feature

Configure the role required to access the compose email feature that enables you to send emails directly from a supplier case or supplier task in the Source-to-Pay Workspace.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **UI Properties**.

2.  In the **Roles that can view email in the Activity formatter when including "Sent/Received Emails"** property field, enter `itil, sn_slm.fulfiller`.

    This property contains the `itil` role by default. Add the `sn_slm.fulfiller` role name after the `itil` role, separated by a comma.

3.  Select **Save**.


**Parent Topic:**[Composing emails with predefined content from the Source-to-Pay Workspace](../concept/email-composer-slm-workspace.md)

