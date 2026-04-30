---
title: Components installed with Health and Safety Incident Management
description: Several types of components are installed with installation of the Health and Safety Incident Management application, including tables, user roles, and scheduled jobs. The application also installs related plugins and store applications if they aren’t already installed.
locale: en-US
release: zurich
product: Health and Safety Incident Management
classification: health-and-safety-incident-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reference, Health and Safety Incident Management, Health and Safety, Employee Service Management]
---

# Components installed with Health and Safety Incident Management

Several types of components are installed with installation of the Health and Safety Incident Management application, including tables, user roles, and scheduled jobs. The application also installs related plugins and store applications if they aren’t already installed.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Store applications installed

<table id="table_ulz_4tw_llba"><thead><tr><th>

Store application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Health and Safety Core

</td><td>

Installs core data model for Health and Safety. This data model includes common components such as Health and Safety user profile and actions that are used in the Health and Safety applications.

 For more information on store applications, roles, and tables installed with Health and Safety Core, see [Components installed with Health and Safety Core](../../hs-core/reference/components-installed-hs-core.md).

</td></tr><tr><td>

Health and Safety Incident Management PA Content Pack

</td><td>

Generates the safety frequency rate metrics on the Health and Safety Workspace landing page.

</td></tr><tr><td>

Workplace Core \[sn\_wsd\_core\]

</td><td>

Enables workplace locations for Health and Safety Incident Management.**Important:** The application installation doesn’t install the location demo data for the Workplace Core location model. As a workaround, repair the Workplace Core plugin with the **Load demo data** option.

</td></tr></tbody>
</table>## Roles installed

<table id="table_hnm_jnp_stb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Safety agent

 \[sn\_ohs\_im.agent\]

</td><td>

Agent for Health and Safety teams who can:-   View the overall status of safety incidents and observations
-   Work on safety incidents and observations to resolve them

</td><td>

-   sn\_ohs\_im.incident\_writer\_restricted
-   workspace\_user
-   sn\_ohs\_im.report\_mapping\_reader
-   sn\_wsd\_core.location\_reader
-   sn\_ohs\_im.workspace\_user
-   sn\_ohs\_im.incident\_reader
-   canvas\_user
-   sn\_ohs\_im.establishment\_reader
-   sn\_hs\_cm.case\_reporter
-   sn\_ohs\_im.observation\_writer\_restricted
-   sn\_ohs\_im.reporter
-   sn\_ohs\_im.action\_reader
-   sn\_ohs\_im.action\_writer\_restricted
-   sn\_ohs\_im.observation\_reader
-   sn\_hs\_cm.case\_writer

</td></tr><tr><td>

Safety executive

 \[sn\_ohs\_im.executive\]

</td><td>

Executive who can:-   Access the Health and Safety executive landing page
-   View safety metrics to gain insight into how the safety team and company are performing in terms of safety
-   View the overall status of safety incidents and observations
-   Drill down into details

</td><td>

-   workspace\_user
-   sn\_ohs\_im.report\_mapping\_reader
-   sn\_wsd\_core.location\_reader
-   sn\_ohs\_im.workspace\_user
-   sn\_ohs\_im.incident\_reader
-   canvas\_user
-   sn\_ohs\_im.establishment\_reader
-   sn\_ohs\_im.reporter
-   sn\_ohs\_im.action\_reader
-   sn\_ohs\_im.observation\_reader

</td></tr><tr><td>

Safety manager

 \[sn\_ohs\_im.manager\]

</td><td>

Manager for Health and Safety teams who can:-   View the overall status of safety incidents and observations
-   Assign safety incidents and observations to safety agents
-   Work on safety incidents and observations to resolve them

</td><td>

-   sn\_ohs\_im.observation\_manager
-   workspace\_user
-   sn\_ohs\_im.action\_manager
-   sn\_ohs\_im.incident\_manager
-   sn\_ohs\_im.report\_mapping\_reader
-   sn\_ohs\_im.workspace\_user
-   canvas\_user
-   sn\_ohs\_im.establishment\_reader
-   sn\_hs\_cm.case\_reporter
-   sn\_ohs\_im.reporter
-   sn\_hs\_cm.case\_manager

</td></tr><tr><td>

Safety operations manager

 \[sn\_ohs\_im.operations\_manager\]

</td><td>

Line manager or supervisor who can:-   View Health and Safety operations landing page
-   View the overall status of safety incidents and observations
-   Report safety incidents and observations from Health and Safety Workspace
-   Work on safety incidents and observations

</td><td>

-   sn\_ohs\_im.requestor
-   sn\_wsd\_core.location\_reader
-   workspace\_user
-   canvas\_user

 -   sn\_ohs\_im.incident\_writer\_restricted
-   workspace\_user
-   sn\_ohs\_im.report\_mapping\_reader
-   sn\_wsd\_core.location\_reader
-   sn\_ohs\_im.workspace\_user
-   sn\_ohs\_im.incident\_reader
-   canvas\_user
-   sn\_ohs\_im.establishment\_reader
-   sn\_ohs\_im.observation\_writer\_restricted
-   sn\_ohs\_im.reporter
-   sn\_ohs\_im.action\_reader
-   sn\_ohs\_im.action\_writer\_restricted
-   sn\_ohs\_im.observation\_reader

</td></tr><tr><td>

Critical event agent

 \[sn\_critical.agent\]

</td><td>

Works on critical event records from initiation to resolution.

</td><td>

-   sn\_comm\_management.comm\_plan\_manager
-   task\_editor
-   canvas\_user
-   sn\_ohs\_im.workspace\_user
-   sn\_critical.read

</td></tr></tbody>
</table>## Tables installed

<table id="table_lnm_jnp_stb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Annual information

 \[sn\_ohs\_im\_annual\_information\]

</td><td>

Stores annual information for an establishment.

</td></tr><tr><td>

Health and Safety establishment

 \[sn\_ohs\_im\_establishment\]

</td><td>

Stores establishment information for an organization​. The establishment records are used to group injury and illness records for auto-filling reports such as OSHA 300, 300A, and 301 forms​.

</td></tr><tr><td>

Health and Safety incident

 \[sn\_ohs\_im\_incident\]

</td><td>

Stores all safety incident records reported by employees that have happened in the workplace. This table extends the Health and Safety task \[sn\_ohs\_im\_task\] table.

</td></tr><tr><td>

Regional details

 \[sn\_ohs\_im\_injury\_region\_data\]

</td><td>

Stores all region specific information.

</td></tr><tr><td>

People involved

 \[sn\_ohs\_im\_involved\_party\]

</td><td>

Stores all logged people involved with investigation​s. People can be existing \[sys\_users\] or external, for example, contracts and on-site visitors.​

</td></tr><tr><td>

Periodic total work hour

 \[sn\_ohs\_im\_periodic\_work\_hour\]

</td><td>

Stores periodic total hours of work per year per establishment.

</td></tr><tr><td>

Health and Safety observation

 \[sn\_ohs\_im\_observation\]

</td><td>

Stores all safety observations records reported by employees in their workplace. This table extends the Health and Safety task \[sn\_ohs\_im\_task\] table.

</td></tr><tr><td>

Health and Safety incident observation

 \[sn\_ohs\_im\_m2m\_incident\_observation\]

</td><td>

Stores all safety observation records linked to the incidents that are reported by employees in the their workplace.

</td></tr><tr><td>

Injury

 \[sn\_ohs\_im\_injury\]

</td><td>

Stores all logged injuries associated with all injury and illness report​s. A custom Seismic component is available to log injuries​.

</td></tr><tr><td>

Injury and illness

 \[sn\_ohs\_im\_injury\_illness\]

</td><td>

Stores all logged injuries and illness records. Information tracked in this table can be used for generating reports such as OSHA forms​.

</td></tr></tbody>
</table>**Parent Topic:**[Health and Safety Incident Management reference](../concept/hs-incident-mgmt-reference.md)

