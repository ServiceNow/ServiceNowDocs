---
title: Installed with Assessments and Surveys
description: Several types of components are installed with the activation of Assessments and Surveys.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 20
breadcrumb: [Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Installed with Assessments and Surveys

Several types of components are installed with the activation of Assessments and Surveys.

-   Demo data is available for Assessments and Surveys.
-   ServiceNow® Vendor Performance offers an extra set of vendor assessment demo data.

## Tables

<table id="table_tables"><thead><tr><th>

Table

</th><th>

Description: Assessments

</th><th>

Description: Surveys

</th></tr></thead><tbody><tr><td>

Assessable Record \[asmt\_assessable\_record\]

</td><td>

Stores all [assessable records](../concept/c_assessable-records.md).

</td><td>

For system use only.

</td></tr><tr><td>

Assessment Category Result \[asmt\_category\_result\]

</td><td>

Stores all [category results](../../survey-administration/concept/c_SchedulePeriods.md).

</td><td>

For system use only.

</td></tr><tr><td>

Assessment Category User \[asmt\_m2m\_category\_user\]

</td><td>

Stores associations between users and metric categories that they can evaluate. A user that is associated to a category is a [category user](r_CategoryUsersAndStakeholders.md).

</td><td>

Stores associations between users and surveys. A user that is associated to a survey is a [survey user](../../survey-administration/concept/c_SurveyUsersAndGroups.md) and is automatically associated to all the survey's categories.

</td></tr><tr><td>

Assessment Group \[asmt\_assessment\]

</td><td>

Stores all [assessment groups](r_CategoryResults.md).

</td><td>

For system use only.

</td></tr><tr><td>

Assessment Instance \[asmt\_assessment\_instance\]

</td><td>

Stores all [assessment instances](../concept/c_AssessmentInstances.md).

</td><td>

Stores all [survey instances](../../survey-administration/task/t_ViewSurveyInstance.md).

</td></tr><tr><td>

Assessment Instance Question \[asmt\_assessment\_instance\_question\]

</td><td>

Stores all assessment instance questions, each of which represents one question on one assessment instance.

</td><td>

Stores all survey instance questions, each of which represents one question on one survey instance.

</td></tr><tr><td>

Assessment Metric \[asmt\_metric\]

</td><td>

Stores all [metrics](../concept/c_AssessmentMetrics.md).

</td><td>

Stores all survey questions.

</td></tr><tr><td>

Assessment Metric Definition \[asmt\_metric\_definition\]

</td><td>

Stores all [metric definitions](../task/t_CreateAMetricDefinition.md).

</td><td>

Stores all [answer options](../../survey-administration/task/t_CreateOrModifyAnswerOptions.md) for survey questions.

</td></tr><tr><td>

Assessment Metric Template \[asmt\_template\]

</td><td>

Stores all [metric templates](r_MetricTemplates.md).

</td><td>

Stores all question templates.

</td></tr><tr><td>

Assessment Metric Type \[asmt\_metric\_type\]

</td><td>

Stores all [metric types](../concept/c_AssessmentInstances.md).

</td><td>

Stores all [survey definitions](../../survey-administration/concept/c_SurveyDefinitions.md).

</td></tr><tr><td>

Assessment Stakeholders \[asmt\_m2m\_stakeholder\]

</td><td>

Stores associations between assessable records and category users. A category user that is associated to an assessable record is a [stakeholder](../concept/c_MetricTypesAndAssessableRecords.md).

</td><td>

Not used for surveys.

</td></tr><tr><td>

Assessment Template Definition \[asmt\_template\_definition\]

</td><td>

Stores all [metric template definitions](r_MetricTemplates.md).

</td><td>

Stores all question template definitions.

</td></tr><tr><td>

Assessment X Category Matrix \[asmt\_m2m\_xcategory\_matrix\]

</td><td>

Users can specify metric categories as the X axis of a [decision matrix](r_AdministerDecisionMatrixes.md).

</td><td>

Not used for surveys.

</td></tr><tr><td>

Assessment Y Category Matrix \[asmt\_m2m\_ycategory\_matrix\]

</td><td>

Users can specify metric categories as the Y axis of a decision matrix.

</td><td>

Not used for surveys.

</td></tr><tr><td>

Bubble Chart \[asmt\_bubble\_chart\]

</td><td>

Stores all [bubble chart](../../service-administration/reference/r_BubbleChartComponents.md) definitions.

</td><td>

Not used for surveys.

</td></tr><tr><td>

Category Assessable Records \[asmt\_m2m\_category\_assessment\]

</td><td>

Stores associations between assessable records and metric categories.

</td><td>

For system use only.

</td></tr><tr><td>

Decision Matrix \[asmt\_decision\_matrix\]

</td><td>

Stores all [decision matrixes](r_AdministerDecisionMatrixes.md).

</td><td>

Not used for surveys.

</td></tr><tr><td>

Metric Category \[asmt\_metric\_category\]

</td><td>

Stores all [metric categories](../concept/c_AssessmentMetrics.md).

</td><td>

Stores all survey categories.

</td></tr><tr><td>

Metric Result \[asmt\_metric\_result\]

</td><td>

Stores all [metric results](../task/t_ViewAMetricResult.md).

</td><td>

Stores all [survey responses](../../survey-administration/concept/c_SurveyResults.md).

</td></tr><tr><td>

Signature \[asmt\_signature\]

</td><td>

Stores all [signature records](../task/t_CreateAnAssessmentSignature.md) for assessments and \[\[Attestations\|GRC attestations\]\].

</td><td>

Stores all signature records for[Surveys](../../survey-administration/reference/r_SurveyManagementLandingPage.md).

</td></tr><tr><td>

Trigger Condition \[asmt\_condition\]

</td><td>

Stores all [assessment trigger conditions](../task/t_CreateTriggerAssessment.md).

</td><td>

Stores all [survey trigger conditions](../../survey-administration/concept/c_TriggerConditions.md).

</td></tr></tbody>
</table>## Properties

You can configure various properties to customize the appearance of Assessments and Surveys questionnaires, require authentication for user signatures, open surveys in the Service Portal view from emails, and limit the number of items shown in a decision matrix field filter.

Assessments and Surveys installs the following properties. You can find these properties by navigating to the following locations:

-   **All** &gt; **Assessments** &gt; **Administration** &gt; **Assessment Properties**
-   **All** &gt; **Survey** &gt; **Administration** &gt; **Properties**

**Important:** You can customize the css.assessment.question.header.background.color, assessment.caption.background.color, and the css.assessment.caption.font.color fields only if Next Experience is turned off.

<table id="table_properties"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_portal\_surveys.sp\_survey.email\_redirection

</td><td>

When this property is enabled, users can use a link in an email to open a survey or assessment in Service Portal.-   Type: **Yes** or **No**
-   Default value: **Yes**

</td></tr><tr><td>

com.snc.assessment.signature\_authentication

</td><td>

When this property is enabled, an authentication is required by user signature. When **Yes** is selected, this property requires credentials for a full name signature.-   Type: **Yes** or **No**
-   Default value: **Yes**

 For more information about working with signatures, see [Signatures](../task/t_CreateAnAssessmentSignature.md).

</td></tr><tr><td>

com.snc.assessment.collect.stats

</td><td>

List of Assessments for which Recent Sent &amp; Recent Completed stats must be collected in an asmt\_assessment\_stat table. Comma-separated list of eligible Assessment Metric Type Sys IDs.

</td></tr><tr><td>

css.assessment.question.header.background.color

</td><td>

Background color of question headers on assessment and survey questionnaires.-   Type: **Color**
-   Default value: **\#767676**

</td></tr><tr><td>

sn\_portal\_surveys.sp\_survey.show\_progress\_bar

</td><td>

Shows or hides a progress bar on the survey pages on Service Portal.-   Type: **Yes** or **No**
-   Default value: **Yes**

**Note:** If the Pagination setting is set to **None**, the survey is displayed in a single page, and no progress bar is shown.

</td></tr><tr><td>

show\_lang\_picker\_for\_publicsurveys

</td><td>

Enable or disable whether to show language picker when a public survey is taken.-   Type: **Yes** or **No**
-   Default value: **Yes**

</td></tr><tr><td>

css.assessment.caption.background.color

</td><td>

Sets the background color of the caption on assessment and survey questionnaires.-   Type: Color
-   Default value: **\#eee**

</td></tr><tr><td>

com.snc.assessment.decision\_matrix\_filter\_max\_entries

</td><td>

Maximum number of items to show for a decision matrix field filter.-   Type: integer
-   Default value: **1000**

</td></tr><tr><td>

css.assessment.caption.font.color

</td><td>

Sets the font color of the caption text on assessment and survey questionnaires.-   Type: color
-   Default value: **\#ffffff**

</td></tr></tbody>
</table>For more information about customizing the appearance of a survey, see [Customize the appearance of a survey](../../survey-administration/task/t_CustomizingAppearance.md).

## User roles

<table id="table_roles"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

assessment administrator\[assessment\_admin\]

</td><td>

Can administer the Assessments application. Can access all the modules of the Assessments application.**Note:** The assessment\_admin role is contained by the itil\_admin role. This role is also contained by the survey\_admin role.

</td><td>

None

</td></tr></tbody>
</table>## Script includes

|Name|Description|
|----|-----------|
|AssessmentUtils|Core code for assessment functionality.|
|AssessmentUtilsAJAX|AJAX-based code for displaying scorecard data.|
|MigrateSurveyToAssessment|Code for [migrating legacy surveys](../../survey-administration/concept/c_MigrateSurveys.md) to assessment surveys.|
|RatingUtilsAJAX|Reserved for future use.|
|SurveyUtils|Core code for survey functionality.|

## Client scripts

<table id="table_ClientScripts"><thead><tr><th>

Name

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Calculate Assessable Record Field choice list

</td><td>

Trigger Condition \[asmt\_condition\]

</td><td>

Limits the Assessable Record Field choices to those choices that are compatible with the selected assessment.

</td></tr><tr><td>

Check survey schedule period

</td><td>

Trigger Condition \[asmt\_condition\]

</td><td>

Checks the selected survey definition's Schedule period. If Schedule period is set to Only Once, this client script displays a warning message that each user can only take the selected survey once.

</td></tr><tr><td>

Clear display\_when when depends changed

</td><td>

Assessment Metric \[asmt\_metric\]

</td><td>

Shows the **Display when** field when the **Depends on** field is set. Clears the **Display when** field when the **Depends on** field changes and the options must change.

</td></tr><tr><td>

Conditionally Set Type for Surveys

</td><td>

Group \[sys\_user\_group\]

</td><td>

Sets the user group Type to survey if you create a new group from the User Groups module.

</td></tr><tr><td>

Data type -- Hide choices for surveys

</td><td>

Assessment Metric \[asmt\_metric\]

</td><td>

Ensures only Data type options that are valid for surveys are available on the Survey Question form.

</td></tr><tr><td>

Data type -- Show/Hide Not Applicable

</td><td>

Assessment Metric \[asmt\_metric\]

</td><td>

Hides the **Allow not applicable** field and sets its value to **false** if the metric method is Assessment and the data type is **Percentage**, **Checkbox**, **Date**, **Date/Time**, **Number**, or **String**.

</td></tr><tr><td>

Data type defaults to String for surveys

</td><td>

Assessment Metric \[asmt\_metric\]

</td><td>

Sets the default **Data type** field value to **String** on the Survey Question form.

</td></tr><tr><td>

Fetch Min/Max

</td><td>

Assessment Metric \[asmt\_metric\]

</td><td>

Updates the **Min** and **Max** fields to match the least and greatest metric template definition values if an assessment administrator selects or changes the Template value.

</td></tr><tr><td>

Hide Assessable Record Field

</td><td>

Trigger Condition \[asmt\_condition\]

</td><td>

Hides the **Assessable Record** field unless the evaluation method of the metric type selected in the **Assessment** field is **Assessment**.

</td></tr><tr><td>

Hide Survey Instance Trigger ID if empty

</td><td>

Assessment Instance \[asmt\_assessment\_instance\]

</td><td>

Hides the **Trigger ID** field and makes it read-only unless it contains a value.

</td></tr><tr><td>

Hide user lists

</td><td>

Assessable Record \[asmt\_assessable\_record\]

</td><td>

Hides the **Category users** related list if the associated metric type schedule type is **On demand**.

</td></tr><tr><td>

Hide user related lists

</td><td>

Metric Category \[asmt\_metric\_category\]

</td><td>

Hides the User related list if the associated metric schedule type is **On demand** and the **Evaluation method** isn't **Survey**.

</td></tr><tr><td>

Hide value or String value

</td><td>

Assessment Instance Question \[asmt\_assessment\_instance\_question\]

</td><td>

Hides the **Value** field and shows the **String value** field if the associated metric data type is **Date**, **Date/Time**, or **String**. Does the opposite if the data type is anything or else.

</td></tr><tr><td>

Live feed deletion warning

</td><td>

Assessable Record \[asmt\_assessable\_record\]

</td><td>

Displays a warning message if an assessment administrator clears the **Live feed** check box.

</td></tr><tr><td>

Method -- Show/Hide Not applicable

</td><td>

Assessment Metric \[asmt\_metric\]

</td><td>

Hides the **Mandatory** and **Allow not applicable** fields and sets both values to **false** if the metric method is Script. Shows the **Mandatory** field if the metric method is Assessment. Shows the **Allow not applicable** field if the method is Assessment, except when the data type is **Percentage**, **Checkbox**, **Date**, **Date/Time**, **Number**, or **String**.

</td></tr><tr><td>

Min/Max Control

</td><td>

Assessment Metric \[asmt\_metric\]

</td><td>

Makes the **Min** and **Max** fields mandatory except when the data type is **Template**.

</td></tr><tr><td>

Min/Max Read-only

</td><td>

Assessment Metric \[asmt\_metric\]

</td><td>

Makes the **Min** and **Max** fields read-only when the data type is **Choice** or **Likert Scale**.

</td></tr><tr><td>

Populate Groups

</td><td>

Assessment Metric Type \[asmt\_metric\_type\]

</td><td>

Populates the available values for the **Filter** field with fields from the selected metric type table.

</td></tr><tr><td>

Read only Type

</td><td>

Metric Category \[asmt\_metric\_category\]

</td><td>

Makes the **Type** field read-only when it contains a value.

</td></tr><tr><td>

Reload Decision Matrix Filter Columns

</td><td>

Assessment Metric Type \[asmt\_metric\_type\]

</td><td>

Populates the available choices for the **Default matrix** filter as appropriate if the **Filter** field value changes.

</td></tr><tr><td>

Reload default filters

</td><td>

Assessment Metric Type \[asmt\_metric\_type\]

</td><td>

Populates the available choices for the **Default filter** as appropriate if the **Display all filters** value changes.

</td></tr><tr><td>

Set scale factor

</td><td>

Assessment Metric Type \[asmt\_metric\_type\]

</td><td>

Reserved for future use.

</td></tr><tr><td>

Set table field

</td><td>

Metric Category \[asmt\_metric\_category\]

</td><td>

Sets the category Table value to that of the metric type.

</td></tr><tr><td>

Show and Hide Scheduled Job

</td><td>

Assessment Metric Type \[asmt\_metric\_type\]

</td><td>

Hides the **Scheduled job** field if the Schedule type is **On demand** and shows the **Scheduled job** field if the Schedule type is **Scheduled**.

</td></tr><tr><td>

Show and Hide Scheduled Job Survey View

</td><td>

Assessment Metric Type \[asmt\_metric\_type\]

</td><td>

Shows the **Scheduled job** field on the Survey Definition form if the Schedule period is **Daily**, **Weekly**, **Monthly**, or **Yearly**.

</td></tr><tr><td>

Toggle Metric Definitions \(Load\)

</td><td>

Assessment Metric \[asmt\_metric\]

</td><td>

Displays the Assessment Metric Definitions related list if the data type is **Choice** or **Likert Scale**.

</td></tr><tr><td>

Toggle Metric Definitions \(Update\)

</td><td>

Assessment Metric \[asmt\_metric\]

</td><td>

Displays the Assessment Metric Definitions related list if the data type is **Choice** or **Likert Scale**. Sets the **Method** field to the appropriate value if the data type is compatible with one method only.

</td></tr><tr><td>

Update Min And Max Default Values

</td><td>

Assessment Metric \[asmt\_metric\]

</td><td>

Sets reasonable default values for the **Min** and **Max** fields, based on the data type.

</td></tr><tr><td>

Validate Probability

</td><td>

Survey Trigger Condition \[asmt\_condition\]

</td><td>

Ensures that the **Probability \(%\)** value is a whole number between **1** and **100**.

</td></tr><tr><td>

Verify Max

</td><td>

Assessment Metric \[asmt\_metric\]

</td><td>

Verifies that the **Max** value is greater than the **Min** value and greater than or equal to zero if the metric method is Assessment.

</td></tr><tr><td>

Verify Min

</td><td>

Assessment Metric \[asmt\_metric\]

</td><td>

Verifies that the **Min** value is less than the **Max** value and greater than or equal to zero if the metric method is Assessment.

</td></tr><tr><td>

Verify Value

</td><td>

Assessment Metric Definition\[asmt\_metric\_definition\]

</td><td>

Verifies that the Value is greater than or equal to zero.

</td></tr><tr><td>

Verify Value

</td><td>

Assessment Template Definition\[asmt\_template\_definition\]

</td><td>

Verifies that the Value is greater than or equal to zero.

</td></tr></tbody>
</table>## Business rules

<table id="table_BusinessRules"><thead><tr><th>

Name

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assessable domain matches type

</td><td>

Assessable Record \[asmt\_assessable\_record\]

</td><td>

Ensures that all new assessable records are in the same domain as the metric type. This is a special requirement of assessment domain separation, that all records must be in the same domain.

</td></tr><tr><td>

Auto stakeholder creation

</td><td>

Assessment Category User \[asmt\_m2m\_category\_user\]

</td><td>

Assigns new category users as stakeholders automatically for assessable records if the associated category has the **Create stakeholders** option selected.

</td></tr><tr><td>

Auto stakeholder creation

</td><td>

Category Assessable Records \[asmt\_m2m\_category\_assessment\]

</td><td>

Creates stakeholders from all of a category's category users automatically for new assessable records if:-   The **Create stakeholders** option is selected for the metric category.
-   The same metric category is associated to the new assessable record.

</td></tr><tr><td>

Auto stakeholder creation

</td><td>

Metric Category \[asmt\_metric\_category\]

</td><td>

Assigns all of a category's category users as stakeholders for each assessable record associated to the category when the **Create stakeholders** option is selected for the category.

</td></tr><tr><td>

Calculate category max weight

</td><td>

Assessment Metric \[asmt\_metric\]

</td><td>

Calculates the sum of all metric weights in a category.

</td></tr><tr><td>

Cancel notification workflow

</td><td>

Assessment Instance \[asmt\_assessment\_instance\]

</td><td>

Cancels the workflow that generates assessment email notifications when an assessment instance is deleted or changes the state to **Complete** or **Canceled**.

</td></tr><tr><td>

Category domain matches type

</td><td>

Metric Category \[asmt\_metric\_category\]

</td><td>

Ensures that all new categories are in the same domain as the metric type. This is a special requirement of assessment domain separation, that all records must be in the same domain.

</td></tr><tr><td>

Check Live Feed Groups

</td><td>

Assessable Record \[asmt\_assessable\_record\]

</td><td>

Selects the **Live feed** option if a Live Feed group is associated with the source record. If the **Live feed** option is selected and no Live Feed group is associated with the source record, this business rule clears the check box.

</td></tr><tr><td>

Check only one default

</td><td>

Bubble Chart \[asmt\_bubble\_chart\]

</td><td>

Ensures that there is only one default bubble chart for a metric type.

</td></tr><tr><td>

Check only one default

</td><td>

Decision Matrix \[asmt\_decision\_matrix\]

</td><td>

Ensures that there is only one default decision matrix for a metric type.

</td></tr><tr><td>

Create actual results

</td><td>

Assessment Instance \[asmt\_assessment\_instance\]

</td><td>

Generates assessment and category results from the user responses if a user completes an assessment.

</td></tr><tr><td>

Create Business Rule on Remote table

</td><td>

Assessment Metric Type \[asmt\_metric\_type\]

</td><td>

Generates the following business rules if an assessment administrator creates or updates a metric type:-   Business rule called Auto business rule for Assessments, which monitors the Table selected for the metric type. When someone adds a record that meets the metric type conditions, this business rule generates an assessable record. If someone changes the metric type's Table or conditions, the Create Business Rule on Remote table business rule updates the automatic business rule script to reflect the changes.
-   Business rule called Auto deletion rule for Assessments, which prevents users from deleting a record on the metric type's Table if the record is associated to metric or category results. If the record has no associated results and a user deletes it, this business rule deletes any associated assessable records.

 The Create Business Rule on Remote table business rule generates automatic business rules only for metric types with Evaluation method set to Assessment.

</td></tr><tr><td>

Create Scheduled Job

</td><td>

Assessment Metric Type \[asmt\_metric\_type\]

</td><td>

Assessments: Generates a scheduled job for the creation of assessment components if either of these conditions is met:-   Someone creates a new metric type with the schedule type set to **Scheduled**.
-   The schedule type changes from **On demand** to **Scheduled**.

 Surveys: Generates a scheduled job for the creation of survey components if the schedule period for a survey definition is set to Daily, Weekly, Monthly, or Yearly.

</td></tr><tr><td>

Create Survey Records

</td><td>

Assessment Metric Type \[asmt\_metric\_type\]

</td><td>

Generates various records and populates certain fields on those records when someone creates a new survey definition, which is a metric type with Evaluation method set to Survey. More specifically, this business rule generates a survey category and assessable record, both associated to the survey definition.

</td></tr><tr><td>

Create UI Action on Remote table

</td><td>

Assessment Metric Type \[asmt\_metric\_type\]

</td><td>

Reserved for future use.

</td></tr><tr><td>

decision\_matrix\_axis

</td><td>

Global \[global\]

</td><td>

Limits available categories for X- and Y-axes to those that belong to the type if there is a metric type specified on the Decision Matrix form.

</td></tr><tr><td>

Delete Live Feed Group

</td><td>

Assessable Record \[asmt\_assessable\_record\]

</td><td>

Deletes the assessable record's Live Feed group, if there is one, when an assessment administrator deletes an assessable record.

</td></tr><tr><td>

delete related users

</td><td>

Category Assessable Records \[asmt\_m2m\_category\_assessment\]

</td><td>

Deletes any stakeholders for the assessable record and category when an assessment administrator disassociates a category from an assessable record.

</td></tr><tr><td>

Do not allow category to change

</td><td>

Assessment Metric \[asmt\_metric\]

</td><td>

Prevents the **Category** field from being changed if there are any conditional question dependencies related to the current record.

</td></tr><tr><td>

Do not allow datatype to change

</td><td>

Assessment Metric \[asmt\_metric\]

</td><td>

Prevents the **Data type** and **Template** fields from being changed if there are any conditional questions that depend on the current record.

</td></tr><tr><td>

Ensure Types Match

</td><td>

Assessment Metric \[asmt\_metric\]

</td><td>

Sets the type of a metric to the type of the associated category.

</td></tr><tr><td>

Ensure types match

</td><td>

Assessment Stakeholders \[asmt\_m2m\_stakeholder\]

</td><td>

Ensures that users can only create a stakeholder from a category user and assessable record of the same type.

</td></tr><tr><td>

Ensure types match

</td><td>

Category Assessable Records \[asmt\_m2m\_category\_assessment\]

</td><td>

Prevents users from associating categories of one type to an assessable record of a different type.

</td></tr><tr><td>

Evaluate filters

</td><td>

Assessable Record \[asmt\_assessable\_record\]

</td><td>

Performs the following after the system generates a new assessable record:-   Checks all filter conditions for categories in the type.
-   Automatically associates the new assessable record to all categories for which it meets the category filter conditions.

</td></tr><tr><td>

Generate assessment trigger condition

</td><td>

Trigger Condition \[asmt\_condition\]

</td><td>

Generates a business rule that the survey or assessment trigger condition uses to send surveys or assessments.

</td></tr><tr><td>

getStakeholders

</td><td>

Global \[global\]

</td><td>

Ensures that only category users for categories associated with the assessable record are available on the Assessable Record form when users edit the Category users related list.

</td></tr><tr><td>

Link assessable record and category

</td><td>

Metric Category \[asmt\_metric\_category\]

</td><td>

Sets these hidden fields as follows for a newly created survey category:-   Table: Assessment Metric Type \[asmt\_metric\_type\]
-   Filter: &lt;sys\_id of the survey definition the new survey category is associated with&gt;

</td></tr><tr><td>

Live Feed Group

</td><td>

Assessable Record \[asmt\_assessable\_record\]

</td><td>

Creates a Live Feed group for the assessable record, if one doesn't exist, when the record is saved with the **Live feed** option selected. If the check box is then cleared and the record saved, this business rule deletes an existing Live Feed group.

</td></tr><tr><td>

Metric domain matches category

</td><td>

Assessment Metric \[asmt\_metric\]

</td><td>

Ensures that all new metrics are in the same domain as the category to which they belong. This rule is a special requirement of assessment domain separation, that all records must be in the same domain.

</td></tr><tr><td>

Notify assessment user

</td><td>

Assessment Instance \[asmt\_assessment\_instance\]

</td><td>

Starts a workflow that sends an email notification to the assigned user when an assessment instance changes to the **Ready** state or the user to which it is assigned changes. The workflow generates other assessment email notifications at later stages.

</td></tr><tr><td>

Prevent recursive dependencies

</td><td>

Assessment Metric \[asmt\_metric\]

</td><td>

Prevents the **Depends on** field from being set in a way that creates a recursive conditional question dependency.

</td></tr><tr><td>

Publish Survey

</td><td>

Assessment Metric Type \[asmt\_metric\_type\]

</td><td>

Generates survey instances and assigns them to the associated survey users when the survey definition state changes from **Draft** to **Published**.

</td></tr><tr><td>

Remove auto create Business Rules

</td><td>

Assessment Metric Type \[asmt\_metric\_type\]

</td><td>

Deletes the automatically created business rule for a metric type when an assessment administrator deletes that metric type.

</td></tr><tr><td>

Remove auto create UI actions

</td><td>

Assessment Metric Type \[asmt\_metric\_type\]

</td><td>

Reserved for future use.

</td></tr><tr><td>

Remove auto created business rule

</td><td>

Survey Trigger Condition \[asmt\_condition\]

</td><td>

Deletes the automatically created business rule when someone deletes the survey trigger condition.

</td></tr><tr><td>

Remove Scheduled Job

</td><td>

Assessment Metric Type \[asmt\_metric\_type\]

</td><td>

Assessments: Deletes the scheduled job for a metric type if either of these conditions is met:-   Someone deletes the metric type.
-   Someone changes the schedule type from **Scheduled** to **On demand**.

 Surveys: Deletes the scheduled job for a survey definition if the schedule period is set to Only Once or No Limit.

</td></tr><tr><td>

Reset Min/Max for metric

</td><td>

Assessment Metric Definition \[asmt\_metric\_definition\]

</td><td>

Updates the **Min** and **Max** fields for metrics and survey questions based on the metric definition value.

</td></tr><tr><td>

Set Domain for M2M Cat Assessable Recs

</td><td>

Category Assessable Records \[asmt\_m2m\_category\_assessment\]

</td><td>

Ensures that assessable records are only associated to categories in the same domain. This rule is a special requirement of assessment domain separation, that all records must be in the same domain.

</td></tr><tr><td>

Set Domain for M2M Category Users

</td><td>

Assessment Category User \[asmt\_m2m\_category\_user\]

</td><td>

Ensures that users are only linked to categories in the same domain. This is a special requirement of assessment domain separation, that all records must be in the same domain.

</td></tr><tr><td>

Set Domain for M2M Stakeholders

</td><td>

Assessment Stakeholders \[asmt\_m2m\_stakeholder\]

</td><td>

Ensures that assessable records are only linked to category users in the same domain. This is a special requirement of assessment domain separation, that all records must be in the same domain.

</td></tr><tr><td>

Set scratchpad fields

</td><td>

Assessment Metric Type \[asmt\_metric\_type\]

</td><td>

Caches field values for use by other scripts that run on the Assessment Metric Type form.

</td></tr><tr><td>

Store view type

</td><td>

Metric Category \[asmt\_metric\_category\]

</td><td>

Ensures that the **Type** field only allows users to select metric types used for assessments.

</td></tr><tr><td>

Synchronize category survey users

</td><td>

Assessment Category User \[asmt\_m2m\_category\_user\]

</td><td>

Ensures that the same users are associated with all of a survey's categories.

</td></tr><tr><td>

Synchronize survey users and stakeholder.

</td><td>

Metric Category \[asmt\_metric\_category\]

</td><td>

Adds all users associated with a survey's existing categories to any newly created category for that survey.

</td></tr><tr><td>

Update Category Count

</td><td>

Assessment Metric \[asmt\_metric\]

</td><td>

Updates the value in the **Total metrics** field on the Metric Category form when metrics are added to and deleted from the category.

</td></tr><tr><td>

Update records that match filter

</td><td>

Metric Category \[asmt\_metric\_category\]

</td><td>

Automatically performs these tasks when an assessment administrator edits the **Filter** field:-   Associates the category to assessable records that meet the filter conditions.
-   Disassociates the category from assessable records that don't meet the filter conditions.

 The Assessable records related list reflects these changes when the record is saved.

</td></tr><tr><td>

Update scheduled job on schedule change

</td><td>

Assessment Metric Type \[asmt\_metric\_type\]

</td><td>

Updates the survey creation scheduled job to reflect schedule period changes.

</td></tr><tr><td>

Validate mandatory and not applicable

</td><td>

Assessment Metric \[asmt\_metric\]

</td><td>

Sets the **Mandatory** and **Allow not applicable** fields to **false** if the metric method is Script. If the metric data type is Percentage, the business rule sets the **Allow not applicable** field to **false**.

</td></tr><tr><td>

Verify min/max

</td><td>

Assessment Metric \[asmt\_metric\]

</td><td>

Ensures that the Min is greater than or equal to zero and less than the Max. Sets the Min to 0 and the Max to 1 if the data type is **Checkbox** or **Yes/No**.

</td></tr><tr><td>

Verify value

</td><td>

Assessment Template Definition \[asmt\_template\_definition\]

</td><td>

Ensures that the metric template definition Value is:-   Greater than or equal to zero.
-   Different from the Value for all other metric template definitions related to the template.

</td></tr><tr><td>

Verify value

</td><td>

Assessment Metric Definition \[asmt\_metric\_definition\]

</td><td>

Ensures that users can only enter a metric definition Value greater than or equal to zero. Ensures that the metric definition value is different from the Value for all other metric definitions related to the metric.

</td></tr></tbody>
</table>**Parent Topic:**[Assessments and Surveys](../concept/assessments-surveys-landing-page.md)

