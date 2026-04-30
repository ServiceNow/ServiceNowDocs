---
title: Configuring Grants Management
description: Install the Grants Management application, which enables users to submit and track grants management requests and provides government agents with a predefined process for handling and resolving these requests. You can then configure the features available for submitting requests and routing requests to agents.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configuring Grants Management

Install the Grants Management application, which enables users to submit and track grants management requests and provides government agents with a predefined process for handling and resolving these requests. You can then configure the features available for submitting requests and routing requests to agents.

As a user with the admin role, complete the following configuration tasks to set up Grants Management, after you install the [Public Sector Digital Services Core](../task/install-public-sector-digital-services-core.md) application.

<table id="table_cmk_mdm_fwb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Install Grants Management for Public Sector Digital Services](psds-install-grants-management.md)

</td><td>

Install Grants Management from the ServiceNow® Store.

</td></tr><tr><td>

[Configure Restricted Caller Access \(RCA\) for Document Templates](../task/psds-config-gmp-fdtn-doc-template-rca.md)

</td><td>

Allow secure, controlled access for generating results letters.

</td></tr><tr><td>

[Assign user personas, roles, groups, and responsibilities in Grants Management](psds-config-gmp-assign-user-roles-responsibilities.md)

</td><td>

Assign roles to members of your grants organization Grants Management application so that your users can have delegated access to Grants Management features, capabilities, and data.

</td></tr><tr><td>

[Configure PaCE Eligibility Framework Engine for use with Grants Management](psds-config-gmp-pace.md)

</td><td>

Configure the eligibility framework engine, powered by PaCE, to allow agents to confirm whether an applicant is eligible for the specific grant being requested.

</td></tr><tr><td>

[Configure the Reviewer Service Portal](psds-config-reviewer-service-portal.md)

</td><td>

Configure the Grants Management Reviewer Service Portal for merit reviewers to track, score, and review grants proposals.

</td></tr><tr><td>

[Set up a grant program in Grants Management](psds-config-gmp-grant-pgr.md)

</td><td>

Set up and configure the details of a new grant program using Grants Management.

</td></tr><tr><td>

[Create a test grant program and grant proposal](psds-using-grants-management-playbook.md)

</td><td>

Verify the newly-configured grant program setup and grant proposal playbooks are working as expected by creating a new grant program and test grant proposal using the Grants Management.

</td></tr></tbody>
</table>## Key capabilities that support the Grants Management Workflows

The main ServiceNow capabilities that are leveraged to support the Grants Management workflows are:

-   Document Management/Processor​: Manage internal docs with version control, security, &amp; workflow integration. Request and verify docs from applicants​.
-   [Playbooks](playbooks-psds-exploring.md)​: Provide a visual, step-by-step guide for applicants and agents to complete key processes.​
-   [Policy as Code Engine \(PaCE\)](https://www.servicenow.com/docs/access?context=pace-managing-policies&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US): Streamline the creation, maintenance, and use of screening criteria with a low-code rules engine.
-   Configurable Portal Widgets: Use pre-built UI components for easy portal set up and modification.
-   [Smart Assessment](psds-config-gmp-smart-assessment-engine.md): Improve the creation and maintenance of application questions.
-   [Decision Trees](psds-config-gmp-config-pre-eligibility.md): Provide a structured, step-by-step approach for pre-screening potential applicants.​​​

