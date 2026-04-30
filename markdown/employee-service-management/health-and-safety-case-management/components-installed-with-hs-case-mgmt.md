---
title: Components installed with Health and Safety Case Management
description: Several types of components are installed with installation of the Health and Safety Case Management application, including tables, user roles, and scheduled jobs. The application also installs related store applications if they aren’t already installed.
locale: en-US
release: zurich
product: Health and Safety Case Management
classification: health-and-safety-case-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Health and Safety Case Management, Health and Safety, Employee Service Management]
---

# Components installed with Health and Safety Case Management

Several types of components are installed with installation of the Health and Safety Case Management application, including tables, user roles, and scheduled jobs. The application also installs related store applications if they aren’t already installed.

## Store applications installed

<table><thead><tr><th>

Store application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Health and Safety Core

</td><td>

Installs core data model for Health and Safety. This data model includes common components such as Health and Safety user profile and actions that are used in the Health and Safety applications.

 For more information on store applications, roles, and tables installed with Health and Safety Core, see [Components installed with Health and Safety Core](../../hs-core/reference/components-installed-hs-core.md).

</td></tr></tbody>
</table>## Roles installed

<table id="table_ejw_hrr_ybc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Safety case manager

 \[sn\_hs\_cm.case\_manager\]

</td><td>

Manager for Health and Safety cases who can

-   View Health and Safety cases and their related records in the Health and Safety Workspace
-   Create, update, and delete these from the Health and Safety Workspace
    -   Health and Safety cases
    -   Return to work cases

</td><td>

-   sn\_hs\_cm.case\_reporter
-   sn\_hs\_cm.rtw\_writer
-   sn\_hs\_cm.case\_writer

</td></tr><tr><td>

Safety case reporter

 \[sn\_hs\_cm.case\_reporter\]

</td><td>

-   View cases created for the Health and Safety questions asked
-   Submit Health and Safety questions from the Employee Center

</td><td>

none

</td></tr><tr><td>

Safety case reader

 \[sn\_hs\_cm.case\_reader\]

</td><td>

-   Can view Health and Safety cases in the Health and Safety Workspace
-   Can view safety incidents and observations associated with Health and Safety cases

</td><td>

-   sn\_ohs\_im.incident\_reader
-   sn\_ohs\_im.observation\_reader
-   sn\_ohs\_im.hs\_profile\_reader
-   sn\_ohs\_im.document\_reader
-   sn\_ohs\_im.action\_reader

</td></tr><tr><td>

Safety case writer

 \[sn\_hs\_cm.case\_writer\]

</td><td>

-   Create and update Health and Safety cases in the Health and Safety Workspace
-   Can associate related safety incidents and observations to Health and Safety cases

</td><td>

-   sn\_ohs\_im.incident\_writer
-   sn\_ohs\_im.observation\_writer
-   sn\_hs\_cm.case\_reader
-   sn\_ohs\_im.document\_writer
-   sn\_ohs\_im.action\_writer

</td></tr><tr><td>

Return to work case reader

 \[sn\_hs\_cm.rtw\_reader\]

</td><td>

Can view Return to work cases in the Health and Safety Workspace

</td><td>

sn\_ohs\_im.hs\_profile\_reader

</td></tr><tr><td>

Return to work case writer

 \[sn\_hs\_cm.rtw\_writer\]

</td><td>

Safety case writer who can create and update Return to work cases in the Health and Safety Workspace

</td><td>

-   sn\_hs\_cm.case\_writer
-   sn\_hs\_cm.rtw\_reader

</td></tr><tr><td>

Claim case writer

 \[sn\_hs\_cm.claim\_case\_writer\]

</td><td>

Safety case writer who can create, update, and delete claim cases in the Health and Safety Workspace

</td><td>

-   sn\_hs\_cm.case\_writer
-   sn\_hs\_cm.claim\_case\_reader

</td></tr><tr><td>

Claim case reader

 \[sn\_hs\_cm.claim\_case\_reader\]

</td><td>

Can view Health and Safety claim cases in the Health and Safety Workspace

</td><td>

sn\_hs\_cm.case\_reader

</td></tr></tbody>
</table>## Tables installed

<table id="table_ijw_hrr_ybc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Health and Safety case

 \[sn\_hs\_cm\_case\]

</td><td>

Stores all records of Health and Safety cases. This table extends the Health and Safety task \[sn\_ohs\_im\_task\] table.

</td></tr><tr><td>

Leave

 \[sn\_hs\_cm\_leave\]

</td><td>

Stores Health and Safety cases of type Injury and illness related leave.

</td></tr><tr><td>

Health and Safety Case Payment

 \[sn\_hs\_cm\_payment\]

</td><td>

Stores payment details for Health and Safety compensation claim cases.

</td></tr></tbody>
</table>## User groups installed

<table id="table_ih5_mvg_lhc"><thead><tr><th>

Name of group

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Health and Safety routing group

</td><td>

Assignment group for Universal Request for Health and Safety cases.

</td><td>

-   agent\_workspace\_user
-   workspace\_user
-   sn\_ohs\_im.workspace\_user
-   sn\_uni\_req.routing\_agent
-   sn\_hs\_cm.case\_manager

</td></tr></tbody>
</table>**Parent Topic:**[Health and Safety Case Management reference](../concept/hs-case-management-reference.md)

