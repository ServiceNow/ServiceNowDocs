---
title: Manually override edition value in Software Asset Management classic
description: When the edition of a software install is not automatically discovered, you can specify the edition on the Software Installation form with the correct value \(if known\) so the software can be successfully reconciled.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [View normalization suggestions in Software Asset Management classic, Using Software Asset Management classic, Software Asset Management, IT Asset Management]
---

# Manually override edition value in Software Asset Management classic

When the edition of a software install is not automatically discovered, you can specify the edition on the Software Installation form with the correct value \(if known\) so the software can be successfully reconciled.

## Before you begin

Role required: sam\_admin

## About this task

For reconciliation to run successfully, the publisher, product, version, and edition fields of the software must be set. When the edition is not discovered automatically \(edition value is not included as part of the **Display name** field\) but you know the edition, you can manually set it to the correct value \(`Enterprise`, for example\).

Once the edition value is set, the discovery model for the software install is automatically reset. If the appropriate discovery model does not exist, a new one is created.

**Note:** Not all software products consist of an edition. Of the software products consisting of an edition, not all edition values are automatically discoverable.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Discovery** &gt; **Software Installations** and open the software installation record for which to set the edition value.

2.  Fill in the **Edition override** field, as appropriate.

    **Note:** The **Edition override** field is a free-form field \(no lookup list\) therefore, since this field is used as a key, the value entered must be exact.

3.  Select **Update**.

    The software installation is associated to different discovery model containing the edition value as part of the primary key. If the appropriate discovery model does not exist, a new one is created.


**Parent Topic:**[View normalization suggestions in Software Asset Management classic](view-norm-suggestions-sam.md)

