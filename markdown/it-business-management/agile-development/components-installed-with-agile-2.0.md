---
title: Components installed with Agile Development 2.0
description: Several types of components are installed with activation of the Agile Development 2.0 plugin, including tables, user roles, and properties.Properties are added with activation of Agile Development 2.0.
locale: en-US
release: australia
product: Agile Development
classification: agile-development
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Agile Development 2.0 reference, Agile Development 2.0, Agile Development, Strategic Portfolio Management]
---

# Components installed with Agile Development 2.0

Several types of components are installed with activation of the Agile Development 2.0 plugin, including tables, user roles, and properties.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

Demo data is available for this feature.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Scrum admin\[scrum\_admin\]

</td><td>

A scrum admin has full control on the Agile Development 2.0 application.

</td><td>

-   scrum\_user
-   rm\_product\_admin
-   rm\_task\_admin
-   rm\_test\_admin
-   rm\_doc\_admin
-   rm\_story\_admin
-   rm\_epic\_admin
-   rm\_releasescrum\_admin
-   rm\_sprint\_admin

</td></tr><tr><td>

Scrum master\[scrum\_master\]

</td><td>

A scrum master guides team members through a sprint and serves as a sounding board for issues that arise.

 A scrum master can move stories between a release backlog and a sprint. This user can create and manage:

 -   Epics
-   Stories
-   Sprints
-   Team Members

</td><td>

-   scrum\_sprint\_planner
-   scrum\_story\_creator
-   scrum\_user

</td></tr><tr><td>

Scrum product owner\[scrum\_product\_owner\]

</td><td>

Users with this role are responsible for the business value of a project and for maintaining the product backlog.

 A product owner can move stories between the product backlog and releases. This user can create and manage:

-   Themes
-   Epics
-   Stories
-   Products
-   Releases
-   Teams

</td><td>

-   scrum\_release\_planner
-   scrum\_story\_creator
-   scrum\_user

</td></tr><tr><td>

Scrum release planner\[scrum\_release\_planner\]

</td><td>

Users with this role perform release planning activities.

 A release planner can create and manage:

-   Themes
-   Products
-   Releases

</td><td>

-   scrum\_user
-   scrum\_story\_creator

</td></tr><tr><td>

Scrum sprint planner\[scrum\_sprint\_planner\]

</td><td>

Users with this role manage the sprint process.

 A sprint planner can create and manage:

-   Stories
-   Sprints

</td><td>

-   scrum\_user
-   scrum\_story\_creator

</td></tr><tr><td>

Scrum story creator\[scrum\_story\_creator\]

</td><td>

Users with this role create the descriptive elements of a product.

 A story creator can create and manage:

-   Epics
-   Stories
-   Tasks

</td><td>

-   rm\_scrum\_task\_admin
-   scrum\_user

</td></tr><tr><td>

Scrum story editor \[scrum\_story\_editor\]

</td><td>

Users with this role have edit access to the Story \[rm\_story\] table.

</td><td>

-   scrum\_user
-   rm\_scrum\_task\_admin

</td></tr><tr><td>

Scrum team member\[scrum\_team\_member\]

</td><td>

Users with this role are the scrum users who work on a story in a sprint.

 A team member can create a scrum task, perform updates to a story, and log enhancement requests or defect reports.

</td><td>

-   scrum\_user
-   scrum\_story\_creator
-   scrum\_story\_editor
-   rm\_defect\_admin
-   rm\_enhancement\_admin
-   rm\_scrum\_task\_admin

</td></tr><tr><td>

Scrum task admin\[rm\_scrum\_task\_admin\]

</td><td>

Scrum task administrator with access to \[rm\_scrum\_task\] table.

</td><td>

scrum\_user

</td></tr><tr><td>

Scrum user\[scrum\_user\]

</td><td>

Basic scrum role that all other roles inherit. It confers read-only rights to the Agile Development application.

 A scrum user can view all elements of agile, but cannot create, edit, or manage records of any type.

</td><td>

cmdb\_read

</td></tr></tbody>
</table>## Tables installed

<table id="table_AgileDev2.0"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Product Assignment Group\[m2m\_product\_group\]

</td><td>

Stores relationship between products and groups.

</td></tr><tr><td>

Release Assignment Group\[m2m\_release\_group\]

</td><td>

Stores relationship between releases and groups.

</td></tr><tr><td>

Application Model \[cmdb\_application\_product\_model\]

</td><td>

Represents whole product whose releases are being managed.

</td></tr><tr><td>

Release Product\[m2m\_product\_release\]

</td><td>

Represents all managed products.

</td></tr><tr><td>

Story Dependencies\[m2m\_story\_dependencies\]

</td><td>

Represents all related stories \(prerequisite and dependent\) to an existing story.

</td></tr><tr><td>

Scrum task\[rm\_scrum\_task\]

</td><td>

Represents a discrete amount of work for a story carried out during a sprint.

</td></tr><tr><td>

Release team member\[scrum\_pp\_release\_team\_member\]

</td><td>

Represents the list of users who are part of a release.

</td></tr><tr><td>

Sprint team member\[scrum\_pp\_sprint\_team\_member\]

</td><td>

Represents the list of users who are part of a sprint.

</td></tr><tr><td>

Team\[scrum\_pp\_team\]

</td><td>

Represents who completes scrum tasks and stories during releases and sprints.

</td></tr><tr><td>

Team name\[scrum\_pp\_team\_name\]

</td><td>

Represents the name of the scrum team.

</td></tr><tr><td>

Theme\[scrum\_theme\]

</td><td>

Represents either a tangible product \(such as a trading application\) or an abstract goal \(such as performance tuning\).

</td></tr><tr><td>

Scrum release \[rm\_release\_scrum\]

</td><td>

Represents individual versions \(releases\) of the product. Each release contains a list of sprints with a time range in which the stories in those sprints must be completed.

</td></tr><tr><td>

Sprint \[rm\_sprint\]

</td><td>

Stores sprints, which are the backlog items to be addressed together during a given time period.

</td></tr><tr><td>

Epic \[rm\_epic\]

</td><td>

Represents related stories or requirements that you have not yet transformed into stories.

</td></tr><tr><td>

Story \[rm\_story\]

</td><td>

Represents self-contained pieces of work that can be completed within a sprint.

</td></tr><tr><td>

Defect \[rm\_defect\]

</td><td>

Represents a deviation from the expected behavior of a product.

</td></tr><tr><td>

Documentation Task \[rm\_doc\]

</td><td>

Represents documentation tasks for the product.

</td></tr><tr><td>

Enhancement \[rm\_enhancement\]

</td><td>

Represents an improvement to an existing product.

</td></tr><tr><td>

SDLC release \[rm\_release\_sdlc\]

</td><td>

Represents individual versions of the product.

</td></tr><tr><td>

Testing Task \[rm\_test\]

</td><td>

Represents testing tasks for the product.

</td></tr></tbody>
</table>**Note:**

Dashboards in Agile Development require a separate plugin to be installed and configured. For information about Agile 2.0 dashboards and reports, including burndown charts and cumulative flow diagrams, see [Agile Development process flow](../concept/agile-development-process-flow.md) and [Performance Analytics Content Pack for Agile 2.0](../../../use/dashboards/application-content-packs/pa-content-pack-for-agile-2.0.md).

**Parent Topic:**[Agile Development 2.0 reference](agile-development-2-reference.md)

## Properties installed with Agile Development 2.0

Properties are added with activation of Agile Development 2.0.

Agile Development 2.0 adds the following properties.

**Note:** All of these properties are located in the System Properties \[sys\_properties\] table. To access the table, enter `sys_properties.list` in the navigation filter.

<table id="agile2.0_properties"><thead><tr><th>

Property

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

Draw Burndown Chart ideal line as a linear straight linecom.snc.sdlc.scrum.pp.burndown.ideal.linear

</td><td>

Draws the burn down chart ideal line as a straight line.-   Type: true\|false
-   Default value: false

</td></tr><tr><td>

Stories in any one of the states specified in this comma separated list will be shown in the progress board \(in the order specified\)com.snc.sdlc.scrum.pp.progress.story.states

</td><td>

Specify the story states using a comma separated list that should be shown in the story progress board. The states in the progress board follow the same order as specified here.-   Type: integer
-   Default values in their order:
    -   -6: Draft
    -   1: Ready
    -   2: Work in progress
    -   -7: Ready for testing
    -   -8: Testing
    -   3: Complete

</td></tr><tr><td>

Tasks in any one of the states specified in this comma separated list will be shown in the progress board \(in the order specified\)com.snc.sdlc.scrum.pp.progress.task.state

</td><td>

Specify the task states using a comma separated list that should be shown in the progress board. The states in the progress board follow the same order as specified here.-   Type: integer
-   Default values in their order:
    -   -6: Draft
    -   1: Ready
    -   2: Work in progress
    -   3: Complete

</td></tr><tr><td>

Enable the Actual Hours field for scrum taskscom.snc.sdlc.scrum.pp.task\_uses\_actual\_hours

</td><td>

Enable the Actual hours field in the Scrum Task form. Displays actual hours of tasks on the task progress board.-   Type: true\|false
-   Default value: true

</td></tr><tr><td>

The default sprint length \(in days\) used if the length cannot be calculated from the sprint.com.snc.sdlc.scrum.pp.default\_sprint\_length

</td><td>

Specify a default sprint duration that should be used when creating a sprint, if the sprint length cannot be calculated from the sprint.-   Type: integer
-   Default value: 14

</td></tr></tbody>
</table>