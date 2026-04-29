---
title: Smart Assessment components
description: Several types of components are installed with the Smart Assessment feature, including tables, business rules, script includes and scheduled jobs.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Components installed with additional plugins, Reference, Field Service Management]
---

# Smart Assessment components

Several types of components are installed with the Smart Assessment feature, including tables, business rules, script includes and scheduled jobs.

## Tables

Smart Assessment adds the table listed in the following table.

<table id="table_emm_nqh_12c"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Questionnaire Template\[sn\_fsm\_smart\_asmt\_template\]

</td><td>

Stores information about Smart Assessment templates and its associated questionnaire.

</td></tr></tbody>
</table>## Business Rules

Smart Assessment adds the business rules listed in the following table.

<table id="table_ot4_gvh_12c"><thead><tr><th>

Business Rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Trigger smart assessment

</td><td>

Work Order Task\[wm\_task\]

</td><td>

Generates Smart Assessment instances for work order tasks.

</td></tr><tr><td>

Trigger smart assessment

</td><td>

Work Order\[wm\_order\]

</td><td>

Generates Smart Assessment instances for work orders.

</td></tr><tr><td>

Trigger smart assessment

</td><td>

Affected Product\[wm\_m2m\_product\_to\_work\_order\]

</td><td>

Generates Smart Assessment instances for affected products.

</td></tr><tr><td>

Verify Duplicate Association Of Template

</td><td>

Questionnaire template\[sn\_fsm\_smart\_asmt\_template\]

</td><td>

Ensures that each smart assessment template is associated with only one questionnaire record. A smart assessment template can't be linked to multiple questionnaire records.

</td></tr></tbody>
</table>## Script Includes

Smart Assessment adds the script includes listed in the following table.

|Script Include|Description|
|--------------|-----------|
|FSMSmartAsmtUIControlSNC|Has methods to control UI components and actions based on the configuration for Smart Assessment.|
|FSMSmartAsmtUIControl|Contains a customizable wrapper for the script FSMSmartAsmtUIControlSNC.|
|FSMSmartAssessmentUtilSNC|Contains methods for all reference qualifiers and generates assessments from the Smart Assessment template if the conditions are met.|
|FSMSmartAssessmentUtil|Contains a customizable wrapper for the script FSMSmartAssessmentUtilSNC.|
|FSMSmartAssessmentDaoSNC|Contains all the database queries related to Smart Assessment.|
|FSMSmartAssessmentDao|Contains a customizable wrapper for the script FSMSmartAssessmentDaoSNC.|
|FSMSmartAssessmentMigrationHelperSNC|Contains methods related to survey type questionnaire and its instances migration to Smart Assessment.|
|FSMSmartAssessmentMigrationHelper|Wrapper|
|FSMSmartAssessmentsConstants|Holds the constants for Smart Assessment.|
|QuestionnaireUtilSmartAssessmentImpl|Implements the extension point QuestionnaireUtilExtPoint and contains utility methods for questionnaires and assessments.|
|QuestionnaireUtilAjax|Contains methods to alter fields on the record page based on the configuration.|

## Scheduled Job

Smart Assessment adds the scheduled job listed in the following table.

|Scheduled Job|Description|
|-------------|-----------|
|Migrate survey instances to smart assessments|Migrates questionnaire instances to Smart Assessment and re-triggers the migrated instances.|

**Parent Topic:**[Components installed with additional plugins for Field Service Management](components-inst-additional-plugin.md)

