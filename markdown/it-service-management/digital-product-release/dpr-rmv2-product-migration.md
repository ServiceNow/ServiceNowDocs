---
title: Migrate data from Release Management v2 to Digital Product Release
description: If you have the Release Management v2 \(RM v2\) application installed, you can migrate your data from RM v2 to Digital Product Release.
locale: en-US
release: xanadu
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Digital Product Release, Digital Product Release, IT Service Management]
---

# Migrate data from Release Management v2 to Digital Product Release

If you have the Release Management v2 \(RM v2\) application installed, you can migrate your data from RM v2 to Digital Product Release.

## Before you begin

Role required: admin

To provide access to additional roles, you can add comma-separated values of other roles installed with DPR in the system property **sn\_dpr\_model.rmv2.migration\_roles**. For more information, see [Digital Product Release properties](../reference/digital-product-release-properties.md).

## About this task

The migration utility performs the following tasks:

-   Migrate RM v2 product to Digital product: Copies data from rm\_product into newly created Application Product Models.
-   Create Release Template from RM v2 Release: Creates a DPR Release Template by leveraging the Phases and Tasks from an existing RM v2 Release record.

For more information about migrating data from Release Management V2 to Digital Product Release, see the [RMV2 Product Migration \[KB1644412\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1644412) article in the Now Support Knowledge Base.

## Procedure

1.  Define your custom field mappings as needed.

2.  Add any additional post-processing instructions after the creation of the cmdb\_application\_product\_model record.

3.  Perform the migration either from the rm\_product list view or running the migration script from the sn\_dpr\_model app scope.


