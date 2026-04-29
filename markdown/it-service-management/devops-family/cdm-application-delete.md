---
title: Delete a CDM application
description: Delete a CDM application to delete all associated config data and snapshots.
locale: en-US
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Changesets and version control in CDM, Using DevOps Config, DevOps Config, IT Service Management]
---

# Delete a CDM application

Delete a CDM application to delete all associated config data and snapshots.

## Before you begin

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

Role required: CDM Admin \[sn\_cdm.cdm\_admin\]

## Procedure

1.  Select the **Applications** icon \(![Applications icon](../image/icon-applications-nav.png)\) and then select one or more applications.

2.  Select **Delete** and then confirm the delete action.


## Result

The system performs the following operations when you delete an application:

-   Change the state of the application to "Deleted".
-   Disconnect the application from its associated SDLC component.
-   Disconnect deployables from CMDB services.
-   Return an error for any attempt to query associated snapshots.

