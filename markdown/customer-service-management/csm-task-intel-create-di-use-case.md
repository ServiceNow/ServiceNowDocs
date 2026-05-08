---
title: Create a Document Intelligence use case
description: Create a use case that identifies the information to extract from email and case attachments and determines how users with CSM agent roles interact with the extracted values in the Document Intelligence workspace.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Configure, Task Intelligence for Customer Service, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Create a Document Intelligence use case

Create a use case that identifies the information to extract from email and case attachments and determines how users with CSM agent roles interact with the extracted values in the Document Intelligence workspace.

-   **Before you begin**

    Role required: sn\_csm\_ml\_task.ti\_analyst, sn\_csm\_ml\_task.ti\_admin

-   **About this task**

    A use case contains the list of fields to extract from attachments and a mapping of those fields to fields in the Case table or a case type table. It also contains an extraction mode that controls how the values for the extracted fields are added to the case.

    Use cases include the following information.

    |Use case information|Description|
    |--------------------|-----------|
    |Fields|Configure the list of fields to predict for a use case. A field is a single piece of information to extract from a document. For example, the date on a document.|
    |Document tasks|Create a document task and include attachments that are used to train the Document Intelligence model to identify the correct information.|
    |Integrations|Select conditions for a use case that tell the Document Intelligence feature when to run.|

-   **Prerequisite**

    -   Activate Task Intelligence for Customer Service \(com.snc.csm\_ml\_task\).
    -   Activate Document Intelligence Admin \(com.snc.docintel\_admin\).
    For more information, see [Configure Document Intelligence for Customer Service](csm-doc-intel-configuring-.md).


## Access the DocIntel Admin experience

1.  Navigate to **All** &gt; **Task Intelligence for Customer Service** &gt; **Setup** to open the Task Intelligence Admin Console.
2.  In the Explore related applications section of the console, select **Open DocIntel** in the Document Intelligence card to open the DocIntel Admin experience.

## Create a use case

Create a use case to identify a document or set of documents to be processed together in Document Intelligence. With Document Intelligence for Customer Service, the [Use Cases list](csm-document-intelligence.md#section_cyk_n1r_fwb) in the DocIntel Admin experience uses a default filter with an OR condition to show use cases for:

-   Application = Task Intelligence for Customer service -or-
-   MLUC ID = MLUC CSM-00003

To create a use case:

1.  Select **Use Cases** in the DocIntel Admin header.
2.  Select **New use case** in the Use Cases list.
3.  In the Define a new use case pop-up window, enter the following information.

<table id="table_trk_1dg_2wb"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the use case.

</td></tr><tr><td>

Location for the extracted data

</td><td>

The table that contains the records to be automatically populated with data extracted from attachments.Set this field to the case or case type that is relevant to your use case.

</td></tr><tr><td>

Extraction mode set by default

</td><td>

The extraction mode determines how the results are displayed to agents in the Document Intelligence workspace.The DocIntel Admin starts by showing the results for each use case as recommendations.

</td></tr></tbody>
</table>4.  Select **Save** to add the use case to the Use Cases list.

## Define the fields to extract

After creating a use case, select the fields that you want to extract. You can select one or more fields for a use case. These fields can be of the text or Boolean type.

**Note:** The fields to be extracted should already exist in the use case target table. If the fields do not exist in the target table, add them to the table and then complete this step.

1.  Select a use case in the Use Cases list.
2.  Select the Fields tab.

    This tab lists the fields that have been selected for extraction for the use case.

3.  Select **Define your fields**.

    If you have already defined one or more fields and you want to add another field, select **New field**.

4.  Fill in the fields in the Define a new field pop-up window.

<table id="table_tsh_4mb_fwb"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Use case

</td><td>

\[Read only\] The use case associated with this field record.

</td></tr><tr><td>

Field Name

</td><td>

The display name of the field to extract as it appears in the Document Intelligence workspace.

</td></tr><tr><td>

Field Type

</td><td>

The type of field \(for example, a text field or a check box option\).Field type is read-only if you add this field to a field group. The field type is whatever is designated for the group.

Some field types convert the extracted value into a standard format. See Data normalization.

</td></tr><tr><td>

Is field required

</td><td>

\[Text and number fields only\] Required fields can’t be left empty or unreviewed.

</td></tr><tr><td>

Add field

</td><td>

Select the field group that you want to add the field to.

</td></tr><tr><td>

Target Table

</td><td>

\[Read only\] The table that stores the document processing results for this use case.

</td></tr><tr><td>

Target Field

</td><td>

Field on the target table you want to align this field with. Used for interation.**Note:** You must select a use case with a target table.

</td></tr><tr><td>

Define multiple fields

</td><td>

If you’re adding more than one field to the use case, enable this check box to keep the pop-up window displayed on the screen.

</td></tr></tbody>
</table>5.  Select **Add field**.

    The system adds the field definition to the Fields list.


## Create a document task

Document tasks include attached documents that are used to train the model to identify and extract the correct information.

1.  Select a use case in the Use Cases list.
2.  Select the Document tasks tab.

    This tab lists the tasks that have been created for the use case.

3.  Select **Create a document task**.

    If you have already created one or more tasks and you want to add another task, select **New document task**.

4.  In the Create the document task pop-up window, enter a **Document task name**.
5.  Select **+Add File** to add one or more attachments.
6.  Select the file and then select **Open**.
7.  In the Upload a file pop-up window, select **Upload**.
8.  In the Create the document task pop-up window, select **Add Extraction**.

    The system adds the task to the Document Tasks list and Document Intelligence begins the data extraction process, which can take a short time to complete.

    -   When the extraction process is complete, the **Is Processed** field is set to true.
    -   When the values have been extracted from the document, the **Status** field is set to Done.
9.  Open the task and select **Open in Document Intelligence** to view the task in the Document Intelligence Workspace.
10. Train the extracted fields to identify the correct values.
    1.  If a field value is correct: put your cursor in the field and press Return to confirm the value.
    2.  If a field value is missing: select the value from the list and press Return to confirm the value.
    3.  If a field value is incorrect: delete the incorrect value and type the first few characters of the correct value. When the correct value appears in the list, select it and then press Return.
    4.  If a field value is incorrect and the correct value does not appear on the image, select Missing in the document from the list.
    5.  Select **Submit**.

## Create an integration

Select conditions for a use case that tell the Document Intelligence feature when to run.

You can create one or more integrations for a use case. If a use case has more than one Integration, the system uses the latest one at run time.

**Note:** When creating an integration, make sure that the **Create Flow** check box remains unchecked.

1.  Select a use case in the Use Cases list.
2.  Select the Integrations tab.

    This tab lists the integrations that have been created for the use case.

3.  Select **Set up your first integration**.

    If you have already created one or more integrations, select **Add integration**.

4.  In the Create Integration pop-up window, enter a name for the integration.
5.  Use the condition builder to select conditions that tell the Document Intelligence feature when to predict values.

    At run time, the system identifies the right task definition based on these filters. The first active task definition that matches the filters for the case or case type is selected.

6.  Select **Save**.

## Set general Document Intelligence features

General settings determine how the Document Intelligence feature displays information to agents. General settings apply to all use cases.

1.  Select **Settings** in the DocIntel Admin header.
2.  Enable or disable the **Exact match option**. When enabled, Document Intelligence displays only the candidate values that exactly match what the agent types.
3.  Enable or disable the **Candidate score** to display confidence scores for each recommendation.
4.  Select a layout for the **Side panels**.
5.  Set the **Default width of the extraction panel**.
6.  Set the **Default width of the thumbnail panel**.
7.  Select the **Default document fit for the image panel**.

For more information about the general settings, see Configure Document Intelligence.

## Configure the data extraction mode

The extraction mode determines how the Document Intelligence workspace handles the extracted values. Two extraction modes are available: Recommendation and Autofill.

-   Recommendation mode provides recommendations for the extracted fields in the Document Intelligence workspace. Agents can choose the recommended value for a field or manually enter a value.
-   Autofill mode adds values to the fields in the Document Intelligence workspace if the extraction confidence is higher than the **Autofill Threshold** value.

1.  Select **Settings** in the DocIntel Admin header.
2.  In the left column of the Settings page, expand the Use Cases list and select a use case.
3.  Select **Extraction Mode**.
4.  To use the Recommendation mode, enable **Mode 1: Recommendation**.

    ![DocIntel Admin Recommendation data extraction mode](../image/doc-intel-admin-extraction-mode-1.png)

5.  To use the Autofill mode, enable **Mode 2: Autofill**.

    1.  Enter a percentage value in the **Set the Autofill Threshold** field.
    2.  Enter a percentage value in the **Set the Warning Threshold** field.
    ![DocIntel Admin Autofill data extraction mode](../image/doc-intel-admin-extraction-mode-2.png)


## Configure the agent verification setting

By default, agents review and verify the fields with values that are extracted from attached documents. You can enable Straight Through Processing to automatically populate these fields with extracted values. When enabled, agents only review and verify the extraction tasks if the confidence score of all field values is below the set threshold.

1.  In the left column of the Settings page, expand the Use Cases list and select a use case.
2.  Select **Agent Verification**.

    ![DocIntel Admin agent verification mode for a use case](../image/doc-intel-admin-agent-verification.png)

3.  If desired, enable **Straight Through Processing**.
4.  Enter a percentage value in the **Set Straight Through Processing Threshold** field.

