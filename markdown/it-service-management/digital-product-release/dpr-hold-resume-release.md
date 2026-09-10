---
title: Put a release on hold
description: Mark a release on hold when work must pause temporarily, and resume or cancel it later from the same menu.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-product-release/dpr-hold-resume-release.html
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2026-08-07"
reading_time_minutes: 1
keywords: [Mark on hold, Hold reason, Resume release, On Hold state]
breadcrumb: [Manage releases for digital products and services, Use, Digital Product Release, IT Service Management]
---

# Put a release on hold

Mark a release on hold when work must pause temporarily, and resume or cancel it later from the same menu.

## Before you begin

The release is in the **Pending** or **In Progress** state.

Role required: sn\_dpr\_model.release\_admin

## About this task

Put a release on hold when work must stop temporarily, for example while you wait on an external dependency or investigate an issue. While the release is on hold, a warning banner appears on the release pages, and the **Complete phase** action and automatic phase progression are blocked. Task updates, field edits, configuration item and change request association, running policies, and downstream integrations continue to work as usual. For more information about the On Hold state, see [Release states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-release-states.md).

**Important:** You're prompted to enter a hold reason when you mark a release on hold, even though the field isn't configured as mandatory at the record level.

## Procedure

1.  On the release page, select the release overflow menu \(\[Omitted image "dpr-icon-more-actions.png"\] Alt text: More actions button icon.\) and select **Mark on hold**.

2.  In the **Hold reason** field, enter the reason for putting the release on hold.

3.  Select **Mark on hold** to confirm.


## Result

-   The release state updates to **On Hold**, and a warning banner appears on the release pages. The banner remains until the release is resumed or cancelled and can't be dismissed.
-   The **Complete phase** action and automatic phase progression are blocked.
-   You can't add a product to the release while it's on hold.

## What to do next

While a release is on hold, you can resume it or cancel it from the same release overflow menu \(\[Omitted image "dpr-icon-more-actions.png"\] Alt text: More actions button icon.\).

1.  Select **Resume release** and confirm to return the release to the state it was in before it was put on hold \(**Pending** or **In Progress**\).
2.  Select **Cancel release** and confirm to cancel the release directly from the **On Hold** state.

**Parent Topic:**[Manage releases for digital products and services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-manage-releases.md)

