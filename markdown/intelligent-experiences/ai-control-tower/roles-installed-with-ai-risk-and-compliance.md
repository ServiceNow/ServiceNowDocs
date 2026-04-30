---
title: AI Risk and Compliance roles
description: The AI Risk and Compliance application installs the essential role to perform respective day-to-day operational tasks for managing AI systems across the enterprise.
locale: en-US
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, AI Control Tower, Enable AI experiences]
---

# AI Risk and Compliance roles

The AI Risk and Compliance application installs the essential role to perform respective day-to-day operational tasks for managing AI systems across the enterprise.

<table id="table_m2t_czq_mqb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

AI Risk and Compliance Admin

 \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_admin\]

</td><td>

​The AI Risk and Compliance Admin can perform the following tasks:-   Set up risk and impact assessment frameworks. Configure risk assessment methodologies, risk contribution factors, and impact assessment templates.
-   Define automation rules for impact assessments to determine applicable risks and controls based on the assessment responses.
-   Set up and profile AI case types.
-   Delete AI systems.

</td><td>

-   sn\_risk.admin
-   sn\_smart\_asmt.template\_manager
-   sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager
-   sn\_smart\_asmt.assessment\_admin
-   sn\_grc\_workspace.state\_model\_admin
-   sn\_smart\_asmt.template\_contributor
-   sn\_compliance.admin
-   sn\_compliance.control\_framework\_admin\*
-   sn\_compliance.library\_admin\*
-   sn\_compliance.policy\_admin\*

</td></tr><tr><td>

AI Risk and Compliance Manager

 \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager\]

</td><td>

​The AI Risk and Compliance Manager can access all AI systems on the system and perform the following tasks:​-   Initiate impact assessments.
-   Manage the lifecycle of an AI system.
-   Initiate risk assessments.
-   Initiate control attestations.

</td><td>

-   sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst
-   sn\_smart\_asmt.template\_contributor
-   sn\_smart\_asmt.template\_manager
-   sn\_risk.manager
-   sn\_compliance.control\_framework\_manager\*
-   sn\_compliance.library\_manager\*
-   sn\_compliance.policy\_manager\*

​

</td></tr><tr><td>

AI Risk and Compliance Analyst

 \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\]

</td><td>

The AI Risk and Compliance Analyst can access all AI systems assigned to them in the system and perform the following tasks only on the assigned records:-   Initiate impact assessments.
-   Manage the lifecycle of an AI system.
-   Initiate risk assessments.
-   Initiate control attestations.

</td><td>

-   sn\_smart\_asmt.assessment\_reader
-   sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user
-   sn\_smart\_asmt.template\_reader
-   sn\_risk\_advanced.ara\_approver
-   sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_​reader
-   sn\_grc\_workspace.user
-   sn\_risk.user
-   sn\_risk\_advanced.ara\_assessor
-   sn\_compliance.library\_user\*
-   sn\_compliance.control\_framework\_user\*
-   sn\_compliance.policy\_user\*

​

</td></tr><tr><td>

AI Risk and Compliance User

 \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user\]

</td><td>

The ​AI Risk and Compliance User can perform the following tasks:-   Create AI case on the Employee Center.
-   Work on the assigned tasks.
-   Perform control attestations.

</td><td>

​-   sn\_grc\_workspace.assessment\_template\_configuration\_reader
-   sn\_smart\_asmt.actor
-   sn\_grc.business\_user
-   sn\_grc\_workspace.user
-   sn\_smart\_asmt.assessment\_reader
-   sn\_compliance.control\_framework\_business\_user\*
-   sn\_compliance.library\_business\_user\*
-   sn\_compliance.policy\_business\_user\*

</td></tr><tr><td>

AI Risk and Compliance Reader

 \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_reader\]

</td><td>

​The AI Risk and Compliance Reader can have read access to the AI systems and AI impact assessments.

</td><td>

-   sn\_risk.reader
-   sn\_grc\_workspace.user
-   sn\_compliance.library\_reader\*
-   sn\_compliance.control\_framework\_reader\*
-   sn\_compliance.policy\_reader\*

​

</td></tr><tr><td>

AI System Reader

 \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_ai\_system\_reader\]

</td><td>

​The AI System Reader can have read access to the AI systems on AI Control Tower workspace and AI Risk and Compliance workspace.​

</td><td>

NA​

</td></tr><tr><td>

AI Case Business User

 \[sn\_ai\_case\_mgmt.ai\_case\_business\_user\]

</td><td>

The AI Case Business User can create ​AI case and AI inquiry on the Employee Center.

</td><td>

sn\_grc\_case\_mgmt.grc\_case\_business\_user​

</td></tr><tr><td>

AI Case Analyst

 \[sn\_ai\_case\_mgmt.ai\_case\_analyst\]

</td><td>

The AI Case Analyst can review the AI cases and AI inquiries assigned to them in the system and perform the following tasks only on the assigned records:​-   Identify and manage impacted and related areas such as policies, regulations, and enterprise wide compliance risks.
-   Identify and manage issues related to impacted areas to eliminate the root causes.

</td><td>

-   sn\_grc\_case\_mgmt.grc\_case\_analyst
-   sn\_ai\_case\_mgmt.ai\_case\_business\_user

​

</td></tr><tr><td>

AI Case Manager

 \[sn\_ai\_case\_mgmt.ai\_case\_manager\]

</td><td>

​The AI Case Manager can review all the AI cases, AI inquiries, and its associated information.

</td><td>

​-   sn\_ai\_case\_mgmt.ai\_case\_analyst
-   sn\_grc\_case\_mgmt.grc\_case\_manager

</td></tr><tr><td>

AI Case Admin

 \[sn\_ai\_case\_mgmt.ai\_case\_admin\]

</td><td>

The AI Case Admin can manage type profiles to segregate AI cases. They can set up assignment rules and delete AI cases.

</td><td>

​-   sn\_grc\_case\_mgmt.grc\_case\_admin
-   sn\_ai\_case\_mgmt.ai\_case\_manager

</td></tr></tbody>
</table>**Important:** Roles indicated with an asterisk \(`*`\) indicate feature roles.

**Note:** Feature Roles provide granular access to individual risk and compliance capabilities, enabling teams to share only the functionality they need. This capability replaces broad Integrated Risk Management \(IRM\) roles with feature-specific roles for better control. Non-Integrated Risk Management families like Privacy Management, Operational Sustainability Management, and AI Risk and Compliance are restricted from accessing IRM-specific data or core plugin features. This model ensures secure, domain-specific access and simplifies governance across GRC applications.

For more information, see [https://www.servicenow.com/products/employee-center.html](https://www.servicenow.com/products/employee-center.html).

**Parent Topic:**[AI Control Tower reference](aict-references.md)

