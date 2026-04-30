---
title: Types of landing pages in Service Operations Workspace for ITSM
description: Landing pages provide an agent with quick visibility into the work assigned, announcements, upcoming tasks, and so on.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Access controls in Service Operations Workspace for ITSM, Getting started with Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Types of landing pages in Service Operations Workspace for ITSM

Landing pages provide an agent with quick visibility into the work assigned, announcements, upcoming tasks, and so on.

Following landing pages are available by default for the Service Operations Workspace ITSM Applications \(sn\_sow\_itsm\_cont\) application.

-   Tier 1 landing page
-   Tier 2 landing page

Other landing pages are available if you have the corresponding plugins installed, for example, Service Operations Workspace ITOM Apps \(sn\_sow\_itom\_cont\).

**Important:**

-   A user's access to the landing page is based on the audience associated with that page. Configure the audiences with the required service desk groups and the users that are part of these service desk groups can then access the landing page. For information about audiences, see [Learn about audiences](https://www.servicenow.com/docs/access?context=add-audiences&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).
-   When multiple audiences are available for the landing page, the audience with the least order is considered.

## Criteria to access the tier 1 landing page

Any user that meets one of the following audience criteria is redirected by default to the tier 1 landing page.

|Audience|Role|User criteria inclusion|
|--------|----|-----------------------|
|SOW Common Audience|admin|None|
|SOW Service Desk Audience Granular|sn\_incident\_write|User should belong to a user group included in the **Service Desk Group Inclusion** user criteria inclusion of the audience.|
|SOW Service Desk Audience|itil|User should belong to a user group included in the **Service Desk Group Inclusion** user criteria inclusion of the audience.|

## Criteria to access the tier 2 landing page

Any user that meets the following audience criteria is redirected by default to the tier 2 landing page.

|Audience|Role|User criteria inclusion|
|--------|----|-----------------------|
|SOW Tier 2/3 landing page Audience|itil|None|

**Parent Topic:**[Access controls in Service Operations Workspace for ITSM](access-controls-sow-itsm.md)

