---
title: Publish or unpublish a snapshot
description: Publish a snapshot so that it can be exported to enable the CI/CD pipeline to access and use the config data. Exporters can execute only on published snapshots.
locale: en-US
release: zurich
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [View snapshots, Use, DevOps Config, IT Service Management]
---

# Publish or unpublish a snapshot

Publish a snapshot so that it can be exported to enable the CI/CD pipeline to access and use the config data. Exporters can execute only on published snapshots.

## Before you begin

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

Role required: CDM Editor \[sn\_cdm.cdm\_editor\] or CDM Admin \[sn\_cdm.cdm\_admin\]

## About this task

-   You publish a snapshot when you feel that the deployable that it represents is ready to export to the pipeline.
-   While defining or updating a deployable, you can specify that only validated snapshots can be published.
-   A deployable must be connected to a service to publish its snapshots.
-   If a published deployable is disconnected from services, then you can perform the following actions, but cannot publish snapshots of the deployable until it is connected to a service:
    -   Edit config data.
    -   Create snapshots.
    -   Validate snapshots.
    -   Fix validation errors.

**Tip:** You can add a text description of a snapshot or rename it on the **Details** tab for the snapshot.

-   When exporters look for the latest snapshot, they should look for the latest `created` snapshot that is published.
-   The published\_date is the data at which the publish happens.
-   The unpublish snapshot action removes the publish flag and removes the published\_date value.

## Procedure

1.  Use either of the following methods to publish a snapshot:

    -   On any tab for an open snapshot, select **Publish**.
    -   On the **Version** tab for an application, select **Publish** from the **Actions** menu for the snapshot.
    ![Snapshots tab for a mature application](../image/cdm-snapshots-tab.png)

2.  View info

<table id="table_zpb_vyg_rpb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Changeset number

</td><td>

The system auto-assigns the changeset number. The system uses the number as the default changeset name.

</td></tr><tr><td>

Changeset name / Description

</td><td>

The system uses the changeset number as the default changeset name. Update the fields to help other users by changing to a more user-friendly name or by associating descriptive information with the changeset.

</td></tr><tr><td>

Deployable

</td><td>

Deployable on which the snapshot is based.

</td></tr><tr><td>

Validation status

</td><td>

-   Not validated: No policy has been executed against the snapshot.
-   Passed: The snapshot has passed all policy executions.
-   Failed: The snapshot has failed one or more policy executions.
-   In progress: Policies are currently executing.
-   Execution error: A policy failed to execute to completion.


</td></tr><tr><td>

Created / Created by

</td><td>

User that created the changeset and timestamp\` of creation.

</td></tr><tr><td>

Published on

</td><td>

Timestamp when the snapshot was published.

</td></tr></tbody>
</table>3.  Use either of the following methods to unpublish a snapshot:

    -   On any tab for an open snapshot, select **Unpublish**.
    -   On the **Version** tab for an application, select **Unpublish** from the **Actions** menu for the snapshot.

