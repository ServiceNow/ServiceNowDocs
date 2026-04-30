---
title: Available question types in Creator Studio
description: Build apps using different types of questions on a form in Creator Studio.
locale: en-US
release: zurich
product: Creator Studio
classification: creator-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Reference, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Available question types in Creator Studio

Build apps using different types of questions on a form in Creator Studio.

You get to pick the questions to ask requesters. Creator Studio provides two types of questions you can ask:

-   **General questions** are where you give requesters an empty box to write a short answer \(think name or email\) or a list of choices to pick from \(like a dropdown menu or those little circles you fill in\).
-   **Reference-based questions** are where you provide a list of choices that you define in a table.

The type of question you select from the **Content type** field in the Question details panel changes the question's settings that appear.

## Types of general questions

<table id="table_j3t_kkr_f1c"><thead><tr><th>

Content type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short answer \(Single-line text\)

</td><td>

Single-line question.

</td></tr><tr><td>

Multi-line text

</td><td>

Longer option that provides space for a question multiple lines in length.

</td></tr><tr><td>

Dropdown

</td><td>

Question with a list of pre-defined answers that users select from a dropdown menu. Users can select only one answer.

</td></tr><tr><td>

Radio button

</td><td>

Question with list of pre-defined answers that users select from radio buttons. Users can select only one answer.

</td></tr><tr><td>

Check box

</td><td>

True or false question that users answer by selecting the relevant check box.**Note:** If you put two checkbox questions side-by-side on a form, they make a section. You can't add other types of questions to that section.

</td></tr><tr><td>

Yes/No

</td><td>

Question where users select Yes or No as their answer.

</td></tr><tr><td>

Date

</td><td>

Question where the answer is a date that users must select from a calendar.

</td></tr><tr><td>

Date and time

</td><td>

Question where the answer is a date and time that users must specify.

</td></tr><tr><td>

Question set

</td><td>

Preconfigured questions that you can't change.Admins create question sets in Service Catalog. For more information, see [Service catalog variable sets](https://www.servicenow.com/docs/access?context=c_ServiceCatalogVariableSets&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

**Note:**

-   You can't change an existing question into a question set. To include a question set on a form, you must newly add it to the form.
-   If you put two checkbox questions side-by-side on a form, they make a section. You can't add other types of questions to that section.

</td></tr><tr><td>

Attachment

</td><td>

Question where users add an attachment.**Note:** The **Attachment** question differs from the **Add attachment** option for the overall form. You can use the **Add attachment** question to include in dynamic behavior, for example appearing when a user answers a **Photograph on badge?** question with `Yes`, enabling them to upload a headshot. For more information on dynamic behavior, see [Make a form change based on responses in Creator Studio](../task/creator-studio-dynamic-behavior.md).

</td></tr><tr><td>

Duration

</td><td>

Question where users specify a length of time.When you add a **Duration** question, you then specify the **Days**, **Hours**, **Minutes**, and **Seconds** that an event will last.

**Note:** You can also add duration for dynamic behavior questions. For more information, see [Make a form change based on responses in Creator Studio](../task/creator-studio-dynamic-behavior.md).

</td></tr></tbody>
</table>## Types of reference-based question types

Reference-based questions pull their possible values from the table that you must designate as the **Source table**.

<table id="table_g33_fjl_k1c"><thead><tr><th>

Content type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Record choices

</td><td>

Question where the answers are retrieved from an additional specified table when the filter conditions, which you must also define, are met.Use this question on a form that references data from another form, such as a form that uses the Incident table. "Choose the related incident" is an example Record choices question, which could use a filtered list of incidents as possible answer selections.

If you have a Record choices question on a form, you'll see an **Add auto-fill** option when you configure other questions on the form. Select the **Add auto-fill** option to choose a value from the Record choices question's table to automatically populate the question's answer.

For example, a form can enable someone to select a user for the **Choose the gift box recipient** field, which retrieves its values from the User table. An additional **Preferred name** field can be automatically populated from the **First name** field of the User table selection, but then edited if someone prefers a nickname.

</td></tr><tr><td>

Field choices

</td><td>

Question where the answers are retrieved from a field on the specified table when the filter conditions, which you must also define, are met.For example, you could create a Field choices question for a table with a "Country" field, which the user could then use to select their country.

</td></tr><tr><td>

Multi-select

</td><td>

Question where users can select multiple answers that are retrieved from the specified table when the filter conditions, which you must also define, are met.Use this question on a form that references data from multiple other forms, such as a form that pulls answers from multiple separate Incident tables.

</td></tr></tbody>
</table>## Question details

Depending on the type of question you add to a form, you must specify some of the following details.

<table id="table_h1c_k53_j1c"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Available for

</th></tr></thead><tbody><tr><td>

Question label

</td><td>

Question or statement that says what the question is asking.

</td><td>

All question types

</td></tr><tr><td>

Help text

</td><td>

Additional information that appears as a tooltip to guide the user when they hover over the information icon.

</td><td>

All question types

</td></tr><tr><td>

Show questions on form

</td><td>

Hide the question from the form by leaving this option unselected.You can use this option to associate data with the form behind the scenes by adding it to the app's table.

</td><td>

All question types

</td></tr><tr><td>

Mark as required

</td><td>

Option to make the question required before the user can submit the form.

</td><td>

All question types

</td></tr><tr><td>

Mark as read-only

</td><td>

Option to make the question read-only.For example, if you don't automatically pull the user's role into the form's table, you could create a single-line text question where the default value is their role \(such as Sales\) and then hide it. You could even hide the question from the form to make the data exchange invisible to the user.

</td><td>

All question types

</td></tr><tr><td>

Default value

</td><td>

Value that's auto-populated in the question’s answer when the form is opened.For reference-based questions where you designate a source table, you must use an asterisk \(`*`\) as a wildcard when searching for values in the **Default value** field.

For example, if the question references the User table and you're looking for Abel Tuter, entering `Tuter` won't find that user but entering `*Tuter` will.

</td><td>

All question types

</td></tr><tr><td>

Choices

</td><td>

Customizable answers to the question, which you can drag to rearrange in a new order.

</td><td>

-   Dropdown
-   Radio button

</td></tr><tr><td>

Include "None" as a choice

</td><td>

Option to include **None** as a possible answer to the question.

</td><td>

-   Dropdown
-   Radio button
-   Field choices

</td></tr><tr><td>

Default to the first choice

</td><td>

Option to display the first choice as the possible answer when the user sees the question.

</td><td>

Radio button

</td></tr><tr><td>

Source table

</td><td>

Table location that provides data for answers to the question.

</td><td>

-   Record choices
-   Field choices
-   Multi-select

</td></tr><tr><td>

Field

</td><td>

Field in the specified source table that possible answers are retrieved from.

</td><td>

Field choices

</td></tr><tr><td>

Filter conditions

</td><td>

Conditions that must be met to view certain choices. Select **Add condition** and use the condition builder to create the filter. For more information, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

</td><td>

-   Record choices
-   Field choices
-   Multi-select

</td></tr></tbody>
</table>**Parent Topic:**[Creator Studio reference](creator-studio-reference.md)

