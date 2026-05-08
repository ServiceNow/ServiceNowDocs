---
title: How Document Intelligence for Customer Service works
description: Document Intelligence for Customer Service performs a series of steps to extract relevant information from email and case attachments and add that information to fields on the case record.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Document Intelligence, Task Intelligence for Customer Service, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# How Document Intelligence for Customer Service works

Document Intelligence for Customer Service performs a series of steps to extract relevant information from email and case attachments and add that information to fields on the case record.

## Use cases

A use case, previously known as a task definition, is a template that is used to define the structure of a type of document you want to process. A use case is made up of the use case record and its related fields, field groups, integrations, flows, and all the related machine learning \(ML\) models. For more information, see Set up document extraction use cases.

<table id="table_cdv_trj_h5b"><thead><tr><th>

Component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Fields

</td><td>

Identifies a field that you want to extract a value for. A use case includes the list of fields to extract from case and email attachments and a mapping of the extracted values to fields in the Case table.

</td></tr><tr><td>

Field groups

</td><td>

Field groups help Document Intelligence extract data from documents with tables, check box lists, and other logical groupings of fields.

</td></tr><tr><td>

Document tasks

</td><td>

A document task includes one or more attached documents that are used to train the use case to identify and extract the correct information. Document tasks are stored in the Document Tasks related list on the Use Case form.

 The Document Intelligence feature creates these tasks for each case with valid attachments. Each task trains the model. In CSM Configurable Workspace, agents can view these tasks, confirm or correct extracted values, and continue to train the model.

</td></tr><tr><td>

Integrations

</td><td>

Select conditions that tell the Document Intelligence feature when to extract values. The system creates tasks for those cases that meet the specified conditions.For example, you can add a condition on the **Category** field where **\[Category\]** **\[is\]** **\[Credit Card\]**.

 At run time, the system evaluates the active use cases and identifies the use case to use for the case based on the integration. The first active use case that matches the integration for the case or case type is selected.

 If there are use cases for the case or case type but none that match the integrations, then no use case is selected.

 You can create one integration for a use case. If a use case has more than one integration, the system uses the latest one.

**Note:** When creating an integration, make sure that the **Create Flow** check box remains unchecked.

</td></tr></tbody>
</table>Users with the ti\_admin role or the ti\_analyst role can create use cases for cases and for case types. At run time, the system identifies the correct use case based on the case or case type when a case is created and has a valid attachment. If there is no use case for a specific case type, the system goes up in the hierarchy chain until it finds a use case to use.

Use cases are stored in the Use Case \(di\_task\_definition\) table.

## Extraction modes

A use case includes an extraction mode that determines how the data is extracted in the document task and how the task is processed. The mode changes the behavior of the fields in the Document Intelligence workspace.

DocIntel uses the following extraction modes

<table id="table_vzp_p3p_d5b"><thead><tr><th>

Extraction mode

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Recommendation

</td><td>

Provides recommendations for the extracted fields in the Document Intelligence workspace. Agents can choose the recommended value for a field or manually enter a value. All fields must be reviewed.

 Recommendations are ordered based on how confident the AI is in the prediction. As Document Intelligence continues processing your documents, recommendations can improve over time.

</td></tr><tr><td>

Auto-fill

</td><td>

Adds values for the extracted fields in the Document Intelligence workspace. All fields must be reviewed.

 Auto-fill works only if the AI has enough confidence to make the prediction. You can change the confidence threshold by updating the **Auto-fill threshold** field in the use case.

</td></tr><tr><td>

Fully automated\(Straight through processing\)

</td><td>

DocIntel extracts the data for all fields and processes the document task if the confidence scores for all required fields are above the defined confidence threshold.

 DocIntel becomes more confident over time, as it processes more and more documents. Choose Fully automated mode for frequently processed documents or if you’re confident in the system.

</td></tr></tbody>
</table>## Extraction labels

In CSM Configurable Workspace, the fields on the Case form that contain Document Intelligence predicted values are identified with an AI icon \(![AI icon](../../../common/image/icon-ai-sparkle.png)\) and label. These fields also include an information icon that displays a message with additional context about the predicted values.

In Core UI, the fields on the Case form that contain Document Intelligence predicted values are identified with the message `Predicted from DocIntel`.

-   For Fully automated mode, the message appears below each extracted field returned by the task. The values and messages for each field are added to the case before the agent views the case record.
-   For the other extraction modes, the message appears below the extracted fields after the agent reviews the extracted values in the Document Intelligence interface, confirms or corrects values, and submits those values.

## Predicted field values

In CSM Configurable Workspace, the fields on the Case form that contain Document Intelligence predicted values are identified with an AI icon \(![AI icon](../../../common/image/icon-ai-sparkle.png)\) and label. These fields also include an information icon that displays a message with additional context about the predicted values.

In Core UI, the fields on the Case form that contain Document Intelligence predicted values are identified with the message `Predicted from DocIntel`.

## Performance

The Document Intelligence for Customer Service feature needs time to identify cases with attachments, scan the attachments, and make recommendations for case fields. The response time also depends on factors such as case with attachment volume and data center location.

The system displays notifications to the user for the following scenarios:

-   If the extraction fails.
-   If the extraction is too slow.
-   If there are no attachments.
-   If there are unexpected attachments.

## How it works

When a case is created, Document Intelligence for Customer Service checks to see:

-   If the case has one or more attachments.
-   If the attachment types are specified in the **sn\_csm\_ml\_task.case.docintel.parsing\_supported\_types** system property.

If yes, the feature:

-   Identifies the right use case to use based on the case or case type and the use case integrations.
-   Creates a task using the use case, the sys\_id of each attachment, and the case reference.
-   Sends the task, attachment sys\_ids, and case reference as inputs to the prediction model.
-   Uses optical character recognition \(OCR\) solutions to extract data from the documents.
-   Sets the status of the task to Done once the solution has completed.
-   If the extraction mode in the use case is set to Fully automated, the extracted values are added to the case.
-   If the extraction mode is set to Autofill or Recommendation, the agent can validate the extracted values in the Document Intelligence workspace.

The agent can open a case and review the predicted fields or review the prediction task by selecting **Review in DocIntel** and opening the Document Intelligence workspace interface in a separate tab. From this interface, agents can:

-   Review each predicted field.
-   Confirm correctly predicted values.
-   Update incorrect or missing values.
-   Submit the changes.

**Parent Topic:**[Document Intelligence for Customer Service](csm-document-intelligence.md)

