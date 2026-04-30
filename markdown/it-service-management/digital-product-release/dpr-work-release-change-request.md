---
title: Manage change requests in a release
description: View and manage change requests in a release. You can create and add new change requests to the release or add existing ones.
locale: en-US
release: xanadu
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2025-07-22"
reading_time_minutes: 2
breadcrumb: [Manage releases for digital products and services, Using Digital Product Release, Digital Product Release, IT Service Management]
---

# Manage change requests in a release

View and manage change requests in a release. You can create and add new change requests to the release or add existing ones.

## Before you begin

Role required: sn\_dpr\_model.product\_manager or sn\_dpr\_model.release\_admin

## About this task

You can associate a change request to a phase only once, although it can be added to multiple phases in the release.

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the releases icon \(![Releases icon.](../image/dpr-icon-release.png)\).

3.  Select a release from the list to open.

4.  Select **Change requests** to manage change requests in the release.

    The Change requests list displays all change requests that are associated with the selected phase of the release.

5.  Select a phase from the **Phase** list.

6.  Create change requests and add them to the phase, add existing change requests to the phase, or remove the ones that are already associated with the phase.

<table id="choicetable_l2q_vl2_52c"><thead><tr><th align="left" id="d298277e113">

Option

</th><th align="left" id="d298277e116">

Steps

</th></tr></thead><tbody><tr><td id="d298277e122">

**Create and add a change request to the phase**

</td><td>

1.  In the **Change requests** tab, select **New**.
2.  Select a Change request model and then select **Next**.
3.  Fill in the details in the Change Request form and select **Save**.

For more information, see [Create a change request](../../change-management/task/t_CreateAChange.md).

 The new change request is created and added to theselected phase. The **Software model** field in the change request is filled with the version of the release.

</td></tr><tr><td id="d298277e173">

**Add existing change requests to the phase**

</td><td>

1.  Select **Add**.

All existing change requests that have the **Software model** field empty are listed.

2.  Select the change request to add to the release.
3.  Select **Add**.
 The selected change requests are added to theselected phase. The **Software model** field in these change requests is filled with the version of the release.

</td></tr><tr><td id="d298277e214">

**Remove associated change requests from the phase**

</td><td>

1.  Select change requests form the list that you want to dissociate from the release.
2.  Select **Remove**.
 The selected change requests are removed from theselected phase. **The Software model** field in these change requests is also cleared.

</td></tr></tbody>
</table>7.  Import the configuration items \(CIs\) from the attached phases into the change request as affected CIs.

    1.  Select the **Affected CIs** tab.
    2.  Selecting **Add CIs from release phases**.

## Result

-   If the change request is associated with a single phase, the **Attached to phases** in the header section of the Change Request record shows the name of that phase. Select the link to open the phase.
-   If the change request is associated with more than one phase of the release, the **Attached to phases** shows the count of those phases. Select the link to open the list of those phases.

**Parent Topic:**[Manage releases for digital products and services](dpr-manage-releases.md)

