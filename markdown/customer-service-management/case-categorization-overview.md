---
title: Record categorization
description: The record categorization feature included with Task Intelligence for Customer Service uses machine learning models to evaluate text, predict field values, and automatically populate fields on case and interaction records.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Task Intelligence for Customer Service, Machine learning solutions for Customer Service Management, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Record categorization

The record categorization feature included with Task Intelligence for Customer Service uses machine learning models to evaluate text, predict field values, and automatically populate fields on case and interaction records.

Record categorization supports multiple languages and can scan attachments in addition to evaluating text from emails and records. Use this feature to categorize cases, case types, and interactions from multiple channels including email, web, and chat.

You can use the results of the categorization to automatically route records to the right service desk, which prevents the need for multiple email inboxes and RPA bots. Auto routing also frees up your employees to work on other tasks.

![Case form view highlighting the predicted values for the Account and Category sections.](../image/task-intel-case-categorization-fields.png "Case form with predicted and recommended field values")

## Predicted field values

On case and interaction records, the fields that contain predicted values are identified with an AI icon and label \(![generative AI sparkle icon and label](../image/task-intel-categorization-field-icon.png)\). These fields also include an information icon that displays a message with additional context about the predicted values.

**Note:** in CSM Configurable Workspace, the AI icon is persistent over the lifecycle of the record. In Core UI, the AI icon is removed when the agent changes the field value.

In CSM Configurable Workspace and Core UI, the fields on the record that contain predicted values are identified with the **Predicted** or **Recommended** messages.

## Recommended field values

Fields that are predicted by AI include recommended values. When an agent selects a predicted field, the system displays a dropdown list that includes the top three recommendations at the top of the list followed by all other values. This feature is available for the following types of fields:

-   Choice lists
-   Single lookup
-   Multi lookup
-   Single and multi text fields

If the top three recommendations are not available, the system displays a message in the Top Recommendations section of the dropdown list that no predictions are available. The other values follow this message.

The agent can select any value from the dropdown list, either one of the top three recommended values or one of the other values. The agent can also type in the field and filter the results in the dropdown list, with the exception of the top three recommendations which are always displayed.

**Note:** The top three recommendations remain in the dropdown list through the case lifecycle regardless of the selected field value.

## Filtering inactive field values from predictions

Enable the **sn\_csm\_ml\_task.case.categorization.enable\_inactive\_filter** to remove inactive field values from predictions. The default setting for this property is false.

## AI prediction banner

When a case record includes a categorization prediction, the system displays a banner at the top of the record. The banner is displayed when there is at least one field with autofill predictions in categorization models. The banner is displayed for records in the Case table and extensions of the Case table.

**Note:** The banner is displayed in CSM Configurable Workspace and in the Core UI.

The system displays the banner when there is at least one field with an autofill prediction in categorization models or when one of the extracted fields has not been reviewed by the agent. The banner is displayed for records in the Case table.

**Note:** If the agent changes the predicted value, the banner is removed. If all predicted fields are recommended, the banner is not displayed.

The banner can be enabled or disabled by the **sn\_csm\_ml\_task.ui.banner.enabled** system property.

## Prediction feedback

The system stores feedback on prediction results in the Predictor Result \[ml\_predictor\_results\] table. Users with the ml\_admin role can access the table and view the results.

-   Autofill: a value is considered to be predicted correctly \(set to true\) if the predicted value and the final value are the same.
-   Recommendation: a value is considered to be predicted correctly if any one of the predicted values matches the final value.

The Predictor Result table also stores information about skipped and failed predictions. For more information about this table, see [Components installed with Task Intelligence for Customer Service](../reference/case-categorization-components.md).

## Multi-lingual record categorization

Use a machine learning model that understands the following languages to evaluate text in emails and records created in different languages and to predict and automatically populate fields on cases, case types, and interactions.

-   English
-   French
-   German
-   Spanish

Multi-lingual record categorization uses one machine learning model that is trained to understand multiple languages. This model can:

-   Understand the text in emails and records.
-   Evaluate the text and predict field values.
-   Add the predicted values to fields on cases, case types, and interactions.

Multi-lingual record categorization can support the following additional languages on demand:

-   Arabic
-   Chinese \(PRC\)
-   Chinese \(Taiwan\)
-   Dutch
-   Italian
-   Japanese
-   Korean
-   Polish
-   Portuguese
-   Russian
-   Thai
-   Turkish

**Note:** If you need to evaluate emails or cases in these additional languages, reach out to the product team for support.

## Attachment-based record categorization

Attachments can include valuable signals that help support desks to categorize and route records automatically. To take advantage of attachment information, you can use a machine learning model to parse email and record text and attachments and automatically populate fields on cases, case types, and interactions based on signals contained in the text.

The model can predict information about a case based on:

-   Text in the subject line and body of a customer email.
-   Text in the short description and description of a case or interaction.
-   Text in email and record attachments.

**Note:** The model can be configured to use different fields for prediction.

Attachment-based categorization uses all of this information to predict field values. As a result, you can automatically route records to the appropriate service desk based on these values.

**Parent Topic:**[Task Intelligence for Customer Service](csm-task-intelligence.md)

**Related topics**  


[Configure record categorization](case-categorization-configure.md)

[Task Intelligence Admin Console](csm-task-intel-admin-center.md)

[Create a model to predict record fields](csm-task-intel-create-cat-solution.md)

