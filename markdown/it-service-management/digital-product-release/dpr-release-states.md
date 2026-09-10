---
title: Release states
description: A release moves through a defined set of states, from creation to closure. The On Hold state lets you pause a release temporarily without losing task, policy, or association data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-product-release/dpr-release-states.html
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: concept
last_updated: "2026-08-07"
reading_time_minutes: 2
keywords: [Release states, On Hold state, Release state model, Hold reason]
breadcrumb: [Release for a product or service, Explore, Digital Product Release, IT Service Management]
---

# Release states

A release moves through a defined set of states, from creation to closure. The On Hold state lets you pause a release temporarily without losing task, policy, or association data.

In Digital Product Release \(DPR\), every release has a state that reflects its position in the release lifecycle. The release state determines which actions are available and whether the release still requires setup, is actively being worked, or is paused, closed, or discontinued. For more information about the overall release process, see [Release for a product or service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-product-release.md).

## Release states

The following states apply to a release.

<table id="table_release-states"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Draft**

</td><td>

The release is missing required setup information, such as a release template or a release readiness target date. You can finish creating the release from the **Release Planning** page or the **Releases** list.

</td></tr><tr><td>

**Pending**

</td><td>

The release is fully set up and scheduled to start. A scheduled job moves the release to the **In Progress** state automatically when its planned start date arrives.

</td></tr><tr><td>

**In Progress**

</td><td>

The release is actively moving through its phases. Tasks, policies, and approvals for the current phase are underway.

</td></tr><tr><td>

**On Hold**

</td><td>

Work on the release is temporarily paused. A warning banner appears on the release pages, and the **Complete phase** action and automatic phase progression are blocked until the release is resumed. However, other release activities, including task updates, field edits, configuration item and change request association, and running policies continue to work normally.For more information, see [Put a release on hold](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-hold-resume-release.md).

</td></tr><tr><td>

**Review**

</td><td>

All phases are completed and the release awaits final review before it's marked complete. A release can move to the **Review** state automatically when the **sn\_dpr.auto\_transition\_release\_to\_review** property is enabled.

</td></tr><tr><td>

**Completed**

</td><td>

The release is closed. All release work is finished and the phases mapped to it are compliant with their policies.For more information, see [Close a release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-complete-release.md).

</td></tr><tr><td>

**Cancelled**

</td><td>

The release is discontinued and no further work occurs.

</td></tr></tbody>
</table>**Parent Topic:**[Release for a product or service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-product-release.md)

**Related topics**  


[Manage releases for digital products and services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-manage-releases.md)

