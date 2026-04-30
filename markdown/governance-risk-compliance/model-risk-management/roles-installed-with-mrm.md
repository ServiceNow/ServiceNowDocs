---
title: Roles installed with Model Risk Management
description: The Model Risk Management application installs the essential roles to perform respective day-to-day operational tasks for managing models.
locale: en-US
release: xanadu
product: Model Risk Management
classification: model-risk-management
topic_type: reference
last_updated: "2025-08-07"
reading_time_minutes: 2
breadcrumb: [Reference, Model Risk Management, Governance, Risk, and Compliance]
---

# Roles installed with Model Risk Management

The Model Risk Management application installs the essential roles to perform respective day-to-day operational tasks for managing models.

<table id="table_m2t_czq_mqb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

MRM Admin

 \[sn\_model\_risk\_mgmt.admin\]

</td><td>

The MRM \(Model Risk Management\) admin can perform the following tasks:-   Configure approval configurations for Model Risk Management.
-   Create Model Risk Management scoring configurations.
-   Create or modify assessment templates that belong to Model Risk Management category from the Model Risk Workspace.

</td><td>

-   sn\_grc\_appr.admin
-   sn\_model\_risk\_mgmt.model\_risk\_reader
-   sn\_smart\_asmt.template\_manager

</td></tr><tr><td>

Model Risk Governance

 \[sn\_model\_risk\_mgmt.model\_governance\]

</td><td>

User with Model Risk Governance role can perform the following tasks:-   Configure approval configurations for Model Risk Management.
-   Access the Model Risk Workspace.
-   Perform end to end workflow tasks for all the submitted models.
-   Create or modify assessment templates that belong to Model Risk Management category from the Model Risk Workspace.

</td><td>

-   sn\_model\_risk\_mgmt.model\_risk\_create
-   sn\_smart\_asmt.template\_manager
-   sn\_grc\_advanced.evidence\_admin
-   sn\_grc\_appr.admin
-   sn\_grc.reader
-   sn\_grc.business\_user
-   sn\_model\_risk\_mgmt.model\_risk\_delete

</td></tr><tr><td>

Model Risk Coordinator

 \[sn\_model\_risk\_mgmt.risk\_coordinator\]

</td><td>

Model Risk Coordinator can perform the following tasks:-   Access the Model Risk Workspace.
-   Access model intakes and tasks, and perform actions as needed where the user is assigned as a stakeholder.
-   Perform and modify model risk and model risk tasks where the user is assigned as a stakeholder.

</td><td>

-   sn\_grc.business\_user
-   sn\_grc\_advanced.evidence\_admin
-   sn\_model\_risk\_mgmt.model\_risk\_reader
-   sn\_grc.reader

</td></tr><tr><td>

Model Validator

 \[sn\_model\_risk\_mgmt.model\_validator\]

</td><td>

Model validator can perform the following tasks:-   Access the Model Risk Workspace.
-   Perform a smart assessment of models that are assigned to them from the Model Risk Workspace and GRC task page.
-   View the model risks where the user is assigned as a stakeholder.
-   Perform and modify model risk tasks where the user is assigned as a stakeholder.

</td><td>

-   sn\_grc.business\_user
-   sn\_grc\_advanced.evidence\_admin
-   sn\_smart\_asmt.actor
-   sn\_model\_risk\_mgmt.model\_risk\_reader
-   sn\_grc.reader

</td></tr><tr><td>

Model Executive Reader

 \[sn\_model\_risk\_mgmt.executive\_reader\]

</td><td>

Model Executive Reader can perform the following tasks:-   Access the Model Risk Workspace.
-   View all the information available in the Model Risk Workspace such as model intakes, tasks, issues.

</td><td>

-   sn\_model\_risk\_mgmt.model\_risk\_reader
-   sn\_grc\_advanced.evidence\_reader
-   sn\_grc.reader
-   sn\_grc\_appr.approver

</td></tr><tr><td>

Model Task Approver

 \[sn\_model\_risk\_mgmt.task\_approver\]

</td><td>

Model Task Approver can perform the following tasks:-   View model risks and model risk tasks for which they’re the designated approver.
-   Approve the model risk tasks assigned to them.

</td><td>

-   sn\_grc\_appr.approver
-   sn\_grc.reader
-   sn\_model\_risk\_mgmt.task\_read

</td></tr><tr><td>

Model Owner

 \[sn\_model\_risk\_mgmt.model\_owner\]

</td><td>

Model Owner can perform the following tasks:-   Request new models from the Employee Center or Service Portal.
-   Perform a smart assessment from the GRC task page when either the business\_user or business\_user\_lite role is assigned.

</td><td>

-   sn\_grc\_advanced.evidence\_responder
-   sn\_smart\_asmt.actor

</td></tr><tr><td>

Model Risk Initiator

 \[sn\_model\_risk\_mgmt.model\_initiator\]

</td><td>

Model Risk Initiator can request new models from the Employee Center or Service Portal.**Note:** Model Risk initiators can only request a new model but cannot perform assessments. They must define a model owner when raising the model request.

</td><td>

 

</td></tr></tbody>
</table>For more information, see the [Employee Center](https://www.servicenow.com/products/employee-center.html).

**Parent Topic:**[Model Risk Management reference](../concept/mrm-reference.md)

