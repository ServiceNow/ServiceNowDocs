---
title: Tables installed with Model Risk Management
description: Tables are added with the activation of the Model Risk Management application.
locale: en-US
release: yokohama
product: Model Risk Management
classification: model-risk-management
topic_type: reference
last_updated: "2025-08-07"
reading_time_minutes: 1
breadcrumb: [Reference, Model Risk Management, Governance, Risk, and Compliance]
---

# Tables installed with Model Risk Management

Tables are added with the activation of the Model Risk Management application.

See the following table for a description of the tables.

<table id="table_kf4_nqk_qjb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Model Risk

 \[sn\_model\_risk\_mgmt\_model\_risk\]

</td><td>

Captures model intakes submitted via the Employee Center, serving as a central repository for all submitted model requests.

</td></tr><tr><td>

Model Risk task

 \[sn\_model\_risk\_mgmt\_model\_risk\_task\]

</td><td>

Captures model risk tasks created for the model risks in the model risk workflow.

</td></tr><tr><td>

Model risk task approval

 \[sn\_model\_risk\_mgmt\_model\_risk\_task\_approval\]

</td><td>

Captures the approval status of all approval records generated for model risk tasks through approval configurations.

</td></tr><tr><td>

Issue to Model Risk

 \[sn\_model\_risk\_mgmt\_m2m\_issue\_model\_risk\]

</td><td>

Stores the many-to-many \(M2M\) mapping between all issues attached to the model risk.

</td></tr><tr><td>

Issue to Model Risk task

 \[sn\_model\_risk\_mgmt\_m2m\_issue\_model\_risk\_task\]

</td><td>

Stores the M2M mapping between all issues attached to the model risk task.

</td></tr><tr><td>

Model Risk configuration

 \[sn\_model\_risk\_mgmt\_model\_risk\_configuration\]

</td><td>

Stores the model risk assessment scoring configuration created for Smart Assessment templates in the Model Risk Management category.

</td></tr><tr><td>

Model Risk Config to SAE section

 \[sn\_model\_risk\_mgmt\_m2m\_model\_scoring\_section\]

</td><td>

Stores the M2M mapping between all the Smart Assessment sections added for use in the model risk configuration scripts.

</td></tr><tr><td>

Model Risk Config To SAE Question

 \[sn\_model\_risk\_mgmt\_m2m\_model\_scoring\_question\]

</td><td>

Stores the M2M mapping between all the Smart Assessment questions added for use in the model risk configuration scripts.

</td></tr><tr><td>

Model risk score

 \[sn\_model\_risk\_mgmt\_model\_risk\_score\]

</td><td>

Stores the scores calculated by the execution of model risk scoring configurations whenever a Smart Assessment is submitted and the assessment task is completed.

</td></tr></tbody>
</table>**Parent Topic:**[Model Risk Management reference](../concept/mrm-reference.md)

