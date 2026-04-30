---
title: Document Intelligence for Customer Service
description: Use the Document Intelligence for Customer Service feature to extract relevant information from email and case attachments, such as credit card numbers or customer addresses, and add that information to cases.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Task Intelligence for Customer Service, Machine learning solutions for Customer Service Management, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Document Intelligence for Customer Service

Use the Document Intelligence for Customer Service feature to extract relevant information from email and case attachments, such as credit card numbers or customer addresses, and add that information to cases.

![Case details tab displaying Predicted or Predicted from Docintel labels under certain field values, such as Account or Vendor name, alerting agents that the information was extracted by Document Intelligence.](../image/doc-intel-case-fields-predicted.png "Document Intelligence for Customer Service extracted fields")

Agents can review values for extracted fields and make corrections as needed by accessing the Document Intelligence interface directly from the case. From this interface, agents can confirm correct values, fix incorrect values, and continue to train the model. This HITL/Human In the Loop interaction of verifying the recommended values enables agents to refine the model and continually improve performance.

## Predicted field values

In CSM Configurable Workspace and Core UI, the fields on the Case form that contain Document Intelligence predicted values are identified with an AI icon \(![AI icon](../../../common/image/icon-ai-sparkle.png)\) and label. These fields also include an information icon that displays a message with additional context about the predicted values.

**Note:** The system displays the AI icon automatically. The agent doesn’t need to refresh the record page.

In CSM Configurable Workspace and Core UI, the fields on the Case form that contain Document Intelligence predicted values are identified with the message `Predicted from DocIntel`.

## Prediction banner

The system displays a banner at the top of a case record that contains one or more Document Intelligence field predictions. The banner is displayed:

-   When there is at least one field with an auto-filled prediction from a categorization model.
-   When one or more of the extracted fields haven’t been reviewed by the agent.
-   When the fields are being updated.
-   When the fields can’t be generated or predicted.

Once an agent reviews the field, the banner is removed.

The banner is displayed for records in the Case table, extensions of the Case table, and interaction records. The banner is displayed in the Core UI and CSM Configurable Workspace.

The banner can be enabled or disabled by the **sn\_csm\_ml\_task.ui.banner.enabled** system property.

## DocIntel Admin experience

The DocIntel Admin experience provides an easy-to-use interface that you can use to do the following:

-   Create and configure document processing use cases
-   Monitor the performance of Document Intelligence solutions

The DocIntel Admin experience is available with the Document Intelligence Admin \(com.snc.docintel\_admin\) store app. This app automatically activates the flows and properties required by Document Intelligence for Customer Service.

Access the DocIntel Admin experience through the Task Intelligence Admin Console:

1.  Navigate to **Task Intelligence for Customer Service** &gt; **Setup**.
2.  In the Explore related applications section of the console, select **Open DocIntel** in the Document Intelligence card.

    **Note:** If Document Intelligence Admin isn’t installed, the home page displays a link that you can use to download and activate the application.


For more information, see the following topics:

-   [Create a Document Intelligence use case](csm-task-intel-create-di-use-case.md)
-   [Monitor Document Intelligence performance](https://www.servicenow.com/docs/access?context=doc-intel-monitor-performance&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

.

## Use Cases list

From the DocIntel Admin experience, select **Use Cases** in the header to display a list of the use cases. The Use Cases list uses a default filter with an OR condition to show use cases for:

-   Application = Task Intelligence for Customer service -or-
-   MLUC ID = MLUC CSM-00003

**Note:** The user can’t modify these filter conditions from the advanced view.

Each use case has an MLUC ID number that is automatically assigned when the use case is created. This ID number is used for machine learning usage tracking. The Task Intelligence for Customer Service application manages the MLUC ID for Document Intelligence for Customer Service use cases.

## Document classification

With the system administrator role, you can create [document classification use cases](https://www.servicenow.com/docs/access?context=set-up-document-classification-use-cases&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) and define the classes or categories for the AI to detect and apply to documents. This process is useful in situations where there are multiple types of documents that must be evaluated.

Set up a document classification use case in the following steps.

1.  [Create a document classification use case.](https://www.servicenow.com/docs/access?context=set-up-document-classification-use-cases&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

    Define the name and properties for the use case.

2.  [Create a document class.](https://www.servicenow.com/docs/access?context=create-document-classes&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

    Define the classes or categories that the AI learns to detect and apply to documents.

3.  [Create a document task](https://www.servicenow.com/docs/access?context=upload-documents-for-extraction&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for document classification and upload sample documents for each class.
4.  [Train a use case.](https://www.servicenow.com/docs/access?context=train-a-use-case&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

    Initiate a training job to provide user inputs from completed document tasks to the AI for continuous improvement.


-   **[How Document Intelligence for Customer Service works](csm-docintel-how-it-works.md)**  
Document Intelligence for Customer Service performs a series of steps to extract relevant information from email and case attachments and add that information to fields on the case record.

**Parent Topic:**[Task Intelligence for Customer Service](csm-task-intelligence.md)

**Related topics**  


[Document Intelligence](https://www.servicenow.com/docs/access?context=document-intelligence-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

[Configure Document Intelligence for Customer Service](csm-doc-intel-configuring-.md)

[Review and submit values predicted by Document Intelligence](../task/csm-doc-intel-review-values.md)

