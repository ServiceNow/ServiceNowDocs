---
title: Delete an architectural artifact version
description: Delete an architectural artifact version that is in Draft state from the Enterprise Architecture Workspace.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-04-21"
reading_time_minutes: 1
breadcrumb: [Manage architectural artifacts, Working with information portfolio, Portfolio list view, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Delete an architectural artifact version

Delete an architectural artifact version that is in **Draft** state from the Enterprise Architecture Workspace.

## Before you begin

Role required: sn\_apm.apm\_user

## Procedure

1.  Navigate to **Workspace** &gt; **Enterprise Architecture Workspace**.

2.  Open the Portfolio List view by selecting the Portfolio icon ![Portfolio icon](../../image/portfolio-icon.png).

3.  Select the expand row icon \(![Expand Row icon](../../image/ExpandIcon.png)\) next to **Information Portfolio**.

4.  Select **Architectural Artifacts**.

5.  Open the architectural artifact for which you want to delete an architectural artifact version.

6.  Delete the architectural artifact version.

    -   For architectural artifacts of type **URL** and **Attachment**:
        1.  Select **Artifact versions**.
        2.  Select the check box next to the architectural artifact version that you want to delete. You can only delete versions that are in **Draft** state.
        3.  Select **Delete**.

            A confirmation pop-up appears.

        4.  Select **Delete**.
    -   For architectural artifacts of type **Architectural Decision Record**:
        1.  Select the version of ADR that you want to delete and that has status **Draft**.

            ![ADR artifact content page with version drop-down highlighted.](../../image/eaw-image/adr-version-dropdown.png)

        2.  Select the delete version icon \(![](../../image/icon-three-dot-menu-eaw.png)\) and then select **Delete version**.

            ![ADR artifact content page with the Delete version button highlighted.](../../image/eaw-image/adr-delete-version-button.png)

            A confirmation pop-up appears.

        3.  Select **Delete**.

## Result

The record version is deleted. On deleting a particular version of an architectural artifact, the details of the previous version of the architectural artifact are displayed by default.

**Parent Topic:**[Manage architectural artifacts](../../concept/eaw-concept/eaw-managing-architectural-artifacts.md)

