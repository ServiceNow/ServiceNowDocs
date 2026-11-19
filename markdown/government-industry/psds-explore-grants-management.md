---
title: Exploring Grants Management for Public Sector Digital Services
description: With Grants Management, you can set up and award grants, and allow applicants to apply for them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/government-industry/psds-explore-grants-management.html
release: zurich
topic_type: concept
last_updated: "2026-06-08"
reading_time_minutes: 6
breadcrumb: [Playbooks and solutions, Explore, Public Sector Digital Services \(PSDS\)]
---

# Exploring Grants Management for Public Sector Digital Services

With Grants Management, you can set up and award grants, and allow applicants to apply for them.

If you're a government agency, you can use Grants Management for Public Sector Digital Services to set up and award grants, apply for them, or both.

\[Omitted image "psds\_explore\_gm\_landing\_page.png"\] Alt text: Grants management agent landing page view

Grants are financial funding provided to individuals or organizations for a particular purpose, usually to fund initiatives that serve the public good. Grant-making agencies use Grants Management to create structured funding opportunities, collect and evaluate proposals from applicants, and manage award decisions and notifications — all from a single platform.

Grants Management is a packaged application with playbooks and workflows built in to support an agency's grant portfolio at multiple levels. It manages portfolio-level funding programs, individual grant programs, and case-level proposals and awards. Two core playbook-driven workflows power the solution: the Grant Program Setup workflow for creating and configuring funding opportunities, and the Proposal Management workflow for handling application intake, review, and award decisions.

Grants Management uses funding programs and grant programs to separate portfolio‑level funding governance from opportunity‑level execution. Each construct serves a distinct role in the grant lifecycle and supports different users and decisions.

Grants Management 1.31 introduces rolling grant approvals. Grant program managers can propose and submit funding decisions for any scored subset of applications at any time. They do not need to wait for the entire proposal portfolio to complete merit review.

Designed for government investigative agencies at the federal, state, and local level, Grants Management provides a complex data ecosystem on a single platform. It allows centralized visibility across every grant program your agency offers and proposals your applicants submit.

## Key Features

Key features of Grants Management include:

-   **Grants Management Grants Program Setup Playbook**

    The Grants Management Grants Setup Playbook feature provides

    \[Omitted image "psds-gm-setup-agent-view.png"\] Alt text:

    The Grant Program Set-Up Playbook Workflow support the comprehensive process of establishing a Grant Program. This workflow is divided into four distinct stages, each intended to guide the Grant Program Manager through both internal and external program configuration requirements.

    For more information on the Grants Management Setup Playbook, see [Using the Grant Program Setup Playbook in Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-using-gmp-grant-pgr-setup.md).

-   **Grants Proposal Playbook**

    The ICM Grants Proposal Playbook feature allows users

    \[Omitted image "psds-gm-proposal-agent-view.png"\] Alt text:

    The Grants Management proposal playbook workflow manages the life cycle of grant applications submitted by organizations through the portal. This workflow is divided into four key stages, each with specific objectives and activities that guide the application from initiation to final decision.

    For more information on the Grants Proposal Playbook, see [Using the Grants Management Proposal Playbook in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-using-gmp-grants-proposal-playbook.md).

-   **Grants Management Applicant Portal**

    \[Omitted image "psds-gm-portal-applicant-view.png"\] Alt text:

    Use the ServiceNow Otto for Public Sector Digital Services \(PSDS\) Investigative Case summarization skill to synthesize case narratives, entities, evidence, and activity into a condensed, structured summary. Agents can grasp case context, respond to inquiries, and propose solutions. The skill integrates into the ICM workspace, allowing agents to generate a summary directly from the case record page and integrate generated resolution information into the case record.


## Grants Management hierarchy

Grants Management organizes grant data in a three-level hierarchy. This hierarchy helps you plan how to structure your agency's grant portfolio.

|Entity|Description|
|------|-----------|
|Funding program|A portfolio-level construct that represents a line of business, policy initiative, or funding authority. Funding programs are long-lived, persist across fiscal years, and define the overall budget envelope and timeline. One or more grant programs are created under a funding program.|
|Grant program|An individual funding opportunity created under a funding program. Each grant program defines eligibility criteria, budget categories, milestones, review frameworks, and the application form presented to prospective applicants on the Grants Management Portal. Each grant program creates a product model record.|
|Proposal and award|Case-level records used to receive, evaluate, and manage individual grant applications. When an applicant applies to a published grant program, they submit a proposal. If approved, the proposal transitions through the award process.|

**Note:** A grant program must be linked to a funding program before it can be published. The grant program's budget and timeline must fall within the funding program's budget and timeline.

## What you can do with Grants Management

Grants Management supports the complete grant life cycle. Depending on your role, you can use Grants Management to:

-   Create and manage funding programs that organize grant funding under a common portfolio, line of business, or policy initiative.
-   Set up grant programs that define individual funding opportunities, including eligibility criteria, budgets, milestones, and merit review frameworks. Once a program is created, you can copy and edit it for a new grant period without starting from scratch.
-   Publish grant program announcements to the Grants Management Portal so that prospective applicants can discover and apply for funding opportunities.
-   Accept, screen, and evaluate grant proposals submitted by applicants through guided playbook workflows, including eligibility checks powered by the Policy as Code Engine \(PaCE\).
-   Create and assign merit review tasks to internal review teams, and track scoring and ranking of proposals using configurable scoring frameworks.
-   Build funding proposals that allocate budgets across selected applicants, and route award decisions to the grants program director for approval.
-   Process funding decisions for any scored subset of proposals as they become available, without waiting for the entire proposal portfolio to complete merit review. For more information, see [Rolling grant approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-gm-rolling-grant-approvals-concept.md).
-   Generate results letters to notify applicants of award, rejection \(ineligible\), or rejection \(decline\) outcomes, with the merit review summary where applicable.
-   Track applicant acknowledgment or decline of awarded grants.

## Key Personas

Key personas of Grants Management include:

-   the Grant Program Manager, who is responsible for overseeing the full lifecycle of a grant program, from initial definition through announcement, application configuration, and final publication.
-   the Grant Program Director, who serves as the senior authority responsible for the strategic oversight and governance of the grant program.
-   the Applicant, who represents an organization or business seeking funding through the grant program. The Applicant prepares and submits the application, provides detailed organizational information, responds to eligibility screening, and assembles required documents such as budget plans and proposal narratives.

For more information on the personas and roles involved in Grants Management, see [Grants Management Personas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-config-gmp-personas.md).

## Related information

To get started with Grants Management, see the following topics:

-   [Install Grants Management for Public Sector Digital Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-install-grants-management.md)
-   
-   [Create a grant program using Grants Management program setup for Public Sector Digital Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-gmp-using-set-up-grants-management-program.md)
-   [Using the Grants Management Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-gmp-using-grants-mgmt-portal.md)
-   [Using the Reviewer Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-gmp-using-merit-review-portal-agent.md)

