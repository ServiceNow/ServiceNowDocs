---
title: Exploring Model Risk Management
description: Learn how you can use the Model Risk Management application to identify, assess, and mitigate risks related to the quantitative models.
locale: en-US
release: zurich
product: Model Risk Management
classification: model-risk-management
topic_type: concept
last_updated: "2025-08-06"
reading_time_minutes: 4
keywords: [explore]
breadcrumb: [Model Risk Management, Governance, Risk, and Compliance]
---

# Exploring Model Risk Management

Learn how you can use the Model Risk Management application to identify, assess, and mitigate risks related to the quantitative models.

## Model Risk Management overview

The Model Risk Management \(MRM\) application provides a unified solution to help organizations proactively manage the risks associated with the use of models. It offers a structured approach to identify, assess, validate, and address model risks throughout the model life cycle. This approach reduces operational and compliance risks caused by inconsistent or inadequate model oversight.

For example, a financial institution uses a Value at Risk \(VaR\) model to estimate potential trading losses. Without proper validation, the model can underestimate risk, leading to poor capital allocation. By using the MRM application, the bank can validate the model regularly, document assumptions, track issues, and confirm it meets regulatory standards. This reduces risk and supports better decision-making.

## Model Risk Management users

|User|Description|
|----|-----------|
|Model Owner|Oversees the model life cycle and monitors its performance.|
|Model Developer|Designs and builds models aligned with business requirements.|
|Model Validator|Performs independent validation to confirm model accuracy, reliability, and robustness.|
|Model Governance|Reviews models for risk and compliance and approves models based on governance standards.|
|Executive Management|Provides strategic oversight and makes high-level decisions informed by model risk insights.|

## Model Risk Management workflow

The following section describes the steps from the submission of a model risk in the Employee Center to the assessment and monitoring of the risks associated with that model.

![Infographic showing how Model Owner, Model Governance, and Model Validator submit, assess, validate, and monitor a model risk. For details, refer to the following description.](../image/mrm-workflow.png "Submitting and managing model risks with Model Risk Management")

1.  An employee can use the Employee Center and submit a new model request.
2.  A new model record is automatically created in the model inventory and can be assessed in the Model Risk Workspace.
3.  The Model Governance team reviews the submitted model, fills in the required details such as stakeholders, and then creates relevant assessments.
4.  The Model Owner performs the risk assessment on the model and submits it to the Model Governance team for review. The assessment task is then sent for approval to the defined approvers configured in the Approver Configurator.
5.  The Model Governance team reviews and approves the assessment. The model then moves to the Pre-deployment stage.
6.  The Model Governance team creates and assigns the validation task to the validator.
7.  The model validator validates the model, collects required documents, reports any issues, and decides if the model is fit for use.
8.  The validation task is then sent for approval to the defined approvers configured in the Approver Configurator.
9.  The model then moves to the Monitor stage.
10. The Model is periodically assessed and validated to confirm regulatory compliance and effective risk management.

## Model Risk Management benefits

<table id="table_hkg_gsr_fgc"><thead><tr><th>

Feature

</th><th>

Benefit

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Model Inventory

</td><td>

Provides a single, reliable source of truth for all models, enabling faster oversight and informed decision-making.

</td><td>

-   Model Governance
-   Model Owner
-   Model Validator
-   Model Risk Owner
-   Model Risk Coordinator

</td></tr><tr><td>

Model Risk Life-cycle

</td><td>

Manages the full model life-cycle by tracking models from initiation to monitoring through defined governance stages, confirming consistent governance and lowering operational and compliance risk.

</td><td>

-   Model Governance
-   Model Owner
-   Model Validator
-   Model Risk Initiator
-   Model Risk Coordinator

</td></tr><tr><td>

Model Risk Assessment

</td><td>

Helps quickly identify and prioritize high-risk models so resources focus where they matter most. To perform a model risk assessment and evaluate the risks associated with a quantitative model, refer to [Perform model risk assessment](../task/perform-model-risk-assessment.md).

</td><td>

-   Model Owner
-   Model Validator

</td></tr><tr><td>

Model Validation

</td><td>

Builds confidence in model reliability through independent checks that reduce errors and regulatory concerns.To perform model validation, refer to [Perform model validation](../task/perform-model-risk-validation.md).

</td><td>

Model Validator

</td></tr><tr><td>

Model Documentation

</td><td>

Makes it easy to maintain clear, audit-ready documentation that streamlines reviews and improves transparency.To link documents from your repository to a model record, refer to [Link existing documents to a model record](../task/link-existing-documents-model-record.md).

</td><td>

-   Model Governance
-   Model Validator
-   Model Risk Coordinator

</td></tr><tr><td>

Model Issue &amp; Remediation

</td><td>

Enables timely detection and resolution of model issues, minimizing business disruption and confirming continuous compliance.To report an issue, refer to [Create an issue for model](../task/create-an-issue-for-model-risk.md).

</td><td>

-   Model Governance
-   Model Validator
-   Model Risk Coordinator

</td></tr></tbody>
</table>## What to explore next

To learn more about configuring and using Model Risk Management, see:

-   [Configuring Model Risk Management](configuring-mrm.md)
-   [Configure scoring logic for model risk assessments](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2287605)
-   [Using Model Risk Management](using-mrm.md)
-   [Model Risk Management reference](mrm-reference.md)

