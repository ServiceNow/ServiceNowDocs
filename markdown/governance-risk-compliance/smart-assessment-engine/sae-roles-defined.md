---
title: Roles installed in Smart Assessment Engine
description: Roles determine the permissions and access in the Smart Assessment Engine application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/sae-roles-defined.html
release: brazil
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Components installed with Smart Assessment Engine, Reference, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Roles installed in Smart Assessment Engine

Roles determine the permissions and access in the Smart Assessment Engine application.

## SAE roles

<table id="table_jp5_vq4_21c"><thead><tr><th>

Role

</th><th>

Permissions

</th></tr></thead><tbody><tr><td>

Assessment actor \[sn\_smart\_asmt.actor\]

</td><td>

-   Respond to the assessments that are assigned to them.
-   Reassign the assessments that are assigned to them.

</td></tr><tr><td>

Assessment reader \[sn\_smart\_asmt.assessment\_reader\]

</td><td>

-   Read assessments that are within the categories that have the assessment reader role assigned.
-   Read, reassign, and comment on the assessments that you have requested.
-   Edit the due date of the assessments that you have requested, while they're in the open state.
-   View and comment on the assessments generated from any templates that have the assessment reader role configured.

</td></tr><tr><td>

Assessment admin \[sn\_smart\_asmt.assessment\_admin\]

</td><td>

Administrator for the SAE application.

 -   Access the Assessment Workspace.
-   Create, view, update, or delete a template category.

**Note:** A template category can't be deleted until any attached templates are removed.

-   Create, view, update, or delete an assessment template.
-   Create, view, update, or delete a question bank, regardless of QB category role.
-   View, cancel, or reassign assessments.
-   Edit the due date of an assessment, while it's in the open state.
-   Migrate the existing metric types to the assessment templates.

</td></tr><tr><td>

Assessment reassign \[sn\_smart\_asmt.reassign\]

</td><td>

Reassign assessments.

</td></tr><tr><td>

Template reader \[sn\_smart\_asmt.template\_reader\]

</td><td>

-   Access the Assessment Workspace with all details displayed in read-only mode.
-   Read the assessment template if you have a template category role that is associated with that template.

</td></tr><tr><td>

Template contributor \[sn\_smart\_asmt.template\_contributor\]

</td><td>

Includes template\_reader.

 -   Read and write specific assessment template elements \(questions, sections, response options, and conditions\) based on categories mapped to the templates.
-   Access to template categories is governed by the same logic as for template reader. Additionally, the user must match the contributor user criteria assigned to the specific template to edit its content.

</td></tr><tr><td>

Template manager \[sn\_smart\_asmt.template\_manager\]

</td><td>

Includes the Template\_reader and question\_bank\_reader roles.

 -   Read, write, and create the specific assessment templates that are based on the categories that are mapped to the templates.
-   Access the template categories if you have a template category role that is associated with that template.
-   Access question banks and add their published questions to assessment templates.

</td></tr><tr><td>

Template developer \[sn\_smart\_asmt.developer\]

</td><td>

Read, write, and create the script for response automation in assessment questions.**Note:** In addition to this role, you must also have either the assessment admin or template manager role to read, write, and create scripts.

</td></tr><tr><td>

Question bank manager \[sn\_smart\_asmt.question\_bank\_manager\]

</td><td>

Includes the question\_bank\_reader role.

 -   Create, view, update, and delete question banks, sections, and questions within categories that have a matching QB category role.
-   Move questions through the draft, ready to publish, published, and retired lifecycle stages.

</td></tr><tr><td>

Question bank reader \[sn\_smart\_asmt.question\_bank\_reader\]

</td><td>

-   View published questions in question banks within categories that have a matching QB category role.
-   Add published questions from a question bank to an assessment template.

</td></tr><tr><td>

Automation reader \[sn\_smart\_imp.auto.automation\_reader\]

</td><td>

-   Read the automation created for the assessment template.
-   Access the Assessment Workspace.
-   Read an assessment template if you have a template category role that is associated with that template.

</td></tr><tr><td>

Automation creator \[sn\_smart\_imp.auto.automation\_creator\]

</td><td>

-   Read, write, and create the automatons for the assessment template.
-   Access the Assessment Workspace.
-   Read an assessment template if you have a template category role that is associated with that template.

</td></tr></tbody>
</table>