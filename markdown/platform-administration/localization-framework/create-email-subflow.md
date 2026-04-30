---
title: Create a custom email subflow
description: Create an email subflow according to your requirements. You can then select this subflow to define translation preferences for a language.
locale: en-US
release: zurich
product: Localization Framework
classification: localization-framework
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Localization Framework settings, Configure the Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer]
---

# Create a custom email subflow

Create an email subflow according to your requirements. You can then select this subflow to define translation preferences for a language.

## Before you begin

Roles required: localization\_admin and flow\_designer

## About this task

The Localization Framework provides a default email subflow that you can customize.

Copy the existing email subflow configured for the Localization Framework and then customize it. Publish the customized subflow so that it is available for selection when setting up the translation preference for a language. For more information, see [Create a subflow](https://www.servicenow.com/docs/access?context=create-subflow&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  In the Workflow Studio window, click **Subflows**.

3.  Click **Send LF Email for Translation** subflow.

    The Send LF Email for Translation subflow opens in the Workflow Studio in read-only format. The inputs in this subflow are described in the following table:

    |Name|Description|Type|
    |----|-----------|----|
    |lftask\_record|Associated Localization Framework task record.|Reference.Localization Task \[sn\_lf\_insight\]|
    |attachment\_record|Contains a file related to the LFTASK that can be sent via Email for translation.|Reference.Attachment|
    |send\_to|Contains email addresses of the recipients to send the LF task file.|String|
    |source\_language|Language from which the localization task was created.|String|
    |target\_language|Language into which the content of the localization task gets translated into.|String|

4.  In the subflow header, click the more actions icon ![More actions](../image/more-actions-icon.png) and select **Copy subflow.**

5.  In the **New subflow name** field, enter the name of the new subflow.

6.  To limit the application scope of the subflow, in the **Application** field, select the required application, otherwise select **Global**.

7.  Click **Copy**.

    The new subflow is created and opens in the subflow designer editor. The inputs from the copied subflow appear.

    **Note:** Inputs are fixed and cannot be edited.

8.  In the Actions section, click **Send Email**.

    This expands the Send Email section. The fields in the Send Email section are described below:

<table id="table_xf1_5yx_xnb"><thead><tr><th>

Field name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action

</td><td>

Name of the action.Default: **Send Email**.

</td></tr><tr><td>

Target Record

</td><td>

Associated Localization Framework task record

</td></tr><tr><td>

Table

</td><td>

Name of the table where the localization task resides.

</td></tr><tr><td>

Include Watermark

</td><td>

Adds a watermark in the file associated with the localization task.

</td></tr><tr><td>

To

</td><td>

Contains email addresses of the recipients who should be addressed directly.

</td></tr><tr><td>

CC

</td><td>

Contains email addresses of the recipients who should see the list of recipients directly addressed in the email.

</td></tr><tr><td>

BCC

</td><td>

Contains email addresses of the recipients who are copied on the email but not displayed in the email.

</td></tr><tr><td>

Subject

</td><td>

The text about the email that its recipients can see.

</td></tr><tr><td>

Body

</td><td>

The text message about the localization task being sent for translation.

</td></tr></tbody>
</table>9.  Click **Done**, when you have modified the fields as per your requirement.

10. Click **Copy Attachment**.

    The Copy Attachment action expands. The fields in the Copy Attachment section are described below:

<table id="table_gss_rdy_xnb"><thead><tr><th>

Field name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action

</td><td>

Name of the action.Copy Attachment is displayed by default.

</td></tr><tr><td>

Source Attachment Record \[Attachment\]

</td><td>

Translatable content file of the localization task.

</td></tr><tr><td>

Target Record

</td><td>

Represents the target record in the email.

</td></tr><tr><td>

Table

</td><td>

Represents the email table.

</td></tr></tbody>
</table>11. Click **Save**, to save the subflow in draft status.

12. Click **Publish**.


## Result

Use the published subflow to define the translation preference for a language.

**Parent Topic:**[Localization Framework settings](../concept/localization-settings.md)

