---
title: Create a risk assessment using the Risk Assessment Designer
description: Use the Risk Assessment Designer to create and edit metric types, use different metric types for different risks, select multiple respondents for a risk assessment, as well as change scoring parameters. The Question Bank offers a library of questions for various categories, so you do not have to build each questionnaire from scratch.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Assess risks, Use, Risk Management, Governance, Risk, and Compliance]
---

# Create a risk assessment using the Risk Assessment Designer

Use the Risk Assessment Designer to create and edit metric types, use different metric types for different risks, select multiple respondents for a risk assessment, as well as change scoring parameters. The Question Bank offers a library of questions for various categories, so you do not have to build each questionnaire from scratch.

## Before you begin

Role required: sn\_risk.asmt\_creator, sn\_risk.manager

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Administration** &gt; **Assessment Types**.

2.  Click **Risk Assessment Designer**.

    The designer contains the following elements:

    |Element|Description|
    |-------|-----------|
    |Controls|Supported question data types are available in the Controls palette. Drag a control onto the designer canvas to create a question of that type.|
    |Questions|A library of questions for various categories, so you do not have to build each questionnaire from scratch.|
    |Categories|New assessment open in the **Design** view. The questionnaire **Name** field appears above the first category in the canvas. A blank question field appears in the category container.|

3.  Enter a name in the **Name** field.

4.  Drag a control onto the designer canvas to create a question of that type.

    |Data type|Description|Scored|
    |---------|-----------|------|
    |Attachment|Question with a Manage Attachments icon that allows users to attach one or more files.|Y|
    |Boolean|Question with a check box or a **Yes/No** list for user responses.| |
    |Choice|List of predefined options. For more information, see the definition for **Choices**.|Y|
    |Date|Date field.|N|
    |Date/Time|Date and time field.|N|
    |Number|Number field with predefined minimum and maximum values. The default is 1-10.|N|
    |Percentage|Percentage field with a prescribed range.|N|
    |Scale|Predefined Likert scale. Answer options appear as radio buttons.|Y|
    |Numeric Scale|Selectable number scale. The default is 1-5. Answer options appear as radio buttons.|Y|
    |String|Single or multi-line text field.|N|
    |Template|Choice list of templates that provide a predefined scale of options.|Y|
    |Reference|Choice list of fields from a specified reference table. This data type does not support reference qualifiers.| |

    **Note:** Set the correct answer for the metric that you want to be scored. Scored metrics determine the compliance status of the risk.

5.  Click one of the following tabs to change the view in the canvas.

<table id="choicetable_lvf_45v_lz"><tbody><tr><td id="d160680e347">

**Design**

</td><td>

Add categories and questions, and configure the properties of each. This is the default view of the canvas when you open the designer.

</td></tr><tr><td id="d160680e356">

**Configuration**

</td><td>

Create introductions and end notes for attestations, and select a signature.

</td></tr><tr><td id="d160680e365">

**Availability**

</td><td>

Select the recipients for each category in the attestation.

</td></tr></tbody>
</table>6.  Point to the menu icon in the upper right of the designer to select one of the following options.

    **Note:** The availability of each option depends on the status of the assessment that is opened in the designer.

<table id="choicetable_mvf_45v_lz"><tbody><tr><td id="d160680e390">

**Save**

</td><td>

Save the current assessment.

</td></tr><tr><td id="d160680e399">

**Preview**

</td><td>

Display a preview to the selected recipients.

</td></tr><tr><td id="d160680e408">

**Publish**

</td><td>

Distributes the assessment to the selected recipients.

</td></tr><tr><td id="d160680e417">

**Save and Publish**

</td><td>

Saves and distributes the assessment in one step.

</td></tr><tr><td id="d160680e426">

**New Attestation**

</td><td>

Opens a fresh canvas for a new assessment.

</td></tr><tr><td id="d160680e436">

**Load Attestation**

</td><td>

Opens a list of existing assessment that you can select and edit.

</td></tr></tbody>
</table>    Unlike other types of assessments, risk assessments do not appear in the **Self-Service** &gt; **My assessments &amp; surveys** module, because hundreds of control attestations could be generated at once. Instead,risk assessments are shown as a list in the **Risk** &gt; **Risk Register** &gt; **My Assessments** and **Risk** &gt; **Risk Register** &gt; **All Assessments** module.


**Parent Topic:**[Assess risks](../concept/assess-risk-old-way.md)

