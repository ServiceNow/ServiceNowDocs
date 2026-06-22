---
title: Manage configuration items in a release
description: View and manage the configuration items \(CIs\) in a release phase. Use the associated CIs to manage change requests and tasks in the release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-product-release/dpr-work-release-config-items.html
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2026-05-11"
reading_time_minutes: 1
breadcrumb: [Manage releases for digital products and services, Use, Digital Product Release, IT Service Management]
---

# Manage configuration items in a release

View and manage the configuration items \(CIs\) in a release phase. Use the associated CIs to manage change requests and tasks in the release.

## Before you begin

Role required: sn\_dpr\_model.product\_manager, sn\_dpr\_model.release\_coordinator, or sn\_dpr\_model.release\_admin

## About this task

You can add a specific configuration item to a phase only once, although it can be added to multiple phases in the release.

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the releases icon \(\[Omitted image "dpr-icon-release.png"\] Alt text: Releases icon.\).

3.  Select a release from the list to open.

4.  Select **Configuration items**.

    The list displays all CIs that are associated with the selected phase.

5.  Select a phase from the **Phase** list to add or remove configuration items.

<table id="choicetable_l2q_vl2_52c"><thead><tr><th align="left" id="d76249e110">

Option

</th><th align="left" id="d76249e113">

Steps

</th></tr></thead><tbody><tr><td id="d76249e119">

**Add existing CIs to the release phase**

</td><td>

1.  Select **Add**.

When product-level release settings are configured, only the configuration items of CI classes defined in the release settings are available for selection. If no CI classes are configured in the product settings, all CI classes are available. For more information, see [Configure product-level release settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-config-product-release-setting.md).

Additionally, CIs are filtered by lifecycle stage or operational status based on the value defined in the `sn_dpr.ci_default_query` system property. To control which CIs are available for selection, modify this property. For more information, see [Digital Product Release properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/digital-product-release-properties.md).

2.  Select the CIs to add to the phase.
3.  Select **Add**.
 The selected configuration items are added to the phase.

</td></tr><tr><td id="d76249e173">

**Remove associated CIs from a phase**

</td><td>

1.  Select configuration items form the list to remove from the phase.
2.  Select **Remove**.


</td></tr></tbody>
</table>
**Parent Topic:**[Manage releases for digital products and services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-manage-releases.md)

