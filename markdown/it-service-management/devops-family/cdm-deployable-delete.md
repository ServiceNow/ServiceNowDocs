---
title: Delete a deployable
description: Delete a deployable to delete its config data and all associated snapshots.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/devops-family/cdm-deployable-delete.html
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create and update a deployable, Configuring DevOps Config, DevOps Config, IT Service Management]
---

# Delete a deployable

Delete a deployable to delete its config data and all associated snapshots.

## Before you begin

**Important:** Starting with the Washington D.C. release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

Role required: CDM Admin \[sn\_cdm.cdm\_admin\]

## About this task

**Note:** When you delete a deployable, existing snapshots cannot be exported or validated and cannot be referred to in exporters or policies.

## Procedure

1.  For an open application, select the **Settings** tab.

2.  Select **Deployables** to view the list of deployables for the application.

3.  Select one or more deployables and select **Delete**.

    -   The deployables no longer appear in any list.
    -   All config data in the deployables is deleted.
    -   All existing snapshots are deleted.
    -   You can create a new deployable with the same name as a deleted deployable.

