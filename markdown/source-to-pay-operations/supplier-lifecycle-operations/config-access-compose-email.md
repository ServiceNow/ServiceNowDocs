---
title: Configure access to the compose email feature
description: Configure the role required to access the compose email feature that enables you to send emails directly from a supplier case or supplier task in the Source-to-Pay Workspace.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Composing emails with predefined content, Using Source-to-Pay Workspace, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Configure access to the compose email feature

Configure the role required to access the compose email feature that enables you to send emails directly from a supplier case or supplier task in the Source-to-Pay Workspace.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **UI Properties**.

2.  In the **Roles that can view email in the Activity formatter when including "Sent/Received Emails"** property field, enter `itil, sn_slm.fulfiller`.![Added required roles in the Roles that can view email in the Activity formatter when including Sent/Received Emails field](../image/configure-access-compose-email-feature.png)

    This property contains the `itil` role by default. Add the `sn_slm.fulfiller` role name after the `itil` role, separated by a comma.

3.  Select **Save**.


## Result

The role required to access the compose email feature is configured.

**Parent Topic:**[Composing emails with predefined content from the Source-to-Pay Workspace](../concept/email-composer-slm-workspace.md)

**Related topics**  


[Composing emails with predefined content from the Source-to-Pay Workspace](../concept/email-composer-slm-workspace.md)

[Communicate using emails from the Source-to-Pay Workspace](send-emails-slm-ws.md)

