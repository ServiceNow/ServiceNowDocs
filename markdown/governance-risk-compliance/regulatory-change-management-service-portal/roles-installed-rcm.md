---
title: User roles in Regulatory Change Management
description: Stakeholders in the Regulatory Change Management \(RCM\) application have different roles and responsibilities.
locale: en-US
release: xanadu
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Regulatory Change Management, Governance, Risk, and Compliance]
---

# User roles in Regulatory Change Management

Stakeholders in the Regulatory Change Management \(RCM\) application have different roles and responsibilities.

The Regulatory Change Management application roles are installed with the activation of the GRC: Regulatory Change Management application. The customization or extension of configuration is not allowed. Only the users with GRC Admin roles can do the configurations setup. The application involves the following types of roles.

<table id="table_npk_pgd_mmb"><thead><tr><th>

Role titles and names

</th><th>

Description

</th><th>

Available roles

</th></tr></thead><tbody><tr><td>

RCM Admin \[sn\_grc\_reg\_change.admin\]

</td><td>

The RCM Admin has access to all the aspects of the Regulatory Change Management application.

</td><td>

-   sn\_grc\_reg\_change.it\_admin
-   sn\_grc\_reg\_change.manager

</td></tr><tr><td>

RCM IT \(Information Technology\) Admin \[sn\_grc\_reg\_change.it\_admin\]

</td><td>

The RCM IT Admin sets up the integrations with third-party regulatory intelligence providers. The RCM IT Admin troubleshoots issues, if any.

</td><td>

-   connection\_admin
-   action\_designer
-   import\_admin
-   credential\_admin
-   flow\_designer
-   oauth\_admin
-   sn\_grc.developer

 **Note:** The GRC User role \(sn\_grc.user\) contains the GRC Business User role \(sn\_grc.business\_user\). For more information, see [Common roles in Governance, Risk, and Compliance](../../grc-common/reference/grc-common-roles.md).

</td></tr><tr><td>

RCM Manager \[sn\_grc\_reg\_change.manager\]

</td><td>

The RCM Manager assigns regulatory alerts and monitors regulatory change tasks and action tasks.**Note:** A group titled as **RCM Managers** is added under **Groups** in the **User Administration** panel under the Regulatory Change Management application. The RCM Managers group reviews the regulatory tasks workflow, ensuring regulatory compliance. The users who belong to this group must have the sn\_grc\_reg\_change.manager role.

</td><td>

sn\_grc\_reg\_change.user

</td></tr><tr><td>

RCM User \[sn\_grc\_reg\_change.user\]

</td><td>

The RCM User assesses the applicability of the alerts, initiates impact assessments, responds to impact assessment questionnaires, and completes the assigned regulatory change tasks and action tasks.

</td><td>

-   sn\_compliance.reader
-   sn\_risk.reader

</td></tr></tbody>
</table>For information about feature roles, see [GRC Feature roles](../../grc-common/reference/grc-feature-roles-common-core.md).

**Parent Topic:**[Regulatory Change Management reference](rcm-reference.md)

