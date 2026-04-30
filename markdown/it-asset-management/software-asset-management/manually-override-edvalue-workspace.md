---
title: Manually override edition value in workspace
description: If the edition of a software installation is not automatically discovered, you can specify the edition on the Software Installation form \(if known\) so the software can be successfully reconciled.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Manually override edition value in workspace

If the edition of a software installation is not automatically discovered, you can specify the edition on the Software Installation form \(if known\) so the software can be successfully reconciled.

## Before you begin

Role required: sam\_admin

## About this task

For reconciliation to run successfully, the publisher, product, version, and edition fields of the software must be set. When the edition is not discovered automatically \(edition value is not included as part of the **Display name** field\) but you know the edition, you can manually set it to the correct value \(for example `Enterprise`\).

Once the edition value is set, the discovery model for the software install is automatically reset. If the appropriate discovery model does not exist, a new one is created.

**Note:** Not all software products consist of an edition. Of the software products consisting of an edition, not all edition values are automatically discoverable.

## Procedure

1.  Navigate to **All** &gt; **Software asset** &gt; **Software Asset Workspace** &gt; **License operations**.

2.  Select **Discovery models**.

3.  In the Discovery models page, open a discovery model.

4.  Select the Software Installations tab and open the software installation record for which you want to set the edition value.

    **Note:** The **Edition override** field is a free-form field \(no lookup list\) and since this field is used as a key, the value entered must be exact.

5.  Select **Save**.

    The software installation is associated to a different discovery model containing the edition value as part of the primary key. If the appropriate discovery model does not exist, a new one is created.


**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

