---
title: Roles in Smart Assessment Engine
description: Roles determine the permissions and access in the Smart Assessment Engine application.
locale: en-US
release: zurich
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Roles in Smart Assessment Engine

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
-   View and comment on the assessments generated from any templates that have the assessment reader role configured.

</td></tr><tr><td>

Assessment admin \[sn\_smart\_asmt.assessment\_admin\]

</td><td>

Includes the assessment\_admin role.

 Administrator for the SAE application.

 -   Access the Assessment Workspace.
-   Create, view, update, or delete a template category.

**Note:** A template category can't be deleted until any attached templates are removed.

-   Create, view, update, or delete an assessment template.
-   View, cancel, or reassign assessments.
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

Template manager \[sn\_smart\_asmt.template\_manager\]

</td><td>

Includes the template\_reader role.

 -   Read, write, and create the specific assessment templates that are based on the categories that are mapped to the templates.
-   Access the template categories if you have a template category role that is associated with that template.

</td></tr><tr><td>

Template developer \[sn\_smart\_asmt.developer\]

</td><td>

Read, write, and create the script for response automation in assessment questions.**Note:** In addition to this role, you must also have either the assessment admin or template manager role to read, write, and create scripts.

</td></tr><tr><td>

Automation reader \[sn\_smart\_imp.auto.automation\_reader\]

</td><td>

-   Read the automation created for the assessment template.
-   Access the Assessment Workspace.
-   Reads an assessment template if you have a template category role that is associated with that template.

</td></tr><tr><td>

Automation creator \[sn\_smart\_imp.auto.automation\_creator\]

</td><td>

-   Read, write, and create the automatons for the assessment template.
-   Access the Assessment Workspace.
-   Read an assessment template if you have a template category role that is associated with that template.

</td></tr></tbody>
</table>