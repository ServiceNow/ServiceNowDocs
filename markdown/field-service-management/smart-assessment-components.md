---
title: Smart Assessment components
description: Several types of components are installed with the Smart Assessment feature, including tables, business rules, script includes and scheduled jobs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/smart-assessment-components.html
release: australia
product: Field Service Management
classification: field-service-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
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
</table>## Actions and roles required

Smart Assessment adds the actions and the corresponding roles required in the following table.

<table id="table_evy_dvw_t3c"><thead><tr><th>

Action

</th><th>

Role required

</th></tr></thead><tbody><tr><td>

Create templates

</td><td>

template\_manager or template\_admin

</td></tr><tr><td>

Edit templates in assessment workspace

</td><td>

Template manager \(sn\_smart\_asmt.template\_manager\) and category role associated with the template

</td></tr><tr><td>

View templates and complete assessments in the workspace or Mobile Agent app

</td><td>

Template reader \(sn\_smart\_asmt.template\_reader\), actor \(sn\_smart\_asmt.actor\), and category role associated with the templateThe template reader and actor roles are a part of the questionnaire\_user role, which is included in the wm\_agent role. Therefore, to view templates and complete assessments in the workspace, simply add the category role to the existing wm\_agent role.

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

**Parent Topic:**[Components installed with additional plugins for Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/components-inst-additional-plugin.md)

