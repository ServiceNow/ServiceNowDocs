---
title: Exploring Grants Management for Public Sector Digital Services
description: The Grants Management solution provides government agencies with a workflow for defining grant programs, screening applications, evaluating proposals, and communicating funding decisions. The solution runs entirely on the ServiceNow platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/public-sector-digital-services/psds-explore-grants-management.html
release: australia
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 4
breadcrumb: [Playbooks and Solutions, Explore, Public Sector Digital Services \(PSDS\)]
---

# Exploring Grants Management for Public Sector Digital Services

The Grants Management solution provides government agencies with a workflow for defining grant programs, screening applications, evaluating proposals, and communicating funding decisions. The solution runs entirely on the ServiceNow platform.

If you're a government agency, you can use Grants Management for Public Sector Digital Services to set up and award grants, apply for them, or both.

Grants are financial funding provided to individuals or organizations for a particular purpose, usually to fund initiatives that serve the public good. Grant-making agencies use Grants Management to create structured funding opportunities, collect and evaluate proposals from applicants, and manage award decisions and notifications — all from a single platform. Grant Program Managers stay in control of each stage, while applicants and external reviewers interact through dedicated portals.

Grants Management is a packaged application with playbooks and workflows built in to support an agency's grant portfolio at multiple levels, from portfolio-level funding programs through individual grant programs to case-level proposals and awards. Two core playbook-driven workflows power the solution:

-   **Setup Playbook** — establishes a grant program for the first time. After a program is created, you can copy and edit it for a new grant period without starting from scratch.

-   **Proposal Playbook** — supports the proposal management workflow handles the full application lifecycle for a published program, such as intake, screening and evaluation through final decision.


Grants Management uses funding programs and grant programs to separate portfolio‑level funding governance from opportunity‑level execution. Each construct serves a distinct role in the grant lifecycle and supports different users and decisions.

Grants Management 1.31 introduces rolling grant approvals. Grant program managers can propose and submit funding decisions for any scored subset of applications at any time. They do not need to wait for the entire proposal portfolio to complete merit review.

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
-   Accept, screen, and evaluate grant proposals submitted by applicants through guided playbook workflows, including eligibility checks powered by the PaCE.
-   Create and assign merit review tasks to internal review teams, and track scoring and ranking of proposals using configurable scoring frameworks.
-   Build funding proposals that allocate budgets across selected applicants, and route award decisions to the grants program director for approval.
-   Grant program managers can propose and submit funding decisions for any scored subset of applications at any time. They don't have to wait for the entire proposal portfolio to complete review. For more information, see [Rolling grant approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-gm-rolling-grant-approvals-concept.md).

-   Generate results letters to notify applicants of award, rejection \(ineligible\), or rejection \(decline\) outcomes, with the merit review summary where applicable.
-   Track applicant acknowledgment or decline of awarded grants.

## Related information

To get started with Grants Management, see the following topics:

-   [Install Grants Management for Public Sector Digital Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-install-grants-management.md)

-   

-   [Create a grant program using Grants Management program setup for Public Sector Digital Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-gmp-using-set-up-grants-management-program.md)
-   [Using the Grants Management Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-gmp-using-grants-mgmt-portal.md)

-   [Using the Reviewer Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-gmp-using-merit-review-portal-agent.md)


