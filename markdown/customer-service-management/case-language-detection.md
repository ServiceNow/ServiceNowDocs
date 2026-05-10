---
title: Language detection
description: The language detection feature uses a pre-trained model to detect the language used to create customer service cases. You can configure the model to add the language to the Language field on the case record and/or add the language as a skill for the case.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Task Intelligence for Customer Service, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Language detection

The language detection feature uses a pre-trained model to detect the language used to create customer service cases. You can configure the model to add the language to the **Language** field on the case record and/or add the language as a skill for the case.

![Case list view with short description field text in different languages and the detected language listed in the Name column.](../image/task-intel-language-detected.png)

Agents can save time by not having to manually select the language for each case or rely on a manual process for case routing. You can use the language skill stored in the Task Skills table to route cases to the assignment groups and agents with the necessary language skills.

-   Cases can be routed automatically with [Advanced Work Assignment \(AWA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-overview.md).
-   Cases can be assigned to agents based on language skills using the [assignment workbench](case-assignment-workbench.md).
-   Cases can be assigned based on the value in the **Language** field.

**Note:** Routing based on detected language must be configured separately.

The language detection feature supports 20 different languages. For details, see [Languages supported by Task Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/task-intelligence/languages-supported-by-language-detection.md).

## Language detection flow

Detecting the language used to create a case is based on a flow, **Task Intelligence Case Language Detected**, which is available with the Task Intelligence for Customer Service application. This flow is triggered at case creation with the condition that at least one of these case fields is not empty:

-   Short description
-   Description

When a case is created, the system calls the Detect Language action in the [Dynamic Translation spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/dynamic-translation/dynamic-translation-spoke.md) which evaluates the text and returns the detected language.

If the returned language confidence is above the defined confidence threshold, the system performs a check to see if the language exists in the Languages \[sys\_language\] table. It performs this check by matching the language code to the value in the ID field.

If the language exists in the Languages table, the system does the following, depending on the language detection model configuration:

-   Adds the language to the **Language** field in the Case table.
-   Stores the prediction results in the Predictor Results for Task table \[ml\_predictor\_results\_task\].
-   Stores the language skill in the Task Skills table \[task\_m2m\_skill\].

For more information, see [Create a model to detect case language](csm-task-intel-create-language-solution.md).

## Prediction results

The system stores feedback on prediction results in the Predictor Result \[ml\_predictor\_results\] table. Users with the ml\_admin role can access the table and view the results.

For language detection, the Predictor Result table stores the prediction results from the Language Detection Service spoke. The **Detected Language** field stores the language returned by the Language Detection Services spoke.

The Predictor Result table also stores information about skipped and failed predictions. For more information about this table, see [Components installed with Task Intelligence for Customer Service](../reference/case-categorization-components.md).

**Parent Topic:**[Task Intelligence for Customer Service](csm-task-intelligence.md)

**Related topics**  


[Configure language detection](case-language-detection-configure.md)

[Task Intelligence Admin Console](csm-task-intel-admin-center.md)

[Create a model to detect case language](csm-task-intel-create-language-solution.md)

