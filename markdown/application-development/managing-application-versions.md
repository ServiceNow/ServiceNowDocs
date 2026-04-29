---
title: Managing application versions
description: Semantic versioning \(Major.Minor.Patch\) is the standard approach for ServiceNow applications. Each time you publish from ServiceNow Studio, you assign a version number, which gives your team a clear audit trail of all changes.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Deployment, Getting Started guide for developers, Building applications]
---

# Managing application versions

Semantic versioning \(Major.Minor.Patch\) is the standard approach for ServiceNow applications. Each time you publish from ServiceNow Studio, you assign a version number, which gives your team a clear audit trail of all changes.

-   **Major version, such as 2.0.0**

    A major version represents breaking changes, schema modifications, or significant feature additions.

-   **Minor version, such as 2.2.0**

    A minor version represents new features or enhancements that are backward-compatible.

-   **Patch version, such as 2.2.1**

    A patch version represents bug fixes and hotfixes with no functionality changes.


When using source control, such as Git, version branches or tags align with published versions in the application repository. This provides a dual record: the Git repository holds the source of truth for code history, while the Application Repository holds the deployable packages. If you must deploy a hotfix while phase 2 development is in progress, then create a branch from your current production version tag, apply the fix, publish that branch as a patch version, and install it on production without disrupting ongoing development work.

**Parent Topic:**[Deployment](get-started-deployment.md)

