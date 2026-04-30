---
title: Request an AI model form
description: The Request an AI model form is designed to streamline the request process for developing or procuring an AI model. This intake form confirms that all necessary details, supporting documents, and compliance considerations are captured before moving forward with the approval process.
locale: en-US
release: zurich
product: AI Risk Management
classification: ai-risk-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Request an AI model, Use, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Request an AI model form

The Request an AI model form is designed to streamline the request process for developing or procuring an AI model. This intake form confirms that all necessary details, supporting documents, and compliance considerations are captured before moving forward with the approval process.

See the following table for a description of the field values.

<table id="table_l35_zwl_kkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Details

</td></tr><tr><td>

Name

</td><td>

Unique name for the AI model. For example, ServiceNow Now LLM 1.0.

</td></tr><tr><td>

State

</td><td>

Indicates whether the AI model is in a draft, development, or deployed state. For more information on states, see [AI asset lifecycle](https://www.servicenow.com/docs/access?context=ai-asset-lifecycle&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

</td></tr><tr><td>

Version

</td><td>

Version number for the AI model. For example, v1.0.

</td></tr><tr><td>

Description

</td><td>

Brief description of the AI system, its core functionality, and intended use. For example, ServiceNow Large Language Model \(LLM\) is an advanced AI-driven solution designed to enhance conversational capabilities and automate workflows within the ServiceNow platform. It leverages natural language processing to improve user interactions, streamline service delivery, and provide intelligent insights, ultimately enhancing operational efficiency for businesses.

</td></tr><tr><td class="sub-head" colspan="2">

Ownership

</td></tr><tr><td>

Provider

</td><td>

Organization responsible for providing the AI model. For example, ServiceNow.

</td></tr><tr><td>

Managed by

</td><td>

User responsible for managing the AI model.

</td></tr><tr><td class="sub-head" colspan="2">

Third-party Models

</td></tr><tr><td>

Model card

</td><td>

Detailed documentation on AI model's purpose, architecture, performance, and ethical considerations for transparency.

</td></tr><tr><td>

Model weights info

</td><td>

Additional model information if available. For example, Refer to weights and biases project.**Note:** This information is mostly applicable for AI models developed within the organization.

</td></tr><tr><td>

Supported languages

</td><td>

Languages supported by the AI model. For example, English, French, Italian, German, Spanish.

</td></tr><tr><td>

Base model

</td><td>

Base model that is relevant for the primary AI Model. A base model is a foundational AI model that has been pretrained on a large dataset and can be further fine-tuned for specific use cases. These models serve as a starting point for developing specialized AI models by adapting them to domain-specific data and requirements. For example, Mixtral.**Note:** The base models are only applicable for AI models developed within the organization.

</td></tr><tr><td>

Training procedure

</td><td>

Procedure used to train the AI model. The options are as follows:-   **Decision Trees**: A tree-like model used for decision-making, where each node represents a condition and branches lead to outcomes. It’s widely used for classification and regression tasks.
-   **Semi-Supervised Learning**: A machine learning approach that combines a small amount of labeled data with a large amount of unlabeled data to improve learning efficiency.
-   **Instruction Finetuning**: A process where an AI model is trained with task-specific instructions to improve its ability to follow human-like commands.
-   **Supervised Finetuning**: A technique where a pretrained model is further trained on labeled data to enhance its performance for a specific task.
-   **Deep Neural Networks**: A type of AI model with multiple layers of interconnected neurons that can learn complex patterns in data, used in deep learning.
-   **Linear Regression**: A statistical method that models the relationship between a dependent variable and one or more independent variables using a straight line.
-   **Logistic Regression**: A classification algorithm that predicts categorical outcomes \(for example, Yes or No\) by estimating probabilities using a sigmoid function.
-   **Random Forest**: An ensemble learning method that combines multiple decision trees to improve accuracy and reduce overfitting in classification and regression tasks.
-   **Supervised Learning**: A machine learning approach where models learn from labeled data, mapping inputs to correct outputs.
-   **Unsupervised Learning**: A learning method where models identify patterns and structures in unlabeled data without predefined categories.
-   **Reinforcement Learning**: A learning approach where an agent interacts with an environment and learns optimal actions through rewards and penalties.
-   **Transfer Learning**: A technique where a pretrained model is adapted to a new, but related, task to improve performance with less training data.

</td></tr><tr><td>

Context window

</td><td>

Number of tokens the AI model can process when generating responses or predictions. For example, 16385.

</td></tr><tr><td>

Model size in MB

</td><td>

Storage space occupied by the AI model in Megabytes.**Note:** The **Model size in MB** field only supports integer values.

</td></tr><tr><td>

Model parameters info

</td><td>

Internal variables learned during training that determine the AI model's behavior and performance. For example, number of parameters for the model is 175.

</td></tr><tr><td>

Evaluation metrics report

</td><td>

Performance measurement results used to assess the AI model's effectiveness during testing or evaluation. For example, you can mention the model's accuracy is 85% and hallucination rate is 15%.

</td></tr><tr><td>

Training datasets

</td><td>

Collection of datasets used to train the AI models.

</td></tr><tr><td>

Evaluation datasets

</td><td>

Collection of datasets used to evaluate or test the AI models. For example P1 incident dataset.

</td></tr><tr><td class="sub-head" colspan="2">

Additional Details

</td></tr><tr><td>

Deployment guidelines

</td><td>

The process of integrating and deploying a trained AI model into a production environment for real-world use.

</td></tr><tr><td>

Required infrastructure

</td><td>

Description of the Hardware and software resources needed to deploy and run the AI model. For example, you can mention that one graphics processing unit \(GPU\) of type A100 is required.

</td></tr></tbody>
</table>**Parent Topic:**[Request an AI model](../task/request-ai-model.md)

