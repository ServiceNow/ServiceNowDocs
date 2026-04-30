---
title: Components installed with Task Intelligence for Customer Service
description: Several types of components are installed with the Task Intelligence for Customer Service application, including tables, roles, properties, flows, and scheduled jobs.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 11
breadcrumb: [Install Task Intelligence, Task Intelligence for Customer Service, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Components installed with Task Intelligence for Customer Service

Several types of components are installed with the Task Intelligence for Customer Service application, including tables, roles, properties, flows, and scheduled jobs.

## Tables

The Task Intelligence for Customer Service application uses the following tables.

<table id="table_ykp_1d5_xrb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ML Solution \[ml\_solution\]

</td><td>

The ML Solution table stores trained machine learning solutions.

 Activating the Task Intelligence for Customer Service application \(com.snc.csm\_ml\_task\) creates a record in this table for the pre-trained sentiment analysis machine learning solution: **ml\_x\_snc\_global\_global\_sentiment**.

</td></tr><tr><td>

ML Sentiment \[ml\_sentiment\]

</td><td>

This table stores machine learning sentiment information and includes the following fields:-   **Original sentiment**: The sentiment that is predicted when the case is created.
-   **Current sentiment**: The sentiment that is predicted when the case is updated.
-   **Sentiment over time**: Displays the sentiment trend prediction as an agent works to resolve the case. To be able to calculate a value for this field, there needs to be a minimum of two sentiment predictions.

The system uses the following formula used to determine the sentiment trend:

**\(currentSentiment - originalSentiment\) &gt; 0 ?'improving' :'declining';**


</td></tr><tr><td>

Predictor Result\[ml\_predictor\_results\]

</td><td>

This table stores prediction results and feedback for record categorization, sentiment analysis, and language detection. This includes skipped and failed predictions that result from prediction requests.

 For case categorization:

-   The **Default confidence** and **Predicted confidence** fields store confidence values returned by the categorization machine learning models.
-   For cases created from email, the **Source ID** field includes a reference to the sys\_email record and the **Predicted Table** field includes a reference to the sys\_email table.

 For sentiment analysis:

-   The default value in the **Predicted correctly** field for each sentiment prediction is set to true.
-   The **Final input value** and **Final output value** fields remain empty because sentiment analysis predictions do not collect feedback from agents.

 For language detection:

-   The Predictor Result table stores the prediction results from the Language Detection Service spoke.
-   The **Detected Language** field stores the language returned by the Language Detection Services spoke.

 The Predictor Result table includes the **Skipped** field, which is a true\|false field.

-   **True**: The prediction was skipped.
-   **False**: The prediction was not skipped.

For more details about skipped predictions, see [Logic for Skipped field values](case-categorization-components.md#table_njw_ztt_d1c) below.

 **Note:** The Predictor Result list includes a filter on the **Capability** field, which displays results where the capability is Classification. Remove this filter to display all of the prediction results.

</td></tr><tr><td>

Case\[sn\_customerservice\_case\]

</td><td>

The Case table stores customer service case records. This table is the recipient for case categorization predictions.The **Language** field has been added to the Case table. This field is a reference to the Language \[sys\_language\] table. This field is populated with the prediction made by the language detection spoke and stores the language that was used to create the email or case.

 The Case table is added with the Customer Service \(com.sn\_customerservice\) plugin.

</td></tr><tr><td>

Task \[task\]

</td><td>

The Task table is one of the core tables provided with the ServiceNow base system. The sentiment analysis feature adds the **Sentiment** column to the Task table. This column is a reference to the Task ML Sentiment \[task\_ml\_sentiment\] table.

</td></tr><tr><td>

Task ML Sentiment \[task\_ml\_sentiment\]

</td><td>

This table stores sentiment predictions. The reference to the prediction record is stored in the **Sentiment** field in the Task table. This table is an extension of the ML Sentiment \[ml\_sentiment\] table.

The **Task** column in the Task Sentiment table is a reference to the Task \[task\] table and is used for domain separation.

</td></tr><tr><td>

Task Skills\[task\_m2m\_skill\]

</td><td>

The Task Skills table stores skills for the Customer Service Management application.

 The language detection feature links language skills to new customer service cases by saving the detected language in the Task Skills table.

 The Task Skills table lists customer service cases and the language skill detected and assigned to each case.

</td></tr></tbody>
</table>|Prediction preference|Top 1 prediction|Top 3 \(at least 1 prediction\)|Skipped|
|---------------------|----------------|-------------------------------|-------|
|Autofill|Yes|Yes|False|
| |Empty|Yes|True|
|Recommendations|Yes|Yes|False|
| |Empty|Yes|False|
| |Empty|Empty|True|
|Monitor only|Yes|Yes|False|
| |Empty|Yes|False|
| |Empty|Empty|True|
|Prediction unsuccessful|NA|NA|True|
|Prediction error|NA|NA|True|

## Tables installed with Document Intelligence for Customer Service

The Document Intelligence for Customer Service application uses the following tables

<table id="table_w3z_tft_gwb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

DocIntel Use Case\[di\_task\_definition\]

</td><td>

Stores Document Intelligence use cases for the Case table \(sn\_customerservice\_case\) or case type tables that extend the Case table.

</td></tr><tr><td>

DocIntel Task\[di\_task\]

</td><td>

Stores Document Intelligence tasks.

 The **is\_stp** field controls straight through processing. When this field is set to true, straight through processing is enabled for the task.

 The **agent\_input** field is set to true if an agent makes changes to predicted values in the DocIntel tab.

**Note:** You can track tasks from the ML Solusions table \(ml\_solution.list​\).

</td></tr><tr><td>

Integration Setup\[di\_integration\_setup\]

</td><td>

Stores use case filters that are applied to cases.The **Target Table** field stores the target for the predicted fields, either the Case table \(sn\_customerservice\_case\) or a case type table.

</td></tr><tr><td>

Field\[di\_key\]

</td><td>

Stores the keys to be extracted by Document Intelligence.

</td></tr><tr><td>

Field Value\[di\_extracted\_value\]

</td><td>

Stores the extracted values for the keys in a use case task.

</td></tr></tbody>
</table>## Roles

The Task Intelligence for Customer Service application includes the following roles.

<table id="table_dny_pcd_ztb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Task Intelligence admin\[sn\_csm\_ml\_task.ti\_admin\]

</td><td>

Can create, train, and retrain machine learning models. This role can also deploy and delete models.

</td><td>

-   sn\_docintel.admin
-   sn\_ti\_admin.tia\_admin
-   sn\_customerservice.case\_viewer

</td></tr><tr><td>

Task Intelligence analyst\[sn\_csm\_ml\_task.ti\_analyst\]

</td><td>

Can create, train, and retrain machine learning models.

</td><td>

-   sn\_customerservice.case\_viewer
-   sn\_ti\_admin.tia\_analyst
-   sn\_docintel.manager

</td></tr><tr><td>

\[sn\_ti\_admin.tia\_admin\]

</td><td>

 

</td><td>

-   ml\_admin
-   platform\_ml\_read

</td></tr><tr><td>

\[sn\_ti\_admin.tia\_analyst\]

</td><td>

 

</td><td>

ml\_admin

</td></tr><tr><td>

\[sn\_ti\_admin.tia\_user\]

</td><td>

 

</td><td>

ml\_report\_user

</td></tr><tr><td>

Task sentiment viewer\[task\_ml\_sentiment\_viewer\]

</td><td>

Provides read access to records in the Task Sentiment \[task\_ml\_sentiment\] table if the user has read access to the associated task records.This role is added to the following roles:

-   sn\_customerservice\_agent
-   sn\_customerservice.consumer\_agent

</td><td>

 

</td></tr></tbody>
</table>**Note:** The sn\_docintel.extraction\_agent role is added to the customer service agent role \(sn\_customerservice\_agent\) and the consumer service agent role \(sn\_customerservice\_consumer\_agent\).

## Properties

The Task Intelligence for Customer Service application includes the following properties.

<table id="table_sdr_1r3_yrb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_csm\_ml\_task.logging.verbosity**

</td><td>

The log verbosity for the Task Intelligence for Customer Service application. This property has the following values:

-   **error**: Show only critical errors which may prevent the search from completing.
-   **warn**: Show warning which indicates possible unexpected changes in behavior while searching. Also shows errors.
-   **info**: Show progress messages as the Code Search application searches for results. Also shows errors and warnings.
-   **debug**: Show information that may be useful while debugging the application. Also shows errors, warnings, and info messages.
-   **off**: Do not generate logs.

 The default setting is info.

</td></tr><tr><td class="sub-head" colspan="2">

Categorization properties

</td></tr><tr><td>

**sn\_csm\_ml\_case.case.categorization.mlpredictor.enabled**

</td><td>

Enables categorization predictions for customer service cases. The default setting is false.

</td></tr><tr><td>

**sn\_csm\_ml\_task.categorization.attachment.max\_size**

</td><td>

Determines the maximum size of an attachment that can be parsed by categorization machine learning models. The maximum supported size is 500kb. The default setting is 450kb.

</td></tr><tr><td>

**sn\_csm\_ml\_task.categorization.allowed\_content\_types**

</td><td>

Controls the content types and file extensions that are supported by the ML predictor for categorization with attachment.

 By default, the following attachment types can be used with attachment-based case categorization predictions: pdf, xls, xlsx, docx, and csv.

 To configure content types:

-   Leave the property blank to allow all of the supported file extensions. This is the default setting.
-   Create a subset of the default values by entering a comma-separate list of content types and file extensions. For example, `application/pdf,text/csv`.

</td></tr><tr><td>

**sn\_csm\_ml\_task.categorization.flow\_start\_time.threshold**

</td><td>

Sets the max waiting threshold for categorization predictions that include attachments. The default value is 10 minutes.

 If the call to the API does not return a prediction before the maximum waiting threshold is reached, predictions are made without the attachment text. These predictions are based on text from the subject and body of the email or the case short description and description.

</td></tr><tr><td>

**sn\_csm\_ml\_task.categorization.case.delay\_attachment\_fetch**

</td><td>

Adds a 1-second delay before fetching valid attachments for Task Intelligence when cases are created from email.

</td></tr><tr><td>

**sn\_csm\_ml\_task.case.categorization.enable\_inactive\_filter**

</td><td>

Enable this property to remove inactive field choices from predictions. The default setting is false.

</td></tr><tr><td class="sub-head" colspan="2">

Sentiment analysis properties

</td></tr><tr><td>

**sn\_csm\_ml\_task.case.sentiment.mlpredictor\_enabled**

</td><td>

Enables sentiment predictions for customer service cases. The default setting is false. To enable sentiment predictions, set this property to true.**Note:** This property is automatically set to true when a sentiment model is trained and deployed from the [Task Intelligence Admin Console](../concept/csm-task-intel-admin-center.md).

</td></tr><tr><td class="sub-head" colspan="2">

Language detection properties

</td></tr><tr><td>

**sn\_csm\_ml\_task.case.language.mlpredictor.enabled**

</td><td>

Enables language detection for customer service cases. The default setting is false. To enable language detection, set this property to true.

**Note:** This property is automatically set to true when a language detection module is tested and deployed from the [Task Intelligence Admin Console](../concept/csm-task-intel-admin-center.md).

</td></tr><tr><td>

**sn\_csm\_customerservice.case.ml.language.detection.threshold**

</td><td>

Controls the threshold for language prediction. The default value for this property is 0.70.

 Predictions with a confidence level greater than the threshold are saved in the Predictor Results \(ml\_predictor\_results\_task\) table and the Task Skills \(task\_m2m\_skill\) table. Predictions with a confidence level less than the threshold are only saved in the Predictor Results \(ml\_predictor\_results\_task\) table.

</td></tr><tr><td>

**sn\_csm\_ml\_task.case.languagedetection.default\_confidence**

</td><td>

Stores the confidence level threshold for the language detection feature. The default value is 0.7.

</td></tr><tr><td class="sub-head" colspan="2">

Document Intelligence properties

</td></tr><tr><td>

**sn\_csm\_ml\_task.case.docintel.mlpredictor.enabled**

</td><td>

Enables Document Intelligence for Customer Service Management.**Note:** This property is activated automatically when the user creates a use case.

</td></tr><tr><td>

**sn\_csm\_ml\_task.case.docintel.parsing\_supported\_types**

</td><td>

Contains a list of the supported attachment types:

 **image/png,image/jpeg,application/pdf**

</td></tr><tr><td>

**sn\_csm\_ml\_task.straight\_through\_processing\_max\_waiting\_threshold**

</td><td>

Defines the maximum waiting time for a straight through processing task to finish. The default time is 5 minutes.

 If a use case is configured to use the straight through processing prediction mode, the agent can see the relevant fields on the Case form automatically populated within 5 minutes of case arrival.

 If this threshold is exceeded, the values are skipped. However, the agent can still view the task in the DocIntel tab and manually extract the values.

</td></tr><tr><td>

**sn\_csm\_ml\_task.case.delay\_attachment\_fetch​**

</td><td>

Waits for several milliseconds before fetching valid attachments for Task Intelligence for Customer Service when a case is created from email.**Note:** This property is disabled by default. If you notice that attachments are being missed for cases created from email, enable this property.

​

</td></tr></tbody>
</table>## Flows

The Task Intelligence for Customer Service application includes the following flows.

<table id="table_e4p_rjl_d5b"><thead><tr><th>

Flow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Task Intelligence Sentiment\[new\_task\_intelligence\]

</td><td>

This flow is inactive out of box and is activated after setting up models on the Task Intelligence Admin Console.

</td></tr><tr><td>

Task Intelligence Sentiment Case Update\[task\_intelligence\_case\_update\_flow\]

</td><td>

This flow is inactive out of box and is activated after setting up models on the Task Intelligence Admin Console.

</td></tr><tr><td>

Task Intelligence Inbound Email Reply\[task\_intelligence\_inbound\_email\_reply\]

</td><td>

This flow is inactive out of box and is activated after setting up models on the Task Intelligence Admin Console.

</td></tr><tr><td>

Task Intelligence Case Language Detection\[task\_intelligence\_case\_language\_detection\]

</td><td>

Language detection determines the language used to create a case.

 Depending on configuration, the system can add this value to the **Language** field on the Case form. This field is a reference to the Language \[sys\_language\] table. It can also add the language as a skill to the Task Skills related list on the Case form.

 This flow is automatically activated when a language detection module is trained and deployed from the [Task Intelligence Admin Console](../concept/csm-task-intel-admin-center.md).

</td></tr><tr><td>

Task intelligence - DocIntel at case creation

</td><td>

This flow is inactive out of box.

</td></tr><tr><td>

Task Intelligence - DocIntel Process Extracted Values

</td><td>

This flow is inactive out of box.

</td></tr></tbody>
</table>## Machine learning models

The sentiment analysis feature uses the **ml\_x\_snc\_global\_global\_sentiment** machine learning model. This model is provided with the Task Intelligence for Customer Service application.

## Scheduled job for categorization solution training

The system administrator can run the **Categorization solution training** scheduled job on demand.

**Note:** It is recommended that you import a training data set to the Case table \[sn\_customerservice\_case\] to support the initial training of the Categorization machine learning model. The training data set should be tailored to the Case fields that you want to predict and include additional case records that have the correct labels \(i.e., the expected field values\) for the specific fields being predicted. By creating this data set, you leverage your own data to train the algorithm to predict on the fields you select.

The system administrator can set the following parameters before running the scheduled job.

<table id="table_pl2_q2p_trb"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

trainNewSolution

</td><td>

Set to true to train a new solution. Set to false to retrain a solution and add the name of the solution in the **existingSolutionName** parameter.

</td></tr><tr><td>

inputFields

</td><td>

The fields that are used to train the model. For example:`["short_description","description"];`

</td></tr><tr><td>

outputFields

</td><td>

The fields to be predicted. For example:`["priority","category"];`

</td></tr><tr><td>

encodedQuery

</td><td>

The query that is applied to the data used for training.

</td></tr><tr><td>

existingSolutionName

</td><td>

The name of an existing solution. Add a name to this parameter if retraining a solution.

</td></tr></tbody>
</table>To determine when a solution is ready to be used for categorization predictions, the system administrator can check the status of the scheduled job. Once the state is Solution Complete, the solution can be used for predictions.

## Scheduled job for publishing previously deployed models

The system administrator can run the **Deploying Task Intelligence for Customer Service Management** after upgrading the Task Intelligence for Customer service plugin.

This scheduled job verifies if there are previously deployed models for record categorization, sentiment analysis, language detection, and Document Intelligence and publishes these models.

