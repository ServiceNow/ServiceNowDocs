---
title: Components installed with ITSM Predictive Intelligence Workbench
description: Several roles are installed with activation of the Predictive Intelligence Workbench plugin.
locale: en-US
release: yokohama
product: Predictive Intelligence Workbench
classification: predictive-intelligence-workbench
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Activate ITSM Predictive Intelligence Workbench, ITSM Predictive Intelligence Workbench administration, ITSM Predictive Intelligence Workbench, IT Service Management]
---

# Components installed with ITSM Predictive Intelligence Workbench

Several roles are installed with activation of the Predictive Intelligence Workbench plugin.

**Important:**

Starting with the yokohama release, the ITSM Predictive Intelligence Workbench will reach its end of life \(EOL\) as part of its deprecation process. It will be completely deprecated and no longer deployed, enhanced, or supported from the yokohama release. To get the latest experience for this functionality, you must install the Task Intelligence for ITSM application \(com.snc.itsm\_ml\_task\) plugin. For more information, see [Task Intelligence for ITSM](../../task-intelligence-for-itsm/concept/c-itsm-task-intelligence.md)

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

Two plugins are available to obtain feature ITSM Predictive Intelligence Workbench functionality.

-   Predictive Intelligence Workbench \(com.sn\_piwb\_ml\): Provides a common framework for creating and managing use cases.

    **Note:** Requires activation of Predictive Intelligence and Predictive Intelligence Reports plugins, which are available with an ITSM Pro subscription.

-   Predictive Intelligence Workbench ITSM content \(com.sn\_piwb\_itsm\_content\): Enables access to ITSM -specific content that provides implementation guidance for use cases created through Predictive Intelligence Workbench Also, with this plugin you can access the **Predictive Intelligence for Incidents** dashboard to communicate value across multiple applications within IT Service Management.

    **Note:** Requires activation of Predictive Intelligence Workbench, Performance Analytics - Content Pack - ITSM Dashboards, and Incident plugins.


## Predictive Intelligence Workbench

<table id="table_jzl_bkc_nlb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Predictive Intelligence Workbench admin\[piwb\_admin\]

</td><td>

Predictive Intelligence Workbench administrator. Configures the Predictive Intelligence Workbench property settings.

 Can create and manage use cases.

</td><td>

-   piwb\_manager
-   ml\_admin

</td></tr><tr><td>

Predictive Intelligence Workbench manager\[piwb\_manager\]

</td><td>

Typically a business process architect. Can create and manage use cases.

 Configures the Predictive Intelligence Workbench property settings.

 Monitors the **Predictive Intelligence for Incidents** dashboard.

</td><td>

-   ml\_admin
-   piwb\_viewer
-   pa\_admin

</td></tr><tr><td>

Predictive Intelligence Workbench viewer\[piwb\_viewer\]

</td><td>

Can view the **Predictive Intelligence for Incidents** dashboard.

</td><td>

-   pa\_viewer
-   ml\_report\_user

</td></tr></tbody>
</table>**Note:** All new records are created and updated through the Predictive Intelligence Workbench application. Only users with the maint role can update the base system tables.

<table id="table_dht_bpj_nlb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Usecase Prediction Run\[piwb\_prediction\_run\]

</td><td>

Used to define the test prediction type for a use case, whether it is a single or batch test.

</td></tr><tr><td>

PIWB Use Case Template\[piwb\_usecase\_template\]

</td><td>

Used to create a use case template. Extends the Application File \[sys\_metadata\] table.

</td></tr><tr><td>

Setup Assistant Tracker\[piwb\_usecase\_sa\_tracker\]

</td><td>

Used to track the status of the guided path steps \(Stage or Task\).

</td></tr><tr><td>

PIWB Setup Assistant Stage Task\[piwb\_sa\_stage\_task\]

</td><td>

Used to store the tasks for each stage of setup assistant plan . Extends the PIWB Setup Assistant Base Task \[piwb\_sa\_task\_base\] table.

</td></tr><tr><td>

PIWB Setup Assistant Plan\[piwb\_sa\_plan\]

</td><td>

Used to define the Setup Assistant Plan \(Guided Path\) for each type of use case.

</td></tr><tr><td>

PIWB Setup Assistant Base Task\[piwb\_sa\_task\_base\]

</td><td>

Used to create a new Setup Assistant Base Task record and to make the task active.

</td></tr><tr><td>

PIWB Use Case\[piwb\_usecase\]

</td><td>

Used to create a new use case per prebuilt template \(piwb\_admin and piwb\_manager can create, update, and delete; piwb\_viewer can only view\).

</td></tr><tr><td>

PI Solution Model\[piwb\_model\]

</td><td>

Used to create a **Predictive Intelligence** solution model and to make the model active \(piwb\_admin and piwb\_manager can create, update, and delete; piwb\_viewer can only view\).

</td></tr><tr><td>

PIWB Setup Assistant Stage\[piwb\_sa\_stage\]

</td><td>

Extends the PIWB Setup Assistant Base Task \[piwb\_sa\_task\_base\] table.

</td></tr><tr><td>

Usecase Prediction Result\[piwb\_prediction\_result\]

</td><td>

Used to define a use case prediction result based on the Prediction Run and Model \(piwb\_admin and piwb\_manager can create, update, and delete; piwb\_viewer can only view\).

</td></tr><tr><td>

PI Solution Comment\[piwb\_model\_comment\]

</td><td>

Used to define a comment on a **Predictive Intelligence** solution for a given class \(piwb\_admin and piwb\_manager can create, update, and delete; piwb\_viewer can only view\).

</td></tr></tbody>
</table>