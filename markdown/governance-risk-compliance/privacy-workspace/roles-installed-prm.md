---
title: Roles installed with Privacy Management
description: The GRC: Privacy Management application installs the roles for the privacy analyst, the privacy manager, and the privacy administrator to perform their respective tasks.
locale: en-US
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Privacy Management, Governance, Risk, and Compliance]
---

# Roles installed with Privacy Management

The GRC: Privacy Management application installs the roles for the privacy analyst, the privacy manager, and the privacy administrator to perform their respective tasks.

<table id="table_m2t_czq_mqb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Privacy Analyst\[sn\_privacy.analyst\]

</td><td>

Privacy analysts are responsible for managing the privacy compliance posture of the processing activities owned by them.​ They perform the following tasks:-   Assess the processing activities regularly by sending and reviewing privacy impact assessments​.
-   Work with the management and business users to identify and manage controls related to a processing activity​.
-   Manage and resolve the concerns of business users about compliance-related issues and policy exceptions​.
-   Test and monitor control effectiveness​.

 ​

</td><td>

-   sn\_grc\_workspace.task\_reader
-   sn\_risk\_advanced.ara\_approver
-   sn\_risk\_advanced.ara\_assessor
-   sn\_risk.user
-   sn\_compliance.user
-   sn\_privacy\_case.privacy\_case\_analyst

</td></tr><tr><td>

Privacy Manager\[sn\_privacy.manager\]

</td><td>

Privacy managers are responsible for managing the overall organization level privacy compliance posture.​ They perform the following tasks:-   Develop and implement privacy regulations, authority documents,​ and policies.
-   Review privacy regulatory requirements and policies​.
-   Design and monitor controls to deal with violations of privacy regulations and internal policies.​
-   Plan privacy programs and scope entities.
-   Creating privacy impact assessment templates.​
-   Continuously monitor control effectiveness and recommend effective improvements.
-   ​ Supervise the privacy compliance team.​
-   Report to management and the Board of Directors on compliance posture​.
-   Discover who is implementing privacy regulation for the first time in their organization.

</td><td>

-   sn\_compliance.manager
-   sn\_privacy.analyst
-   sn\_risk.manager
-   sn\_grc\_workspace.task\_admin
-   sn\_compliance.attestation\_creator
-   sn\_grc\_reg\_change.manager
-   sn\_privacy\_case.privacy\_case\_manager

</td></tr><tr><td>

Privacy Admin\[sn\_privacy.admin\]

</td><td>

Privacy administrators administer the privacy policy and compliance management. ​ Users assigned this role are responsible for configuring privacy management solutions as per the privacy team's requirements.​ They perform the following tasks:-   Configure privacy impact assessments and automated flows to trigger assessments​
-   Configure rules to auto-create processing activities ​out of privacy screening assessments.
-   Monitor the ServiceNow AI Platform dependencies with other applications and modules.
-   Can read the scripts under Processing activity script configurations related list.

 ​

</td><td>

-   sn\_privacy.manager
-   sn\_risk\_advanced.ara\_admin
-   sn\_compliance.admin
-   sn\_privacy\_case.privacy\_case\_admin

</td></tr><tr><td>

Privacy assessment responder \[sn\_privacy.assessment\_responder\]

</td><td>

Privacy assessment responders can respond to the privacy assessments as key stakeholders. They can also raise privacy requests from the portal.

</td><td>

-   sn\_grc\_workspace.task\_reader
-   canvas\_user

</td></tr><tr><td>

Privacy business user \[sn\_privacy.business\_user\]

</td><td>

Privacy business users can edit the assigned processing activities in the [Discover state](../concept/stages-pa.md), and also respond to the assessments.

</td><td>

-   sn\_grc\_workspace.task\_reader
-   canvas\_user
-   sn\_privacy\_case.privacy\_case\_business\_user
-   sn\_grc.business\_user

</td></tr><tr><td>

Privacy developer \[sn\_privacy.developer\]

</td><td>

Privacy developers can write custom scripts

</td><td>

sn\_privacy.admin

</td></tr><tr><td class="sub-head" colspan="3">

If the Privacy Employee User application is installed, then the following roles are available.

</td></tr><tr><td>

Privacy employee user \[sn\_privacy\_emp.privacy\_employee\]

</td><td>

Enables your employees to perform the following operations from the Employee Center: -   Proactively request privacy impact assessments \(PIAs\) for new implementations, applications, and processes from the Employee Center.
-   Report privacy cases related to data privacy policy and regulatory violations.
-   Read and acknowledge organizational privacy policies
-   Create policy exceptions.
-   Create privacy issues.

</td><td>

-   sn\_grc.issue\_employee\_user
-   sn\_compliance.policy\_ack\_employee\_user
-   sn\_compliance.policy\_exception\_employee\_user

</td></tr><tr><td class="sub-head" colspan="3">

If the GRC: Privacy Lite User application is installed, then the following roles are considered as lite operators.

</td></tr><tr><td>

-   sn\_privacy.assessment\_responder
-   sn\_privacy\_case.privacy\_case\_business\_user
-   sn\_privacy.business\_user
-   sn\_grc\_pdr.data\_owner\_admin

</td><td>

Users with the lite operator role can do the following:

 -   Respond to privacy assessment tasks as business users.
-   Work on the processing activity as a business user when it’s assigned to you to collect the required details.
-   Respond to the processing activity's criticality risk assessments and object-based assessment.
-   Respond to the detailed privacy risk assessments on each risk identified on a processing activity.
-   Work on breach assessments and other privacy case tasks.
-   Respond to the assessment and investigation tasks assigned by the privacy team.
-   Work on personal data rights action tasks to handle data according to the requester's requests.
-   Respond to the assigned control attestations.
-   View, update, and close assigned issues.
-   Create, update, and close assigned remediation tasks.
-   Respond to the assigned manual indicator tasks.

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Privacy Management reference](privacy-mgmt-reference.md)

