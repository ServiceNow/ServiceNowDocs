---
title: Manage change requests in a release
description: View and manage change requests in a release. You can create and add new change requests to the release or add existing ones.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-product-release/dpr-work-release-change-request.html
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2026-08-31"
reading_time_minutes: 2
breadcrumb: [Manage releases for digital products and services, Use, Digital Product Release, IT Service Management]
---

# Manage change requests in a release

View and manage change requests in a release. You can create and add new change requests to the release or add existing ones.

## Before you begin

Role required: sn\_dpr\_model.product\_manager or sn\_dpr\_model.release\_admin

## About this task

You can associate a change request to a phase only once, although it can be added to multiple phases in the release.

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the releases icon \(\[Omitted image "dpr-icon-release.png"\] Alt text: Releases icon.\).

3.  Select a release from the list to open.

4.  Select **Change requests** to manage change requests in the release.

    The list displays all change requests that are associated with therelease.

5.  Add change requests to a phase by creating new ones or selecting existing ones, or remove change requests from a phase.

<table id="choicetable_l2q_vl2_52c"><thead><tr><th align="left" id="d406687e110">

Option

</th><th align="left" id="d406687e113">

Steps

</th></tr></thead><tbody><tr><td id="d406687e119">

**Create and add a change request to a phase**

</td><td>

1.  In the **Change requests** tab, select **New**.
2.  Select a Change request model.

When product-level release settings are configured for the product, only the change models and standard change templates defined in the settings are available for selection. If no change models are configured in the product settings, all available models are displayed. For more information, see [Configure product-level release settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-config-product-release-setting.md).

3.  Select **Next**
4.  Fill in the details in the Change Request form and select **Save**.

For a description of the field values, see [Create a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/t_CreateAChange.md).

 The new change request is created and added to the phase based on the **sn\_dpr.default\_phase\_for\_changes** system property. The **Software model** field in the change request is filled with the version of the release.

</td></tr><tr><td id="d406687e184">

**Add existing change requests to a phase**

</td><td>

1.  Select **Add**.

The list displays existing change requests, filtered by change models and standard change templates defined in the product-level release settings. If no change models are configured in the product settings, all change requests are listed.

2.  Select the change request to add to the release.
3.  Select **Add**.
 The selected change requests are added to the phase based on the **sn\_dpr.default\_phase\_for\_changes** system property. The **Software model** field in these change requests is filled with the version of the release.

</td></tr><tr><td id="d406687e225">

**Remove associated change requests from the release**

</td><td>

1.  Select change requests form the list that you want to dissociate from the release.
2.  Select **Remove**.
 The selected change requests are removed from the release. The **The Software model** field in these change requests is also cleared.

</td></tr></tbody>
</table>6.  Import the configuration items \(CIs\) from the attached phases into the change request as affected CIs.

    1.  Select the **Affected CIs** tab.
    2.  Selecting **Add CIs from release phases**.

## Result

-   If the change request is associated with a single phase, the **Attached to phases** in the header section of the Change Request record shows the name of that phase. Select the link to open the phase.
-   If the change request is associated with more than one phase of the release, the **Attached to phases** shows the count of those phases. Select the link to open the list of those phases.

**Parent Topic:**[Manage releases for digital products and services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-manage-releases.md)

