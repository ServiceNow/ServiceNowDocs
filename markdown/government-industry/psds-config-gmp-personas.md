---
title: Grants Management Personas
description: Understand the key personas involved in Grants Management and their responsibilities in supporting grants.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/government-industry/psds-config-gmp-personas.html
release: zurich
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Assign personas, roles, responsibilities, and groups, Foundation, Grants Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Grants Management Personas

Understand the key personas involved in Grants Management and their responsibilities in supporting grants.

## Understanding Grants Management personas

Grants Management supports collaboration between multiple personas, each playing a distinct role in managing, delivering, and consuming services. Understanding these roles helps administrators assign the right access, responsibilities, and tools within the framework.

Grants Management supports access based on predefined personas that reflect the type of work users perform within an agency. These personas can be assigned and tailored to match your agency’s needs. A persona role may contain several roles within. The roles within are automatically added to the user when the persona role is added.

Grants Management models this flexibility through:

-   **Personas and Roles**

    Defined at the user level. Delegates access for the user across the entire agency.

-   **Responsibilities**

    Defined according to each grant program, at the grant program level only. Delegates access for the user according to the specific grant program. A user can be a point of contact for a grants program, part of the internal program team, or part of the external merit reviewer team. All of these are added at the grant program level, through activities in the program setup playbook.


The combination of user roles and responsibilities determines what a user can do within each grants agency, and within each grant program.

## Grants Management user personas

A persona role is pre-configured role in the application that is made up of multiple granular roles, and are designed to correspond to common job titles for members of an agency. Each persona role represents a different way a user interacts with an agency.. The following table contains the persona roles included with the Grants Management, and a description of each persona as it may pertain to an agency. For more information on the roles installed with Grants Management, including the roles contained in each persona, see [Grants Management roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/roles-installed-with-public-sector-digital-services.md).

<table id="table_idr_2r2_1hc"><thead><tr><th>

Persona

</th><th>

Description

</th><th>

Agency Example

</th></tr></thead><tbody><tr><td>

Admin\[admin\], \[sn\_gsm\_grnt\_mgmt.grant\_admin\]

</td><td>

An administrator is a certified ServiceNow system administrator of the agency. An administrator doesn't use the application directly, but supports configuration of the agency and its instances, hierarchy management, assignment of member roles and responsibilities \(including related-party configurations\), as well as general data management.

</td><td>

A system administrator sets up the agency's Servicenow environment, and manages all instances. A Grant Program admin has access to all grant programs within an agency, and can create, edit, or remove grant programs.

</td></tr><tr><td>

Grant Program Director\[sn\_svc\_appl\_pgm\_mg.grant\_program\_director\], \[pps\_resource\]

</td><td>

The Grant Program Director provides oversight and final approval for program setup and funding decisions. They ensure the program aligns with agency goals, compliance requirements, and available funding. The Grant Program Director serves as the senior authority responsible for the strategic oversight and governance of the grant program. This role involves approving final program configurations, ensuring compliance with organizational policies, and making key decisions regarding program direction and resource allocation. The Director reviews and authorizes the publication of opportunities, working closely with the Grant Program Manager to verify that all requirements and standards are met. Additionally, the Director provides guidance on complex issues, helps resolve escalations, and maintains accountability for the program’s overall success.

</td><td>

Review and approve program configuration before publication. Approve or decline funding recommendations submitted by the Program Manager. Provide strategic direction and ensure program compliance. Oversee program performance and outcomes.

</td></tr><tr><td>

Grant Program Manager\[sn\_svc\_appl\_pgm\_mg.grant\_program\_manager\], \[pps\_resource\]

</td><td>

The Grant Program Manager is the primary owner of the grant program, and is responsible for overseeing the full lifecycle of a grant program, from initial definition through announcement, application configuration, and final publication. hey design, configure, and maintain the program throughout its lifecycle. This includes defining eligibility criteria, review frameworks, budget structures, milestones, and required documentation. They also oversee application intake, screening, evaluation, and funding recommendations.

</td><td>

Define program details, eligibility rules, milestones, and budget parameters. Configure application forms, screening logic, and review workflows. Assign reviewers and manage merit review tasks. Monitor evaluation progress and consolidate scoring. Build funding proposals and submit recommendations for approval. Communicate with applicants as needed throughout the process. They are focused on compliance, success, and transparency, and are handling everything from document management, monitoring, reporting and understanding outcomes of a grant program. This role involves setting up program parameters, managing timelines and budgets, selecting review frameworks, and forming implementation teams. The manager ensures that all information and requirements are correctly configured and communicated, facilitating a transparent and efficient application process. Additionally, the Grant Program Manager coordinates with key stakeholders, reviews program setups, and seeks necessary approvals before publishing opportunities.

</td></tr><tr><td>

Merit \(External\) Reviewer\[sn\_gsm\_grnt\_mgmt.external\_reviewer\]

</td><td>

Merit Reviewers are subject matter experts \(SMEs\) assigned to evaluate proposals based on predefined scoring rubrics. They may be internal staff, external partners, or community reviewers depending on the program. These users are added to the grant program's external reviewer team using the activity in the playbook.

</td><td>

A merit reviewer is brought in to conduct merit reviews using structured scoring rubrics that have been pre-defined by the grant agency. The reviewer will evaluate proposals for technical quality, feasibility, and alignment with program goals, and submit scores, comments, and recommendations within assigned deadlines. They may participate in panel discussions if required.

</td></tr><tr><td>

Applicant\[sn\_customerservice.customer\] or \[sn\_gsm.business\_contact\]

</td><td>

The Grant Applicant represents an organization or business seeking funding through the grant program. This persona is responsible for preparing and submitting the application, including providing detailed organizational information, responding to eligibility screening, and assembling required documents such as budget plans and proposal narratives. They must be registered users on the portal.**Note:** The applicant must be a registered user in the Grants Management Applicant Portal, and must have either the

```
sn_customerservice.customer
```

or

```
sn_gsm.business_contact
```

roles.

</td><td>

An applicant seeking funding will work through the Grant Applicant Portal, where they will carefully review program requirements, adhere to compliance mandates, and ensure all conditions are met before they submit their application. Their role often involves collaborating internally to gather necessary data and signatures, as well as acting as the main point of contact for communications with the Grant Program Manager.

</td></tr><tr><td>

Grant Program Writer

</td><td>

A grant program viewer can edit grant programs that they are assigned to.

</td><td>

 

</td></tr><tr><td>

Grant Program Viewer

</td><td>

A grant program viewer can view grant programs that they are assigned to.

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Assign user personas, roles, groups, and responsibilities in Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-config-gmp-assign-user-roles-responsibilities.md)

