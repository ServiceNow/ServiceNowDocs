---
title: Using Grants Management
description: Use Grants Management for Public Sector Digital Services to set up and award grants, and screen proposals for them​.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/government-industry/psds-using-grants-management-playbook.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
keywords: [Using grants management, setup grants, configure grants]
breadcrumb: [Playbooks and solutions, Use, Public Sector Digital Services \(PSDS\)]
---

# Using Grants Management

Use Grants Management for Public Sector Digital Services to set up and award grants, and screen proposals for them​.

The Grants Application Workflow in the Public Sector Digital Services \(PSDS\) Grants Management Playbook provides a structured process for managing grant applications from submission for the pre-award phase. It begins with application intake, where applicants submit required forms and eligibility is verified. The review and evaluation phase involves initial screening, technical assessments, and scoring to determine funding recommendations. Once selections are made, agencies proceed with award decisions and notifications, followed by grant agreement execution, where terms, reporting requirements, and disbursement schedules are established. Grants are financial funding provided to individuals or organizations for a particular purpose, usually to fund initiatives that serve the public good.

## Grants Management Landing Page

The Grants Management experience begins on the Grants Management landing page for grants agents and grants program managers. Grants organizations may customize their landing pages with branding colors or other display changes, but the components may remain the same.

The following is an example of how the default landing page appears in the CSM Configurable Workspace Grants Management workspace for a grant agents or grant program manager.

\[Omitted image "psds\_gmp\_landing\_page.png"\] Alt text: grants management landing page view for agents or managers

Here, you can see your workload at a glance, showing active cases, shared cases, upcoming deadlines and events, recent activity, and pending tasks. You can customize this view to your preferences, sorting cases and tasks with custom filters. You can create a grant program directly from this view, or you can navigate to the Lists menu to create it from there.

## Grants Management Program Setup Playbook

This is the first step in creating a grant program for applicants to submit to.

The process begins with program definition, where agencies establish milestones, internal program team members, eligibility criteria, budgets, and key performance metrics. Next, agencies configure the application process, defining required forms, terms and conditions, required budget categories, and review teams. Once the grant program is configured, it is reviewed, approved, and then published.

\[Omitted image "psds\_gmp\_program\_setup\_playbook\_initial\_view.png"\] Alt text: grants management playbook setup initial view for agents or managers

This playbook contains four stages, and several activities in each stage. It guides the program manager through the process of creating a grants program, from defining key details, to creating the announcement, to defining budget and milestones, to defining eligibility, to publishing it to the agency's Grants Management Portal. For more information on using the PSP to create a GP, see [Using the Grant Program Setup Playbook in Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-using-gmp-grant-pgr-setup.md).

Once you create a Grant program and publish it using the Program Setup Playbook, you can view the details on the program information record page.

## Grants Management Program Record page

Once grant program set-up is complete, you can see every case detail \(narrative, evidence, entities, tasks, and case team\) organized into a single grant program record, even before you publish the opportunity to the portal for applicants to submit. And you publish the opportunity, the state will display as **Accepting Proposals** in this view, and you may see all active proposals for the grant program by selecting the **Proposal** tab, and edit some program details by selecting the corresponding tabs.

\[Omitted image "psds\_gmp-case-view-workspace.png"\] Alt text: case record view for agent

For grants managers and agents, the grants program information record page aims to be a one-stop shop. For more information on configuring the page collection, see 

## Grants Management Application Intake​

For applicants, the application intake experience happens entirely on the Grants Management Portal, separate from the grants program manager/agent view. This feature improves self-service with a Grants Management Portal that simplifies finding, applying for, and tracking grants. Reduce applicant effort with guided intake, including save, resume, and export functionality​. Increase agent productivity with tools to make screening submissions easy​. This is where applicants will submit proposals for a grant program that was published by a grants program manager using the setup step. They can then be screened in the agent portion of the intake and screening feature. With a guided intake setup, including save, resume, and export functionality, Grants Management Intake aims to simplify the process of finding, applying for, and tracking grants for applicants.

\[Omitted image "psds-gmp-applicant-view.png"\] Alt text: entity record view

An applicant submitting a proposal is the first stage of the grants proposal playbook. The playbook is in the screen stage by the time it arrives to the agent. An agent cannot submit an application on behalf of an agent.

For more information on how applicants can use the Grants Management to view grants opportunities, submit applications, and view results, see [Using the Grants Management Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-gmp-using-grants-mgmt-portal.md).

## Grants Management Application Screening

For grants program managers \(case agents\) and directors, the application screening feature provides visibility across all proposal and submission details related to the grant program, once an applicant submits a proposal for an active grant program created by the grant program manager. Tools for agents to streamline the screening of submissions. The Grants Proposal Workflow in Public Sector Digital Services Grants Management provides a structured process for managing grant proposals from submission for the pre-award phase.

Using the Grants Management Screening feature, managers can:

-   Review the proposal
-   Confirm eligibility
-   Approve new contacts
-   Verifying documents submitted by the applicants

\[Omitted image "psds-gmp-rev-prop-details.png"\] Alt text: Enter Applicant information view

For more information on how grants managers can use the Application Screening feature, and [Screen a grant proposal application in the Grants Management Grants Proposal Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-using-gmp-grant-proposal-screen.md).

## Grants Management Application Evaluation

Grant proposals that pass the screening stage enter the evaluation phase, where the grants program manager creates and assigns proposal evaluation tasks to a group of external evaluators known as merit reviewers. Once all evaluation tasks are completed, the application is ready for the funding proposal phase, where certain grant applications will be selected for approval.

\[Omitted image "psds\_gmp\_proposal-playbook\_evaluation\_view.png"\] Alt text:

The funding proposal workflow involves the assessment of the evaluations conducted by the merit reviewers, and the definition of a proposal which will be sent to the Grant Program Director \(GPD\) for final approval. The funding proposal contains the individual grant applications which the grants program manager has selected for approval, as well as the proposed award amount for each.

**Note:** A grants program director can only approve or decline the entire funding proposal, not the individual grant proposals \(applications\) contained within it. A decline involves the creation of a new funding proposal which must be submitted again for approval.

## Grants Management Merit Review

For external reviewers, the Merit Review experience happens on the reviewer service portal, separate from the grants program manager/agent view. This allows external reviewers to review and score proposals, all within a dedicated portal.

\[Omitted image "psds-rsp-mrev-case-details-view.png"\] Alt text: reviewer portal grant program review task record view

For more information on using the Reviewer Service Portal as an external merit reviewer, see [Using the Reviewer Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-gmp-using-merit-review-portal-agent.md).

## Grants Management Application Decision

The final stage of the workflow is the decision phase. Based on the funding decisions made by the Grant Program Management team, a corresponding result letter is generated for each application. When all result letters across all applications are prepared, they are released, and the process awaits the acceptance of the outcome by the respective applicants. Applicants can access the results letter on the portal and either acknowledge or decline the award, and managers can capture the outcome of the proposal and close the record.

\[Omitted image "psds-gmp-create-res-letter.png"\] Alt text: decision view grants program manager

