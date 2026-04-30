---
title: Skipped records that occur during application installation
description: Some records may be skipped when you make local updates to global or scoped applications. Skipped records can occur either when you modify the metadata records in the instance to which you're deploying or when you apply an update set. Depending on the deployment model you use and the state of applicable properties, you may risk "skipped records," which are generated in the sys\_upgrade\_history\_log. Learn what to expect on your instance when you upgrade an application using various different methods.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Installation considerations, Use, Legacy Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Skipped records that occur during application installation

Some records may be skipped when you make local updates to global or scoped applications. Skipped records can occur either when you modify the metadata records in the instance to which you're deploying or when you apply an update set. Depending on the deployment model you use and the state of applicable properties, you may risk "skipped records," which are generated in the sys\_upgrade\_history\_log. Learn what to expect on your instance when you upgrade an application using various different methods.

## General use cases

Under most circumstances, these general use cases occur during application installation:

|Deployment type|Application type|Expected outcome|
|---------------|----------------|----------------|
|Source Control|Scoped|No skips, application loads from Source Control. If local update xml exists, you are prompted to stash those changes.|
|Source Control|Global|No skips, application loads from Source Control. If local update xml exists, you are prompted to stash those changes.|
|App Repository|Scoped|Skipped records are generated and customizations preserved.|
|App Repository|Global|Application changes applied and skipped records are generated only when a superior claim is found. Refer to [Claim Outcomes to Review related list](../../../customer-support/concept/claim-outcomes-to-review-related-list.md) for more details.|
|Store|Scoped|Skipped records are generated, customization changes applied.|
|Source Control|Customization|No skips, customization loads from Source Control. If local update xml exists, you are prompted to stash those changes.|
|App Repository|Customization|No skipped records are generated, customization changes applied.|
|Store/App Repository|Scoped and Customization|No skipped records are generated unless the customization updates the base application record. In this case, a log entry of a skipped update for the base application is created.|

## Author Elective Updates

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

Claims apply to global applications and application-customizations. In global applications, claims allow the system to choose a record deterministically should the same file be included in multiple applications. If you see a superior claim, an upgrade history log for the skipped record is created to identify a conflicting claim status. See [Claim Outcomes to Review related list](../../../customer-support/concept/claim-outcomes-to-review-related-list.md) for details.

**Parent Topic:**[Installation considerations](../concept/install-considerations.md)

