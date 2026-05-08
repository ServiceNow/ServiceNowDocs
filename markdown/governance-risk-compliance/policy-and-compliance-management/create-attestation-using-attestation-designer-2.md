---
title: Manage control attestations
description: Attestations are surveys that gather evidence to prove that a control is implemented. Attestations document how the control is measured. This method is frequently used during the Draft and Monitor state.Use the Attestation Designer to create and edit metric types. Use different metric types for different controls. Select multiple respondents for an attestation, as well as change scoring parameters.Rather than using the default GRC attestation type, the compliance manager can create a new set of questions for each control objective.Policy and Compliance Management and Risk Management offer two methods for consolidating attestations and risk assessments into groups that help eliminate the task of providing repetitive responses for similar assessments. You can provide the same evidence to the grouped assessments or respond to individual assessments in the same user interface.Policy and Compliance Management and Risk Management offer two methods for consolidating attestations and risk assessments into groups that help eliminate the task of providing repetitive responses for similar assessments. You can provide the same evidence to the grouped assessments or respond to individual assessments in the same user interface.You can optionally define additional grouping criteria if the default criteria does not meet your needs.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Mandatory setup, Implement, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Manage control attestations

Attestations are surveys that gather evidence to prove that a control is implemented. Attestations document how the control is measured. This method is frequently used during the Draft and Monitor state.

The attestation designer provides a single interface that users can use to create and edit attestations, as well as change scoring parameters. The question bank offers a library of questions for various categories, so you do not have to build each questionnaire from scratch.

**Note:** To know more about control attestations, see [An overview of policy life cycle in Policy and Compliance Management](pc-policy-life-cycle-ovrvw.md).

Users can create multiple attestation types and set their control objectives to different attestations. A sample attestation called **GRC Attestation** is also provided as the default attestation, which is composed of the following simple questions:

By default, **GRC Attestation** is used for controls and provides the following assessment questions:

-   Is this control implemented?
-   Attach evidence
-   Explain

**My Attestations** is in the **Controls** section of the Policy and Compliance application and contains active attestations for which you are the respondent. The attestations appear in a list with a single attestation record per control.

**My Grouped Attestations** contains attestations that you have grouped to eliminate the task of providing repetitive responses for similar assessments.

**All Attestations** is contained in the **Controls** section of the Policy and Compliance application and contains all active attestations.

Compliance managers can create attestation types containing different types of questions to fit their needs. See [Create a control attestation using the Attestation Designer](c_Attestations.md#).

Compliance managers can create a new set of questions for each control objective. The Question Bank offers a library of questions for various categories, so you do not have to build each questionnaire from scratch. See [Create an attestation type](c_Attestations.md#).

## Attestation Designer

The attestation designer provides a single interface that users can use to create, and edit attestations, as well as change scoring parameters.

All attestation records are stored in assessment tables and displayed in Attestation views of those tables.

**Parent Topic:**[Classic UI for Policy and Control Management](using-policy-compliance-legacy-ui.md)

## Create a control attestation using the Attestation Designer

Use the Attestation Designer to create and edit metric types. Use different metric types for different controls. Select multiple respondents for an attestation, as well as change scoring parameters.

### Before you begin

Role required: sn\_compliance.attestation\_creator, sn\_compliance.manager, sn\_compliance.administrator

### Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Administration** &gt; **Attestation Types**.

2.  Click **Attestation Designer**.

    The designer contains the following elements:

    |Element|Description|
    |-------|-----------|
    |Controls|Supported question data types are available in the Controls palette. Drag a control onto the designer canvas to create a question of that type.|
    |Questions|A library of questions for various categories, so you do not have to build each questionnaire from scratch.|
    |Categories|New assessment opens in the **Design** view. The questionnaire **Name** field appears above the first category in the canvas. A blank question field appears in the category container.|

3.  Enter a name in the **Name** field.

4.  Drag a control onto the designer canvas to create a question of that type.

<table id="table_dgb_pvh_br"><thead><tr><th>

Data type

</th><th>

Description

</th><th>

Scored

</th></tr></thead><tbody><tr><td>

Attachment

</td><td>

Question with a Manage Attachments icon that allows users to attach one or more files.

</td><td>

N

</td></tr><tr><td>

Boolean

</td><td>

Question with a check box or a **Yes/No** list for user responses.

</td><td>

Y

</td></tr><tr><td>

Choice

</td><td>

List of predefined options. For more information, see the definition for **Choices**.

</td><td>

Y

</td></tr><tr><td>

Date

</td><td>

Date field.

</td><td>

N

</td></tr><tr><td>

Date/Time

</td><td>

Date and time field.

</td><td>

N

</td></tr><tr><td>

Number

</td><td>

Number field with predefined minimum and maximum values. The default is 1–10.

</td><td>

N

</td></tr><tr><td>

Percentage

</td><td>

Percentage field with a prescribed range.

</td><td>

N

</td></tr><tr><td>

Scale

</td><td>

Predefined Likert scale. Answer options appear as radio buttons.

</td><td>

Y

</td></tr><tr><td>

Numeric Scale

</td><td>

Selectable number scale. The default is 1–5. Answer options appear as radio buttons.

</td><td>

Y

</td></tr><tr><td>

String

</td><td>

Single or multi-line text field.

</td><td>

N

</td></tr><tr><td>

Template

</td><td>

Choice list of templates that provide a predefined scale of options. **Note:** It is important to assign a template to every attestation. This allows controls to be created automatically based on control objectives and entity types.

</td><td>

Y

</td></tr><tr><td>

Reference

</td><td>

Choice list of fields from a specified reference table. This data type does not support reference qualifiers.

</td><td>

N

</td></tr></tbody>
</table>    **Note:** Set the correct answer for the metric that you want to be scored. Scored metrics determine the compliance status of the controls.

5.  Point to the menu icon in the upper right of the Attestation Designer and select **New Attestation**.

    A fresh canvas opens for you to build a new attestation.

6.  To edit an existing attestation, point to the menu icon in the upper right of the Attestation Designer and select **Load Attestation**.

    You can modify questions, adjust scoring parameters, and change the scale factor. Save your changes when complete.

    **Note:** The availability of the New Attestation and Load Attestation options depend on the status of the attestation that is opened in the designer.

    Unlike other types of assessments, control attestations do not appear in the **Self-Service** &gt; **My assessments &amp; surveys** module, because many control attestations could be generated at once. Instead, controls attestations are shown as a list in the **Policy and Compliance** &gt; **Controls** &gt; **My Attestations** module and **All Attestations** module.


### What to do next

If you are implementing the [Policy and Compliance Management](../../grc-policy-compliance-implementation/task/policy-compliance-impl-checklist.md) software, return to the [Policy and Compliance Management setup checklist](../../grc-policy-compliance-implementation/task/policy-compliance-impl-checklist.md) and proceed to the next step.

**Parent Topic:**[Policy and Compliance Management mandatory setup](../../grc-policy-compliance-implementation/concept/policy-compliance-mandatory-setup.md)

## Create an attestation type

Rather than using the default **GRC attestation** type, the compliance manager can create a new set of questions for each control objective.

### Before you begin

Role required: sn\_compliance.attestation\_creator or sn\_compliance.manager or sn\_compliance-admin

### Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Administration** &gt; **Attestation Types**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the assessment type.|
    |Assessment duration|Length of time allowed from generation to completion of the assessment.|
    |Table|Table this assessment applies to.|
    |Scale factor|Scale value to use for all assessment results.|
    |Condition|Define specifics records from the table.|
    |Description|More details about the assessment.|
    |State|State of the assessment: **Draft** or **Published**|
    |Enforce condition|Option that indicates whether accessible records of this type that do not meet the conditions specified are deleted.|
    |Roles|Roles that have access to information about this metric type.|

4.  Click **Submit**.


## Group attestations using Same Response

Policy and Compliance Management and Risk Management offer two methods for consolidating attestations and risk assessments into groups that help eliminate the task of providing repetitive responses for similar assessments. You can provide the same evidence to the grouped assessments or respond to individual assessments in the same user interface.

### Before you begin

Role required: sn\_grc.business\_user, sn\_grc.business\_user\_lite

### About this task

When you consolidate control attestations using the Same Response feature, you can group attestations that contain a maximum of 1000 questions. When the attestation or risk assessment for the group is taken, all records in the group inherit the answers.

**Note:** To change the 1000-question limit, navigate to **All** &gt; **Policy and Compliance** &gt; **Administration** &gt; **GRC Properties** and modify the **sn\_grc.consolidated\_questions\_limit** property.

If you do not want your users to access to this capability, navigate to **All** &gt; **Policy and Compliance** &gt; **Administration** &gt; **GRC Properties**, and disable the **sn\_grc.enable\_consolidate\_asmt** property.

### Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Controls** &gt; **My Attestations**.

2.  Select the attestations you want to group.

3.  From the **Actions on selected rows** choice list, click **Group Assessments**.

    ![Group assessments](../image/group-assessments.png)

4.  In **Response Type**, select **Provide same response for all assessments**.

5.  Fill in the fields, as needed.

<table id="table_group_assessments"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Default criteria

</td><td>

This field defaults to **Metric Type**.

</td></tr><tr><td>

Additional criteria

</td><td>

You can optionally define additional grouping criteria:-   Category
-   Control Objective/Risk Statement
-   Entity
 You can also [define additional assessment criteria](c_Attestations.md#) options if the defaults do not meet your needs.

 **Note:** Using these grouping schemes makes sense if the grouped attestations contain multiple instances of the selected criteria. For example, if you selected a group of 20 attestations with 10 associated with one entity and the other 10 associated with a different entity, selecting **Entity** in this field causes two separate groups of attestations to be created. If, however, the group consists of 5 attestations associated with one entity and each of the other 15 attestations associated with different entities, only those 5 are grouped and the rest are ignored.

</td></tr><tr><td>

Preview

</td><td>

The **Preview** shows the number of attestations to be grouped. Depending on the **Additional criteria** you selected, the Preview may show multiple groups. If you want to see the attestations to be grouped, click the link that shows the number of attestations or risk assessments to be grouped.

</td></tr></tbody>
</table>6.  When you are satisfied with the attestations or risk assessments to be consolidated, click **Group**.

    A confirmation message displays, along with a link to the attestation group.

    ![Assessment created message](../image/message.png)

    **Note:** When attestation groups are created, you can view them by navigating to **Policy and Compliance** &gt; **Controls** &gt; **My Grouped Attestations**. If you open a grouped attestation, you have the option of removing one or more attestations from the group. This is achieved by selecting the ones you want removed, and selecting **Ungroup Assessment** from the **Actions on selected rows** choice list. If you remove attestations from a group to the point where there is only one attestation, the group is removed.

7.  When you are ready to take the assessment, click the link in the confirmation message or the attestation number in **My Grouped Attestations**.

    ![Assessment instances](../image/take_assessment.png)

8.  Click **Take assessment**.

9.  Complete the assessment like you would any other, and click **Submit**.

    All attestations in the group inherit the answers you provided and the state of each attestation in the group changes to **Complete**.


## Group attestations using Different Response

Policy and Compliance Management and Risk Management offer two methods for consolidating attestations and risk assessments into groups that help eliminate the task of providing repetitive responses for similar assessments. You can provide the same evidence to the grouped assessments or respond to individual assessments in the same user interface.

### Before you begin

Role required: sn\_grc.business\_user, sn\_grc.business\_user\_lite

### About this task

When you consolidate control attestations or risk assessments using the Different Response feature, you can group up attestations or risk assessments that contain a maximum of 150 questions. All of the questions appear in a single UI.

**Note:** To change the 1000-question limit, navigate to **Policy and Compliance** &gt; **Administration** &gt; **GRC Properties** and modify the **sn\_grc.grouped\_questions\_limit** property.

### Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Controls** &gt; **My Attestations**.

2.  Select the attestations you want to group.

3.  From the **Actions on selected rows** choice list, click **Group Assessments**.

    ![Group assessments](../image/group-assessments.png)

4.  In **Response Type**, select **Provide different response for each assessment**.

5.  Fill in the fields, as needed.

<table id="table_group_assessments"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Default criteria

</td><td>

This field defaults to **Metric Type**.

</td></tr><tr><td>

Additional criteria

</td><td>

You can optionally define additional grouping criteria:-   Category
-   Control Objective/Risk Statement
-   Entity
 You can also [define additional assessment criteria](c_Attestations.md#) options if the defaults do not meet your needs.

 **Note:** Using these grouping schemes makes sense if the grouped attestations contain multiple instances of the selected criteria. For example, if you selected a group of 20 attestations with 10 associated with one entity and the other 10 associated with a different entity, selecting **Entity** in this field causes two separate groups of attestations to be created. If, however, the group consists of 5 attestations associated with one entity and each of the other 15 attestations associated with different entities, only those 5 are grouped and the rest are ignored.

</td></tr><tr><td>

Preview

</td><td>

The **Preview** shows the number of attestations to be grouped. Depending on the **Additional criteria** you selected, the Preview may show multiple groups. If you want to see the attestations to be grouped, click the link that shows the number of attestations or risk assessments to be grouped.

</td></tr></tbody>
</table>6.  When you are satisfied with the attestations or risk assessments to be consolidated, click **Group**.

    A confirmation message displays, along with a link to the attestation group.

    ![Assessment created message](../image/message.png)

    **Note:** When attestation groups are created, you can view them by navigating to **Policy and Compliance** &gt; **Controls** &gt; **My Grouped Attestations**. If you open a grouped attestation, you have the option of removing one or more attestations from the group. This is achieved by selecting the ones you want removed, and selecting **Ungroup Assessment** from the **Actions on selected rows** choice list. If you remove attestations from a group to the point where there is only one attestation, the group is removed.

7.  When you are ready to take the assessment, click the link in the confirmation message or the attestation number in **My Grouped Attestations**.

    ![Assessment instances](../image/take_assessment.png)

8.  Click **Take assessment**.

    You see questionnaires for all of the selected attestations in the group.

9.  Complete the assessment for each of the attestations, and click **Submit**.


## Define assessment grouping criteria

You can optionally define additional grouping criteria if the default criteria does not meet your needs.

### Before you begin

Role required: sn\_compliance.admin, sn\_compliance.manager

### Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Administration** &gt; **Assessment Grouping Criteria**.

    ![Assessment grouping criteria](../image/assess-group-criteria.png)

2.  Click **New**.

    ![Create a new assessment grouping criteria record](../image/assess-group-criteria-new.png)

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the assessment grouping criteria.|
    |Field name|Select the field name from the Assessment Instance \[asmt\_assessment\_instance \]table.|
    |Active|Select to activate the grouping criteria.|

4.  Click **Submit**.


