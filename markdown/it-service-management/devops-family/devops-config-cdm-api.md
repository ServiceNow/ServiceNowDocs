---
title: APIs and DevOps Config
description: You can use DevOps Config and CDM APIs to access your config data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/devops-family/devops-config-cdm-api.html
release: zurich
product: DevOps \(Family\)
classification: devops-family
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [DevOps Config reference, DevOps Config, IT Service Management]
---

# APIs and DevOps Config

You can use DevOps Config and CDM APIs to access your config data.

**Important:** Starting with the Washington D.C. release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

## DevOps Config

-   ****

    Manage your application lifecycle, using delete, get, patch, and post operations.


## CDM

-   **CdmApplicationsApi**

    Upload configuration data to the component, collection, deployable, and component variable folders found in the DevOps Config Workspace UI. Export deployable configuration data to your DevOps pipeline and manage shared components and shared applications.

-   **CdmChangesetsApi**

    Manage your changesets, including:

    -   Create new changesets.
    -   Deploy changesets.
    -   Retrieve lists of or individual changesets.
    -   Retrieve node changes within a changeset.
    -   Retrieve a list of applications or deployables impacted by a changeset.
    -   Delete changesets.
    -   Return a list of shared components associated with a specified changeset.
-   **CdmEditorApi**

    Create nodes, update nodes, include existing nodes under other nodes, delete nodes, and retrieve nodes and node includes.

-   **CdmPoliciesApi**

    Manage policy mappings of deployables in CDM. Policies that are properly mapped to a deployable are executed when a snapshot of the deployable is validated.

-   ****

    Create and manage shared libraries and shared components. Upload and export the configuration data of a shared component.

-   **CdmSnapshotApi**

    Publish, unpublish, and revalidate snapshots in CDM.

-   ****

    Publish, unpublish, and export versions \(snapshots\) in CDM for shared components under shared libraries.


**Parent Topic:**[DevOps Config reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-family/devops-config-reference.md)

