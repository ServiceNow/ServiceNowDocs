---
title: Migrated components
description: When you migrate a survey, the system maps records from survey tables to assessment tables.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Legacy survey migration, Survey administration, Use, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Migrated components

When you migrate a survey, the system maps records from survey tables to assessment tables.

To create a functional survey on the assessment framework, the system converts survey records to the most logical equivalent assessment survey records. This may mean multiple assessment survey records represent one legacy survey record.

<table id="table_x1l_gph_45"><thead><tr><th>

Survey component

</th><th>

Assessment survey components

</th></tr></thead><tbody><tr><td>

Survey master \[survey\_master\]

</td><td>

-   Survey definition \[asmt\_metric\_type\]
-   Assessable record \[asmt\_assessable\_record\], for system use only
-   Survey category \[asmt\_metric\_category\]

</td></tr><tr><td>

Survey question \[survey\_question\_new\]

</td><td>

Survey question \[asmt\_metric\]

</td></tr><tr><td>

Question choice \[question\_choice\]

</td><td>

Assessment metric definition \[asmt\_metric\_definition\]

</td></tr><tr><td>

Survey instance \[survey\_instance\]

</td><td>

-   Assessment group \[asmt\_assessment\], for system use only
-   Survey instance \[asmt\_assessment\_instance\]

</td></tr><tr><td>

Survey response \[survey\_response\]

</td><td>

-   Survey instance question \[asmt\_assessment\_instance\_question\]
-   Survey response \[asmt\_metric\_result\]
-   Category result \[asmt\_category\_result\], for system use only

</td></tr></tbody>
</table>**Parent Topic:**[Legacy survey migration](../concept/c_MigrateSurveys.md)

**Related topics**  


[Migrate a legacy survey](../task/t_MigrateALegacySurvey.md)

[Survey question migration](r_SurveyQuestionMigration.md)

[Migrated question review](r_ReviewMigratedQuestions.md)

