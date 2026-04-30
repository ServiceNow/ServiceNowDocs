---
title: AI asset data model attributes
description: Additional attributes for the AI asset data model.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [AI Control Tower Reference, AI Control Tower, Enable AI experiences]
---

# AI asset data model attributes

Additional attributes for the AI asset data model.

## Attributes

AI model product model: Product Information for the AI model that is used by the AI system to generate responses without human intervention \(cmdb\_ai\_model\_product\_model\).

<table id="table_cxz_jsk_t2c"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Model parameters info

</td><td>

Number of parameters for the model.

</td></tr><tr><td>

Supported languages

</td><td>

Languages supported.

</td></tr><tr><td>

Model size

</td><td>

Size of the model in MB. Mostly applicable for models developed and deployed within the organization.

</td></tr><tr><td>

Deployment guidelines

</td><td>

Instructions applicable for models developed and deployed within the organization.

</td></tr><tr><td>

Source

</td><td>

Links or details of source of the model sources example: Hugging face, Microsoft, and so on.

</td></tr><tr><td>

Training procedure

</td><td>

Types of training-   Decision Trees
-   Deep Neural Networks
-   Linear Regression
-   Logistic Regression
-   Random Forest
-   Supervised Learning
-   Unsupervised Learning
-   Reinforcement Learning
-   Transfer Learning
-   Semi-Supervised Learning
-   Instruction Finetuning
-   Supervised Finetuning

</td></tr><tr><td>

Context window

</td><td>

Size of input sequences that the model can handle \(number of tokens\).

</td></tr></tbody>
</table>AI dataset product model: Product Information for the collection of data that is used to train and test AI models \(cmdb\_ai\_dataset\_product\_model\).

|Attribute|Description|
|---------|-----------|
|Data type|Describes data, example: Text, Image, Video, and Table|
|Source|Links or details of source of the dataset sources, example: Customer, Wikipedia, Hugging face, Crowd sourced, and so on.|
|Acceptable usage|Acceptable usage of the data according to license / contract example: Training, and Evaluation.|

AI prompt product model: Product Information for instructions given to AI models to get a response for AI system \(cmdb\_ai\_dataset\_product\_model\).

|Attribute|Description|
|---------|-----------|
|Documentation|Links and information about requirements, design, and related information.|

AI system product model: Product Information for software that provides ML / AI capability to generate outputs, such as decisions, recommendations, content, or predictions \(cmdb\_ai\_system\_product\_model\).

|Attribute|Description|
|---------|-----------|
|Documentation|Links and information about requirements, design, and related information.|

|Attribute|Description|
|---------|-----------|
|Data classification|Classification according to organization's data classification model, example: Public, confidential, and customer confidential.|

|Attribute|Description|
|---------|-----------|
|ServiceNow® record reference|Reference to Now Assist record.|
|ServiceNow® table|Now Assist table.|

|Attribute|Description|
|---------|-----------|
|AI models|Reference to more than one associated models.|
|Evaluation Dataset|Reference to more than one associated datasets used for evaluation.|
|Evaluation Metrics Report|Details of evaluation results.|

|Attribute|Description|
|---------|-----------|
|Base model|This AI model version was derived from an internal model developed within the organization.|
|Model weights info|Additional model information if available. Mostly applicable for models developed within the organization.|
|Required infrastructure|Documentation of infrastructure requirements for model deployment, primarily for models deployed within an organization. Example: Infrastructure stack and processing requirements.|
|Training dataset|Reference to one or more associated datasets used for training the model. These datasets are mostly applicable for models developed within the organization.|
|Evaluation dataset|Reference to one or more associated datasets used for evaluating the model. These datatsets are mostly applicable for models developed within the organization.|
|Evaluation metrics report|Links or details of evaluation results|
|License details|Link or detail to applicable licenses applied to the model.|
|Model card|Links to shareable model card \(Internal and external model card\).|

<table id="table_jqn_pzk_t2c"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base datasets

</td><td>

This version of the AI dataset was derived from the previous version.

</td></tr><tr><td>

Dataset card

</td><td>

Information on number of records, distribution, and so on.Documentation for data quality and known risks and limitations.

</td></tr><tr><td>

License details

</td><td>

Link or detail to applicable licenses applied to the dataset, example: CommonCore, Apache 2.0,etc.

</td></tr></tbody>
</table><table id="table_vjj_xbl_t2c"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Prompt information

</td><td>

Details of the prompt.

</td></tr><tr><td>

AI model

</td><td>

Reference to the AI model for which the prompt is created.

</td></tr></tbody>
</table>**Parent Topic:**[AI Control Tower Reference](aict-references.md)

