---
title: Delete a deployable
description: Delete a deployable to delete its config data and all associated snapshots.
locale: en-US
release: xanadu
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create and update a deployable, Configure, DevOps Config, IT Service Management]
---

# Delete a deployable

Delete a deployable to delete its config data and all associated snapshots.

## Before you begin

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

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

