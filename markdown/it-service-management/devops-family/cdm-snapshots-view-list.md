---
title: View snapshots
description: View the snapshots of all deployables for an application on the Details tab for the application. The release pipeline can access only a snapshot that is the currently published version.
locale: en-US
release: zurich
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, DevOps Config, IT Service Management]
---

# View snapshots

View the snapshots of all deployables for an application on the **Details** tab for the application. The release pipeline can access only a snapshot that is the currently published version.

## Before you begin

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

Role required: cdm\_viewer

## Procedure

1.  Open an application and select the **Snapshots** tab.

    The tab lists all deployables that are associated with the application. Each deployable displays a short list of its snapshots. Select **Show all** to view the full list of snapshots.

<table id="table_x2g_tj3_cqb"><thead><tr><th>

Column name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the snapshot.

 When a snapshot is generated, the system uses the deployable name and the snapshot number to generate a default name \(for example, `deployableName_1`, `deployableName_2`\). You can edit the name.

 **Tip:** You can edit the name on the **Details** tab. Select the snapshot name to open the tab.

</td></tr><tr><td>

Description

</td><td>

Descriptive information that you supply to help other users. **Tip:** You can add a description on the **Details** tab. Select the snapshot name to open the tab.

</td></tr><tr><td>

Published

</td><td>

Boolean that indicates whether the snapshot is published. Only published snapshots can be exported.**Important:** By default, exporters use the most recently created published snapshot.

 While defining or updating a deployable, you can specify that only validated snapshots can be published. You can unupublish a snapshot. See [Publish or unpublish a snapshot](cdm-snapshot-publish.md).

</td></tr><tr><td>

Deployable

</td><td>

Deployable on which the snapshot is based.

</td></tr><tr><td>

Validation

</td><td>

Validation status:-   Not validated: This is the initial snapshot state where no policy has been executed against the snapshot.
-   Requested: The validation flow has started.
-   In progress: The validation flow is running and policies are currently executing.
-   Passed: The snapshot has passed all policies.
-   Failed: The snapshot has failed one or more policies.
-   Execution error: A policy failed to run to completiondue to an unexpected error, mostly when the [CdmPolicyUtil script include](../reference/cdm-about-cdmpolicyutil.md) is not used to provide warning and failure messages..


</td></tr><tr><td>

Last validated

</td><td>

Timestamp when the snapshot was validated last.

</td></tr><tr><td>

Created

</td><td>

Timestamp when the snapshot was created.

</td></tr><tr><td>

Created by

</td><td>

User who created the snapshot.

</td></tr><tr><td>

Changeset

</td><td>

Changeset containing the data of the snapshot. Select the icon to open the changeset.

</td></tr><tr><td>

Tags

</td><td>

Text tag that enables you to filter the snapshots in a list.

</td></tr></tbody>
</table>2.  Select the snapshot name to view its details and set values on the **Details** tab.


