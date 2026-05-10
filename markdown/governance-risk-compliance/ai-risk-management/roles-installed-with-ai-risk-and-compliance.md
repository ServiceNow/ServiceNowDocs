---
title: Roles installed with AI Risk and Compliance
description: The AI Risk and Compliance installs the essential roles to perform respective day-to-day operational tasks for managing AI assets across the enterprise.
locale: en-US
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Roles installed with AI Risk and Compliance

The AI Risk and Compliance installs the essential roles to perform respective day-to-day operational tasks for managing AI assets across the enterprise.

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
-   Enable or disable Entity-Based Access for record types associated with entity properties, and configure the Entity-Based Access settings as needed.

**Note:** GRC: Entity Based Access application must be installed to use this feature.


</td><td>

-   sn\_smart\_asmt.template\_manager
-   sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager
-   sn\_smart\_asmt.assessment\_admin
-   sn\_grc\_workspace.state\_model\_admin
-   sn\_smart\_asmt.template\_contributor
-   sn\_ai\_case\_mgmt.ai\_case\_admin
-   sn\_reg\_body\_mgmt.writer
-   sn\_risk\_advanced.ara\_admin
-   sn\_rec\_pg\_vertical.admin
-   sn\_grc\_ent\_access.admin

**Note:** GRC: Entity Based Access application must be installed for this role to be available.


</td></tr><tr><td>

AI Risk and Compliance Manager

 \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager\]

</td><td>

​The AI Risk and Compliance Manager can access all AI systems on the system and perform the following tasks:​-   Initiate impact assessments.
-   Manage the life cycle of an AI system.
-   Initiate risk assessments.
-   Initiate control attestations.
-   Write and update access to the bulk access update configuration.

**Note:** GRC: Entity Based Access application must be installed to use this feature.


</td><td>

-   sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst
-   sn\_smart\_asmt.template\_contributor
-   sn\_smart\_asmt.template\_manager
-   sn\_risk\_advanced.risk\_asmt\_project\_manager
-   sn\_ai\_case\_mgmt.ai\_case\_manager
-   sn\_grc\_ent\_access.bulk\_access\_config\_admin

**Note:** GRC: Entity Based Access application must be installed for this role to be available.


​

</td></tr><tr><td>

AI Risk and Compliance Analyst

 \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\]

</td><td>

The AI Risk and Compliance Analyst can access all AI systems assigned to them in the system and perform the following tasks only on the assigned records:-   Initiate impact assessments.
-   Manage the life cycle of an AI system.
-   Initiate risk assessments.
-   Initiate control attestations.

</td><td>

-   sn\_ai\_case\_mgmt.ai\_case\_analyst
-   sn\_smart\_asmt.assessment\_reader
-   sn\_smart\_asmt.template\_reader
-   sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user
-   sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_reader
-   sn\_grc\_workspace.user
-   sn\_grc\_workspace.state\_model\_reader
-   sn\_risk\_advanced.ara\_creator
-   sn\_risk\_advanced.ara\_assessor
-   sn\_risk\_advanced.ara\_approver
-   sn\_risk\_advanced.risk\_asmt\_project\_user

</td></tr><tr><td>

AI Risk and Compliance Business User

 \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user\]

</td><td>

The ​AI Risk and Compliance User can perform the following tasks:-   Create AI case on the Employee Center.
-   Work on the assigned tasks.
-   Perform control attestations.

</td><td>

​-   sn\_grc\_workspace.assessment\_template\_configuration\_reader
-   sn\_smart\_asmt.actor
-   sn\_grc\_workspace.user
-   sn\_smart\_asmt.assessment\_reader
-   sn\_risk\_advanced.risk\_asmt\_project\_reader

**Note:** For more information on AI Control Tower roles, see [AI Control Tower roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/roles-installed-with-ai-control-tower.md).

</td></tr><tr><td>

AI Risk and Compliance Reader

 \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_reader\]

</td><td>

​The AI Risk and Compliance Reader can have read access to the AI systems and AI impact assessments.

</td><td>

-   sn\_grc\_workspace.user
-   sn\_grc\_workspace.state\_model\_reader

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

The AI Case Analyst can review the AI cases and AI inquiries assigned to them in the system and perform the following tasks only on the assigned records:-   Identify and manage impacted and related areas such as policies, regulations, and enterprise-wide compliance risks.
-   Identify and manage issues related to impacted areas to eliminate the root causes.

</td><td>

-   sn\_grc\_case\_mgmt.grc\_case\_analyst
-   sn\_ai\_case\_mgmt.ai\_case\_business\_user

</td></tr><tr><td>

AI Case Manager

 \[sn\_ai\_case\_mgmt.ai\_case\_manager\]

</td><td>

The AI Case Manager can review all the AI cases, AI inquiries, and its associated information.

</td><td>

-   sn\_ai\_case\_mgmt.ai\_case\_analyst
-   sn\_grc\_case\_mgmt.grc\_case\_manager

</td></tr><tr><td>

AI Case Admin

 \[sn\_ai\_case\_mgmt.ai\_case\_admin\]

</td><td>

The AI Case Admin can manage type profiles to segregate AI cases. They can set up assignment rules and delete AI cases.

</td><td>

-   sn\_grc\_case\_mgmt.grc\_case\_admin
-   sn\_ai\_case\_mgmt.ai\_case\_manager

</td></tr></tbody>
</table>**Parent Topic:**[AI Risk and Compliance reference](ai-risk-and-compliance-reference.md)

