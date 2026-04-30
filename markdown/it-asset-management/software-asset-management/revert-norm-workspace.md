---
title: Revert normalization in the workspace
description: You can revert the normalization of discovery models in the Software Asset Workspace.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Revert normalization in the workspace

You can revert the normalization of discovery models in the Software Asset Workspace.

## Before you begin

Discovery models with a status of **Normalized**, **Partially Normalized**, or **Publisher Normalized** revert to the status of **Match Not Found**. Discovery models with a status of **Manually Normalized** and discovery models that have been normalized using pattern rules cannot be reverted.

Role required: sam\_admin or sam\_user

## Procedure

1.  Navigate to **All** &gt; **Software asset** &gt; **Software Asset Workspace** &gt; **License operations** &gt; **Discovery models**.

2.  Select a discovery model record.

3.  Select **Revert Normalization**.

    Once the revert normalization process is complete, fields are reset to their original values and any rules associated with the software discovery model are deactivated.


**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

