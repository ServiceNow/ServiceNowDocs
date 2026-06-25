---
title: Using the Grants Proposal Management Playbook in Grants Management
description: Use the Grants Proposal Playbook to manage the life cycle of grant applications submitted by organizations through the portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-using-gmp-grants-proposal-playbook.html
release: australia
topic_type: concept
last_updated: "2026-03-17"
reading_time_minutes: 9
breadcrumb: [Grants Management, Solutions, Use, Public Sector Digital Services \(PSDS\)]
---

# Using the Grants Proposal Management Playbook in Grants Management

Use the Grants Proposal Playbook to manage the life cycle of grant applications submitted by organizations through the portal.

The Grants Management case, or the Grant Proposal, is designed as a case type which extends the Government Service Case and functions as the primary transactional entity for receiving Grant Applications/Proposals. When proposals are submitted, they are entered into this dedicated table. A workflow is then initiated, which is presented to Grants Program managers and directors as a Proposal Playbook. This structured process ensures the efficient management and review of grant proposals. "Proposal" and "application" are used interchangeably.

The Grants Management Proposal Playbook includes Application Intake, Proposal Screening, Proposal Evaluation and Scoring, and Decision. It is designed to systematically manage the life cycle of grant applications submitted by organizations through the portal. This workflow is divided into four stages, each with specific objectives and activities that guide the application from initiation to final decision.

A grant proposal is the formal submission prepared by an individual, non-profit, or organization seeking funding for a specific project or initiative. The Grants Management workflow provides agents with a playbook that guides them step-by-step through reviewing, scoring, and deciding on proposals submitted by individuals to a specific grant program that is has been made available. Grants **proposal** and grants **application** are used interchangeably.

## Proposal Intake

Role required: Grant Applicant \(role: sn\_gsm.business\_contact\)

For applicants, the application intake experience happens entirely on the Grants Management Portal, separate from the grants program manager/agent view. This feature improves self-service with a Grants Management Portal that simplifies finding, applying for, and tracking grants. Reduce applicant effort with guided intake, including save, resume, and export functionality​. Increase agent productivity with tools to make screening submissions easy​. This is where applicants will submit proposals for a grant program that was published by a GPM using the setup step. They can then be screened in the agent portion of the intake and screening feature. With a guided intake setup, including save, resume, and export functionality, Grants Management Intake aims to simplify the process of finding, applying for, and tracking grants for applicants.

\[Omitted image "psds-gmp-applicant-view.png"\] Alt text: entity record view

An applicant submitting a proposal is the first stage of the grants proposal playbook. The playbook is in the screen stage by the time it arrives to the agent. An agent cannot submit an application on behalf of an agent.

Once the application is routed to the Grant Program Manager, the intake stage and all of its activities will show as complete in the Grant Manager's proposal playbook, and it will become read-only.

-   **Answer Eligibility questions**

    \[Omitted image "psds-gmp-ans-pre-elig.png"\] Alt text: answer eligibility questions view

    Prospective applicants are posed a series of qualifying questions, ensuring that applicants meet the predefined eligibility requirements.

-   **Enter applicant information**

    \[Omitted image "psds-gmp-applic-inf.png"\] Alt text: Enter Applicant information view

    The Applicant enters primary information about themselves and the organization on behalf of which they are seeking a grant award. This information is stored in the `sn_svc_appl_info_applicant` table.

-   **Add Authorized Representative**

    \[Omitted image "psds-gmp-auth-rep.png"\] Alt text: Enter auth representativeview

    Applicants can add individuals that can act as a signatory for their organization. This section may be skipped if there are no authorized representatives other than the primary applicant.

-   **Enter proposal information**

    \[Omitted image "psds-gmp-ent-prp-info.png"\] Alt text: Enter proposal information view

    Applicants use this step to add the necessary grant proposal information, such as the project title for which they are seeking funding, the project abstract, proposed project funding start date, and proposed funding end date.

-   **Add proposal narrative**

    \[Omitted image "psds-gmp-prop-narr.png"\] Alt text: Enter Applicant information view

    Applicants provide the narrative around their proposal according to the narrative requirements set by the Grant Program Manager, which determines the required number of goals, and whether the Objective details field is shown as an upload or a form.

    \[Omitted image "psds-gmp-prop-narr-deliv.png"\] Alt text: Deliverables and goals view

    Applicants can enter goals and related information by selecting **Add goal**, and add multiple deliverables by selecting **Add deliverable**.

-   **Add Required Documents**

    \[Omitted image "psds-gmp-prop-docs.png"\] Alt text: Enter Applicant information view

    Applicants can download the required document template and upload the required documents to support their application.

-   **Add key personnel**

    \[Omitted image "psds-gmp-add-pers.png"\] Alt text: Enter Applicant information view

    Applicants add required and additional key personnel to their proposal. By default, applicants can choose to add the following types of personnel to an application: Principal Investigator, Project Director, Faculty Associate, Senior/Key Personnel, Co-Investigator, Research Assistant, Project Coordinator, or Consultant.

-   **Add proposal budget**

    \[Omitted image "psds-gmp-prop-budg.png"\] Alt text: Enter Applicant information view

    Applicants can request or update their budget, upload supporting documents, and ensure the proposal includes a clear financial plan for review. If the budget amount entered exceeds the limit set by the Grant Program Manager \(visible on the Grant Program announcement\), an error will be shown.

-   **Add Letters of Support**

    \[Omitted image "psds-gmp-letters-support.png"\] Alt text: Enter Applicant information view

    Applicants upload any letters of intent, memoranda of understanding, or any other relevant documents that demonstrate partnerships or collaborations for the project.

-   **Add optional attachments**

    \[Omitted image "psds-gmp-optional-attach.png"\] Alt text: Enter Applicant information view

    Applicants can add include additional attachments to support their grant application if necessary. It provides the applicant with the opportunity to upload optional attachments that may be important for the proposal but were not included in earlier activities.

-   **Enter compliance information**

    \[Omitted image "psds-gmp-compliance.png"\] Alt text: Enter Applicant information view

    Here, the applicant will answer a series of questions that ensure that their proposal is compliant with regulations set forth by both the grant program manager and other regulatory agencies. This activity uses a sub-flow to generate an instance of the smart assessment template selected and used in the compliance requirements activity of Grants Management program setup playbook. The sub-flow only runs once in the lifetime of the activity to create the instance and associate it with the current proposal. Responses can be changed until merit review tasks have been created.

-   **Confirm proposal details**

    \[Omitted image "psds-gmp-prop-confirm.png"\] Alt text: Enter Applicant information view

    Applicants can review and confirm all details related to their grant proposal here before submission of the application.

-   **Sign and Submit**

    \[Omitted image "psds-gmp-prop-sign-submit.png"\] Alt text: Enter Applicant information view

    Allows the applicant to review, authorize, and finalize their submission. Captures the applicant’s signature and completes the application submission. The Terms and Conditions displayed in this activity are retrieved from the Point in Time Content \(sn\_svc\_appl\_info\_pitc\) table. For more information on configuring terms and conditions, disclaimers, and other point-in-time content for a grant program, see .


## Proposal Screening

Role required: Grant Program Manager \(sn\_svc\_appl\_pgm\_mg.grant\_program\_manager\).

For grants program managers \(case agents\) and directors, the application screening feature provides visibility across all proposal and submission details related to the grant program, once an applicant submits a proposal for an active grant program created by the grant program manager. Tools for agents to streamline the screening of submissions. The Grants Proposal Workflow in Public Sector Digital Services Grants Management provides a structured process for managing grant proposals from submission for the pre-award phase.

Using the Grants Management Screening feature, managers can:

-   Review the proposal
-   Confirm eligibility
-   Approve new contacts
-   Verify documents submitted by the applicants

-   **Review Proposal Details**

    \[Omitted image "psds-gmp-rev-prop-details.png"\] Alt text: Enter Applicant information view

    Get a comprehensive view of information collected with each applicant's grant proposal \(submitted during Applicant Intake\). Grants program managers have read-only access to the proposals, ensuring data integrity while allowing them to stay informed on submitted proposals.

-   **Confirm eligibility**

    \[Omitted image "psds-gmp-conf-elig.png"\] Alt text: Enter Applicant information view

    Determine the eligibility of an applicant based on the execution of PaCE polices linked to the proposal’s program, defined during the Program Setup phase. For more information on setting up or modifying PaCE policies to determine post-submission eligibility of a grant application, see [Configure Eligibility Rules Engine Policies in Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-gmp-eligibility.md).

-   **Approve new contacts**

    \[Omitted image "psds-gmp-apprv-contacts.png"\] Alt text: Enter Applicant information view

    View and approve, or reject, any new contacts or authorized representatives, submitted in the **Add authorized representative** activity by the applicant, that are not already in the system's user database. A user must have the business contact \(sn\_gsm.business\_contact\) role to be eligible as one of the grant proposal’s contacts. The case cannot proceed until the Grant Program Manager approves or rejects the contact.

-   **Verify Documents**

    \[Omitted image "psds-gmp-verif-doc.png"\] Alt text: Enter Applicant information view

    Verify that all required documents are submitted, correctly formatted, and accurate. If there are incomplete documents, you may flag them and move the proposal directly to decision. The manager has the option to undo a verification if needed.


## Proposal Evaluation

Required role: Grant Program Manager \(sn\_svc\_appl\_pgm\_mg.grant\_program\_manager\).

Grant proposals that pass the screening stage enter the evaluation phase, where the grants program manager creates and assigns proposal evaluation tasks to a group of external evaluators known as merit reviewers. Once all evaluation tasks are completed, the application is ready for the funding proposal phase, where certain grant applications will be selected for approval.

\[Omitted image "psds\_gmp\_proposal-playbook\_evaluation\_view.png"\] Alt text:

The funding proposal workflow involves the assessment of the evaluations conducted by the merit reviewers, and the definition of a proposal which will be sent to the Grant Program Director \(GPD\) for final approval. The funding proposal contains the individual grant applications which the grants program manager has selected for approval, as well as the proposed award amount for each.

**Note:** A grants program director can only approve or decline the entire funding proposal, not the individual grant proposals \(applications\) contained within it. A decline involves the creation of a new funding proposal which must be submitted again for approval.

-   **Conduct Merit Review**

    \[Omitted image "psds-gmp-cond-mer-rev.png"\] Alt text: create merit review tasks view

    Select a reviewer group from the list of reviewers from the grant program and create merit review tasks for each of the reviewers evaluating the grant proposal. Once these tasks are created, the Grant Program Manager can release them to the external reviewers using the Reviewer Service Portal, where they score proposals against a pre-defined criteria set forth by the Grant Program Manager or Director.

-   **Build Funding Proposal**

    \[Omitted image "psds-gmp-build-fund-prop.png"\] Alt text: Reviewing funding proposal view

    Evaluate the funding information of the current proposal, and modify the funding information under funding proposal tab.


## Proposal Decision

Required role: Grant Program Manager \(sn\_svc\_appl\_pgm\_mg.grant\_program\_manager\).

The final stage of the workflow is the decision phase. Based on the funding decisions made by the Grant Program Management team, a corresponding result letter is generated for each application. When all result letters across all applications are prepared, they are released, and the process awaits the acceptance of the outcome by the respective applicants. Applicants can access the results letter on the portal and either acknowledge or decline the award, and managers can capture the outcome of the proposal and close the record.

-   **Create Results Letter**

    \[Omitted image "psds-gmp-create-res-letter.png"\] Alt text: create results letter

    Manage the release of result letters in a coordinated manner, ensuring that applicants receive results at the same time and that no applicant is notified before all decisions are finalized. Based on the funding decisions made by the Grant Program Management team, a corresponding result letter is generated for each application, and when all result letters across all applications are prepared, are released to applicants by the Grant Program Manager.

-   **Record Outcome**

    \[Omitted image "psds-gmp-rec-out.png"\] Alt text: recording outcome view

    Await the acceptance of the outcome by the respective applicants.


