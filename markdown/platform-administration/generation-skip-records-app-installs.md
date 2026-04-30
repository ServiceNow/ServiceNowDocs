---
title: Skipped records that occur during application installation
description: Some records may be skipped when you make local updates to global or scoped applications. Skipped records can occur either when you modify the metadata records in the instance to which you're deploying or when you apply an update set. Depending on the deployment model you use and the state of applicable properties, you may risk "skipped records," which are generated in the sys\_upgrade\_history\_log. Learn what to expect on your instance when you upgrade an application using various different methods.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Installation considerations, Use, Legacy Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Skipped records that occur during application installation

Some records may be skipped when you make local updates to global or scoped applications. Skipped records can occur either when you modify the metadata records in the instance to which you're deploying or when you apply an update set. Depending on the deployment model you use and the state of applicable properties, you may risk "skipped records," which are generated in the sys\_upgrade\_history\_log. Learn what to expect on your instance when you upgrade an application using various different methods.

## General use cases

Under most circumstances, these general use cases occur during application installation:

<table id="table_fmj_n2w_rnb"><thead><tr><th>

Deployment type

</th><th>

Application type

</th><th>

Expected outcome

</th></tr></thead><tbody><tr><td>

Source Control

</td><td>

Scoped

</td><td>

No skips, application loads from Source Control. If local update xml exists, you are prompted to stash those changes.

</td></tr><tr><td>

Source Control

</td><td>

Global

</td><td>

No skips, application loads from Source Control. If local update xml exists, you are prompted to stash those changes.

</td></tr><tr><td>

App Repository

</td><td>

Scoped

</td><td>

Skipped records are generated and customizations preserved.

</td></tr><tr><td>

App Repository

</td><td>

Global

</td><td>

Application changes applied and skipped records are generated only when a superior claim is found.

 For details, see [Review skipped records using related lists](../../../administer/upgrade-center/task/uc-access-rl.md#).

</td></tr><tr><td>

Store

</td><td>

Scoped

</td><td>

Skipped records are generated, customization changes applied.

</td></tr><tr><td>

Source Control

</td><td>

Customization

</td><td>

No skips, customization loads from Source Control. If local update xml exists, you are prompted to stash those changes.

</td></tr><tr><td>

App Repository

</td><td>

Customization

</td><td>

No skipped records are generated, customization changes applied.

</td></tr><tr><td>

Store/App Repository

</td><td>

Scoped and Customization

</td><td>

No skipped records are generated unless the customization updates the base application record. In this case, a log entry of a skipped update for the base application is created.

</td></tr></tbody>
</table>## Author Elective Updates

It's important to understand the purpose of the **author\_elective\_update** folder.

When ServiceNow packages your application for the repository or for committing to Source Control, additional elements \(which might have been previously ignored\), are unloaded to the **author\_elective\_update** folder. \(These deleted elements are often referred to simply as "deletes."\) When your application is installed on your own instance, the deleted files are automatically loaded from the **author\_elective\_update** folder.

For example, if you changed the schema of your application by deleting a table or a column, those files are tracked in the folder but are not applied by default. There are specific rules that apply to author elective updates that you can change, based on the properties you can set. This folder contains metadata deleted files, including schema changes, and choice set unloads that you can apply or ignore. Whether you apply or ignore them, and whether corresponding skipped records are generated, depends on the state of the following properties and processing flow:

|Property name|Behavior|Default|Used in Source Control|
|-------------|--------|-------|----------------------|
|com.glide.apps.include\_only\_sys\_choice|Loads only deleted elements and updates to sys\_choice fields from author\_elective\_update|False|No|
|com.glide.apps.include\_my\_schema|Loads only deleted elements to schema files from author\_elective\_update. Applies to customer application installations and not third-party apps.|False|No|
|com.glide.apps.force\_skips|Creates skipped records for all of author\_elective\_update|False|No|
|com.glide.apps.include\_my\_deletes|Process author\_elective\_update|False|Yes|
|com.glide.apps.include\_global\_deletes|Process author\_elective\_update for global applications|False|Yes|

**Note:**

When there is no property for com.glide.apps.include\_my\_schema, it defaults to False. However, since the Orlando release, new instances have a default entry in the table to set it as True.

![Flow chart](../image/skipped-records-flowchart.png)

## Claims

Claims apply to global applications and application-customizations. In global applications, claims allow the system to choose a record deterministically should the same file be included in multiple applications. If you see a superior claim, an upgrade history log for the skipped record is created to identify a conflicting claim status. For details, see [Review skipped records using related lists](../../../administer/upgrade-center/task/uc-access-rl.md#).

**Parent Topic:**[Installation considerations](../concept/install-considerations.md)

