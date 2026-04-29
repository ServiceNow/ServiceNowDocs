---
title: Managing releases in Service Operations Workspace
description: Service Operations Workspace \(SOW\) and Digital Product Release \(DPR\) workspaces provide a unified release and change management experience. You can manage releases, view release details, and associate change requests with releases — all from SOW.
locale: en-US
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [SOW integration, Statement of Work, change request integration, workspace integration, interoperable routes]
breadcrumb: [Explore, Digital Product Release, IT Service Management]
---

# Managing releases in Service Operations Workspace

Service Operations Workspace \(SOW\) and Digital Product Release \(DPR\) workspaces provide a unified release and change management experience. You can manage releases, view release details, and associate change requests with releases — all from SOW.

## Overview of DPR and SOW unified experience

This seamless experience streamlines collaboration between Change and Release teams by providing a unified view of release activities and associated changes.

-   View release details in SOW
-   Manage change requests associated with releases
-   Import affected configuration items \(CIs\) from release phases

For more information, see [Service Operations Workspace for ITSM](../../service-operations-workspace/concept/sow-landing-page.md).

## Prerequisites

Verify the following before you begin:

-   Both DPR \(v2.4 or later\) and SOW \(v9.0.0 or later\) applications are activated in your ServiceNow AI Platform instance.
-   You have the required roles for both applications.

## Viewing releases in Service Operations Workspace

You can access releases, execute them, and view release details directly from SOW, enabling Change teams to view release context without switching workspaces.

-   **Releases list in SOW**

    SOW includes a **Releases** list that provides direct access to your releases without switching to the Digital Product Release Workspace. The list includes the following filters:

    -   Open releases: Shows active and open releases
    -   My releases: Shows releases where you’re the owner or assigned user
    -   All releases: Shows all releases, including cancelled
    -   Release bundles: Shows release bundles, if any exist
    The following image shows the Releases list in SOW.

    ![Releases list in Service Operations Workspace.](../image/dpr-sow-workspace-rls-list.png "Releases list in SOW")

-   **Release execution in SOW**

    From the Releases list, open any release to view its details within SOW, including:

    -   Release phases and their status
    -   Tasks associated with each phase
    -   Policy compliance information
    -   Release relations

You can also perform release execution from SOW if you have the appropriate DPR roles.

**Parent Topic:**[Exploring Digital Product Release](dpr-exploring-digital-product-release.md)

