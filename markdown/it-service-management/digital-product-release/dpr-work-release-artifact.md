---
title: Manage artifacts in a release
description: Add or remove artifacts from a release.
locale: en-US
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage releases for digital products and services, Use, Digital Product Release, IT Service Management]
---

# Manage artifacts in a release

Add or remove artifacts from a release.

## Before you begin

Make sure you have associated an artifact repository with the product. For more information, see [View and manage data from external tools](dpr-manage-product-ext-tool.md).

Role required: sn\_dpr\_model.product\_manager or sn\_dpr\_model.release\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the releases icon \(![Releases icon.](../image/dpr-icon-release.png)\).

3.  Select a release from the list to open.

4.  On the Release form header, select the number under the **Artifacts** label.

    The **Artifacts** label is available when you select **Overview**, **Release scope**, or **Change requests**.

    ![Number of artifacts listed on the Release form header.](../image/dpr-release-artifacts.png)

5.  On the Release Artifacts list view, add or remove artifacts.

<table id="choicetable_i3k_312_c1c"><thead><tr><th align="left" id="d454521e123">

Option

</th><th align="left" id="d454521e126">

Steps

</th></tr></thead><tbody><tr><td id="d454521e132">

**Add an artifact**

</td><td>

1.  Select **Add artifact**.
2.  On the Link artifact to release dialog box, select an artifact from the **Artifact** list.

By default, the latest version of the artifact is added.

3.  To choose a different version of the artifact, clear **Use latest version** and provide a version in **Semantic version**.

A valid semantic version has the format as major.minor.patch. For example, 5.4.2.

4.  Select **Confirm**.
 **Note:** An artifact can only be added to a release once.

</td></tr><tr><td id="d454521e178">

**Remove an artifact**

</td><td>

1.  Select an artifact from the list.
2.  Select **Delete**.


</td></tr></tbody>
</table>
**Parent Topic:**[Manage releases for digital products and services](dpr-manage-releases.md)

