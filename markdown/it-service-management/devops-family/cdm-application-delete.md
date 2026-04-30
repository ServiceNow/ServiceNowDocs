---
title: Delete a CDM application
description: Delete a CDM application to delete all associated config data and snapshots.
locale: en-US
release: yokohama
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Changesets and version control in CDM, Use, DevOps Config, IT Service Management]
---

# Delete a CDM application

Delete a CDM application to delete all associated config data and snapshots.

## Before you begin

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

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

