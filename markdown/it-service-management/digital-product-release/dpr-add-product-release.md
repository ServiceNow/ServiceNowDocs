---
title: Add a product to a multi-product release
description: Add a product to a multi-product release to expand the scope of the release as requirements evolve. The added product gets its own child release with phases, tasks, and policies aligned to the main release.
locale: en-US
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [add product to multi-product release, catalog request add product, Integration Hub add product]
breadcrumb: [Manage releases for digital products and services, Use, Digital Product Release, IT Service Management]
---

# Add a product to a multi-product release

Add a product to a multi-product release to expand the scope of the release as requirements evolve. The added product gets its own child release with phases, tasks, and policies aligned to the main release.

## Before you begin

The release must be in the Pending or In Progress state.

Role required: sn\_dpr\_model.release\_admin or sn\_dpr\_model.product\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the releases icon \(![Releases icon.](../image/dpr-icon-release.png)\).

3.  Select a release from the list to open.

4.  Select the **Products** tab and select **Add product**.

5.  In the **Product name** field, select a product you want to add.

    You can't add a product that already has an active release in this multi-product release. If a product was previously removed, you can add it again.

6.  In the **Version** field, provide the version of the selected product.

    You can select an existing version or enter a new version.

7.  Select **Add**.


## Result

A catalog request is submitted and auto-approved. The following actions occur:

-   A release is created for the included product with phases aligned to the main release.
-   Tasks and policies are created for each phase based on the release template.
-   The phase management in the release differs based on the release's current state:
    -   **Pending**: The product is added directly and its release is created.
    -   **In Progress**: The product is added and a release is created and started immediately. The system begins executing policies sequentially from the earliest phase to catch up to the main release's current phase. For more information, see [Phase management in a multi-product release](../concept/dpr-product-release.md#dpr-dl-multi-prod-phase-mgmt).

## Adding a product to an in-progress release

Consider a multi-product release with three products \(Product A, Product B, and Product C\) that has the following phases: Planning, Development, Testing, Pre-deployment, and Deployment. The release is in the Testing phase.

You add Product D to this release while it is in the Testing phase. When the product is added, the system executes phase policies sequentially for Product D, starting from the earliest phase:

1.  Planning phase policies are executed first.
2.  If Planning policies pass, Development phase policies are executed.
3.  This execution continues until Product D catches up to the current release phase \(Testing\) or until a phase fails.

If policies for any phase fail — for example, Development — Product D remains in the failed phase. The other products aren’t affected and remain in Testing.

|Product|Current phase|
|-------|-------------|
|Product A|Testing|
|Product B|Testing|
|Product C|Testing|
|Product D|Development \(failed\)|

In this case, the Testing phase can’t be closed until all products, including Product D, pass their policies and reach the Testing phase.

**Parent Topic:**[Manage releases for digital products and services](dpr-manage-releases.md)

