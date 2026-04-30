---
title: Delete an asset profile in Security Posture Control
description: You can delete asset profiles. You delete asset profiles if they are associated to policies so the asset profile's conditions are not included in the next policy audit.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create an asset profile, Use the workspace, Security Posture Control, Security Operations]
---

# Delete an asset profile in Security Posture Control

You can delete asset profiles. You delete asset profiles if they are associated to policies so the asset profile's conditions are not included in the next policy audit.

## Before you begin

Roles required: SPC Admin Group or SPC Analyst Group

## Procedure

1.  Navigate to **All** &gt; **Security Posture Control Workspace** &gt; **Asset profiles**.

2.  Select a profile record.

3.  Select the more actions menu icon \(![More actions menu icon](../../secops-analyst-workspace/image/more-actions-icon.png)\) and select **Delete asset profile**.

4.  In the dialog select **Review policies** to view any policies this profile is linked to.

    Policies that contain the asset profile are listed in the Linked policies tab.

5.  Select the tab with the asset profile that you want to delete.

6.  Select the more actions menu icon and select **Delete asset profile**.

    This is a hard delete. The conditions of the asset profile are removed from any policies and are not included in the next nightly policy audits to get the latest results.


