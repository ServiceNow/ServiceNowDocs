---
title: Associating change requests with releases in Service Operations Workspace
description: The integration between Service Operations Workspace \(SOW\) and Digital Product Release \(DPR\) workspaces provide a unified release and change management experience. You can associate releases with change requests across both workspaces.
locale: en-US
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [SOW integration, Statement of Work, change request integration, workspace integration, interoperable routes]
breadcrumb: [Explore, Digital Product Release, IT Service Management]
---

# Associating change requests with releases in Service Operations Workspace

The integration between Service Operations Workspace \(SOW\) and Digital Product Release \(DPR\) workspaces provide a unified release and change management experience. You can associate releases with change requests across both workspaces.

## Overview of DPR and SOW unified experience

This seamless experience streamlines collaboration between Change and Release teams by providing a unified view of release activities and associated changes.

-   Manage change requests associated with releases.
-   Import affected configuration items \(CIs\) from releases into changes.
-   View release details in the SOW workspace.

For more information, see [Service Operations Workspace for ITSM](../../service-operations-workspace/concept/sow-landing-page.md).

## Prerequisites

Verify the following before you begin:

-   Both DPR \(v2.4 or later\) and SOW \(v9.0.0 or later\) applications are activated in your ServiceNow AI Platform instance.
-   You have the required roles for both applications.

## Embedded release details in Change form in Service Operations Workspace

The **Related release** card on the contextual side panel displays release information for a change request directly within the Change form in Service Operations Workspace.

If a change isn’t associated with a release, the card displays an **Assign** button, which you can use to associate the change with a release.

If a change is associated with a release, the card displays the following key details:

-   Release owner
-   Release readiness target date and release date
-   Current phase
-   Release phase to which the change is attached \(if attached to more than one phase, a count displays — select it to view all attached phases\)
-   Policy status
-   Release state

To open the release execution page, select the release name link.

For more information, see [Create a change request in Service Operations Workspace](../../service-operations-workspace/task/create-change-sow.md#step-create-CR-link-release).

## Affected CIs import

You can import affected configuration items \(CIs\) from release phases directly into change requests, streamlining the change management process.

For large CI sets, the import process runs asynchronously. Manually refresh the list if the imported CIs don’t appear immediately.

For more information, see [Create a change request in Service Operations Workspace](../../service-operations-workspace/task/create-change-sow.md#step-create-CR-add-cis-rls).

**Parent Topic:**[Exploring Digital Product Release](dpr-exploring-digital-product-release.md)

**Related topics**  


[Manage change requests in a release](../task/dpr-work-release-change-request.md)

[Change Management in Service Operations Workspace](../../service-operations-workspace/concept/change-sow.md)

