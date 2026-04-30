---
title: Track multiple releases from a release bundle
description: Track the progress of releases in a release bundle concurrently to improve efficiency and streamline the release management process. You can also identify dependencies and potential conflicts in your releases and coordinate with team members working on different releases.
locale: en-US
release: yokohama
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2025-12-09"
reading_time_minutes: 2
breadcrumb: [Managing multiple releases through release bundles, Manage releases for digital products and services, Use, Digital Product Release, IT Service Management]
---

# Track multiple releases from a release bundle

Track the progress of releases in a release bundle concurrently to improve efficiency and streamline the release management process. You can also identify dependencies and potential conflicts in your releases and coordinate with team members working on different releases.

## Before you begin

Role required: sn\_dpr\_model.release\_coordinator, sn\_dpr\_model.product\_manager, or sn\_dpr\_model.release\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the releases icon \(![Releases icon.](../image/dpr-icon-release.png)\), and then select **Bundles**.

3.  Select a release bundle from the list to open.

4.  On the **Overview** tab, review key metrics for all releases in the bundle.

    |Widget|Description|
    |------|-----------|
    |Releases by state|Total number of releases in the bundle, grouped by their state.|
    |Tasks|Total number of tasks across all releases in the bundle, grouped by their state.|
    |Policies|Total number of policies across all releases in the bundle, grouped by their compliant status.|
    |Approvals|List of all approval tasks across all releases in the bundle, grouped by their approval status.|
    |Enhancements|Total number of product enhancements across all releases in the bundle, grouped by their state.|

5.  On the **Details** tab, view and edit the release bundle details.

    The **State** field shows the overall state of the release bundle, which is determined by the states of its releases, as mentioned below:

    -   Draft: When there are no releases in the bundle.
    -   Ready: When all releases are either in the Pending or Draft state.
    -   In Progress: When at least one release is in the In Progress, Review, or Restarting state, or when there's a combination of Draft and Completed states among the releases.
    -   Completed: When all releases have either the Completed or Cancelled state. For the Completed release bundle, the Active is set to false.
    **Note:**

6.  On the **Releases** tab, view and manage releases in the bundle.

    -   To add a release to the bundle, select **Add** and then select from the list of releases.
    -   To remove an existing release from the bundle, select the release from the list, and then select **Remove**.
    -   To view the details of a release, select the release name from the list.
7.  On the **Change requests** tab, view change requests across all releases in the bundle.

    To view the details of a change request, select it from the list.


**Parent Topic:**[Managing multiple releases through release bundles](../concept/dpr-release-bundle.md)

**Related topics**  


[Create a release bundle](dpr-create-release-bundle.md)

