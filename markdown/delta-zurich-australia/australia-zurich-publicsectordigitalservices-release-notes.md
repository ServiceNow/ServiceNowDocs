---
title: Combined Public Sector Digital Services release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Public Sector Digital Services from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-publicsectordigitalservices-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 15
breadcrumb: [Products combined by family]
---

# Combined Public Sector Digital Services release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Public Sector Digital Services from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Public Sector Digital Services release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Public Sector Digital Services to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

After the upgrade, certain public sector menus and menu items in CSM Configurable Workspace revert to their original CSM label names. You can relabel these items for public sector use by updating the labels for the Customer, Accounts, and Service Organizations UX list category records. For more details on relabeling, navigate to **All** &gt; **Constituent Service** &gt; **Administration** &gt; **Guided Setup**, and select **Configurable Workspace for Public Sector Digital Services** &gt; **Customize Workspace Labels Manually**.

</td></tr><tr><td>

Australia

</td><td>

After the upgrade, certain public sector menus and menu items in CSM Configurable Workspace revert to their original CSM label names. You can relabel these items for public sector use by updating the labels for the Customer, Accounts, and Service Organizations UX list category records. For more details on relabeling, navigate to **All** &gt; **Constituent Service** &gt; **Administration** &gt; **Guided Setup**, and select **Configurable Workspace for Public Sector Digital Services** &gt; **Customize Workspace Labels Manually**.

 Customers who have not opted into new third-party LLM models may be silently routed to them during skill execution. If the new model is not provisioned or available in the customer's environment, this will result in skill execution failures. Check the models your skills are using in the AI Admin Hub console.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Public Sector Digital Services.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Grants Management Funding Program](https://www.servicenow.com/docs/access?context=psds-using-grants-management-playbook&family=zurich&ft:locale=en-US)**

Create a funding program, which serves as the top-level container from which individual grant programs are created and derive their budget allocations.

Grant program managers can create a new funding program, or start by copying data and configurations from an existing funding program, using the funding program ID. From this funding program, admins can create grant programs directly, set and update the duration and overall budget, and ensure budgets flow down logically to individual grants.

Each grant program is associated with a single funding program via the funding program ID. All grant programs linked to a specific funding program share the cumulative budget of that funding program, and their start and end dates fall within the funding program's duration.

-   **[Grants Management Evaluation &amp; Decision​](https://www.servicenow.com/docs/access?context=psds-using-grants-management-playbook&family=zurich&ft:locale=en-US)**

Simplify and streamline your grant application decisions​ with Grants Management:​ Evaluation &amp; Decision. You can review, score, and manage proposals for grant programs in the Merit Review portal and define a funding proposal for a grant program by using the Grants Workspace. You can share this information internally with the grant program director.​ Grant program managers can define the merit review framework criteria, assign a reviewer group to each application, create, and track merit review tasks. Grant program managers can use document templates to compose letters that inform the applicants of results, with template options for Award, Rejected \(Ineligible\), and Rejected \(Decline\).

-   **[Grants Management Reviewer Service portal](https://www.servicenow.com/docs/access?context=psds-gmp-using-merit-review-portal-agent&family=zurich&ft:locale=en-US)**

Enable your merit reviewers to track, score, and monitor grant applications via a dedicated Reviewer Service portal. The merit reviewers can capture and aggregate scores across the Grant Proposal review framework​ in the Grants Workspace. A score and rationale can be summarized as part of the application proposal result.​

-   **[Agentic AI](https://www.servicenow.com/docs/access?context=agentic-ai-psds-explore&family=zurich&ft:locale=en-US)**

Define the fees for information requests and autonomously assess waivers against an agency's criteria​. You can automate the process of synthesizing similar information requests and associated fees, and apply those fees to cases​. Your case fields are automatically filled in and integrated into the Information Request Playbook workflow and ServiceNow's AI framework.


</td></tr><tr><td>

Australia

</td><td>

-   **[Enhancements to the grants management Workspace- Rolling grant approvals](https://www.servicenow.com/docs/access?context=psds-using-grants-management-playbook&family=australia&ft:locale=en-US)**

Propose awards and declines for any scored subset of applications at any time. The Rolling grant approval feature enhances the Grants management funding workflow, by giving Grant Program Managers the flexibility to propose awards and declines for any scored subset of applications at any time, without waiting for the entire proposal portfolio to complete review. From this release, Grant Program Managers can choose to process funding decisions incrementally as proposals are scored, or continue working in the traditional full-portfolio model.

The feature introduces the Funding Allocation Request as a new record type — an approval packet that groups a subset of proposals for Grant Program Director review. The Grant Program Director can either approve the Funding Allocation Request or reject it, returning all proposals in the batch, regardless of whether they were on the funding or decline track. The proposals in the rejected batch feed back into the Grant Program Manager's working queue, re-entering the funding pool for future review and funding allocation opportunities. The Funding Allocation Requests introduce an alternative to the previous all-or-none approval model and enable continuous, long-running grant programs to operate on a single program record.

Release result letters per proposal for Rolling grant approval scenarios in Grants Management. Once a proposal’s funding or decline decision is approved through its Funding Allocation Request \(FAR\), the corresponding award, decline, or ineligibility letter can be issued to that applicant independently—without waiting for program-wide completion.

-   **[Investigative Case Management](https://www.servicenow.com/docs/access?context=psds-explore-inv-case-management&family=australia&ft:locale=en-US)**

Create an investigative case using Investigative Case Management. Investigative Case Management guides investigators through the process of organizing, tracking, and resolving investigations, ​developing case details,​ assigning investigators and team members​, and track evidence with logging and metadata. The following features are available as part of Investigative Case Management:

    -   Entity Management
    -   Evidence Management
With Entity Management, investigators can create investigative tasks and workflows for investigative activities with automated metadata capture \(time, source, entities, classification\)​, as well as define processing with teams and attorneys and collaborate across agencies/divisions. With Evidence Management, investigators can log and triage evidence metadata \(digital, physical, testimonial\)​ and maintain an audit trail \(Chain of Custody logging\), as well as draft, review, and create reports with supporting evidence​​.

-   **[Task Tab and Field Service Management case escalation in Investigative Case Management](https://www.servicenow.com/docs/access?context=psds-using-icm&family=australia&ft:locale=en-US)**

Use the Tasks tab in the investigative case record to view and create investigative tasks directly within the case context. Use the **Create Work Order** to escalate a case directly to an Field Service Management work order without leaving the ICM workspace​​.

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Use ServiceNow Otto for Public Sector Digital Services \(PSDS\) Skills to create case narratives and screen documents](https://www.servicenow.com/docs/access?context=now-assist-psds-using&family=australia&ft:locale=en-US)**

Complete case narratives and make refinements to investigative case records using ServiceNow Otto for PSDS Gen-AI skills. Investigators can streamline case narrative refinement by editing content, adjusting tone, and regenerating the narrative for clarity and completeness.

-   **[Use the Case Narrative Refinement AI Agent to refine case narratives in Investigative Case Management](https://www.servicenow.com/docs/access?context=psds-na-case-narrative-refinement-agent&family=australia&ft:locale=en-US)**

Produce clear, accurate, and well-structured case narratives using the Case narrative refinement AI agent, embedded within the case record page. This AI agent analyzes existing narratives and related case data to suggest improvements in clarity, structure, tone, and completeness, and highlighting gaps and inconsistencies.

-   **[Document Screening AI Skill for Social Benefits Playbook](https://www.servicenow.com/docs/access?context=psds-ai-skill-doc-screening&family=australia&ft:locale=en-US)**

Validate large volumes of uploaded documents, verify information, flag issues, and highlight key details for case agents using the Social Benefits Playbook with the Document Screening Al Skill, part of ServiceNow Otto for Public Sector Digital Services \(PSDS\).

-   **[GOV.UK Developer Toolkit GDS Service Portal](https://www.servicenow.com/docs/access?context=psds-gdsp-overview&family=australia&ft:locale=en-US)**

Launch citizen-facing services using the GOV.UK Developer Toolkit, a collection of pre-built, GDS-compliant portal widgets that developers and partners can use to build service portals for UK government agencies. The GOV.UK Developer Toolkit comes with standardized components \(homepage, FAQs, Registration, Profile, login, case detail, knowledge search, record producers\) that can be used to assemble portals that meet UK accessibility and design standards and are compliant with GOV.UK Design System patterns​. WCAG 2.2AA compliant, and 400% zoom/reflow support has been added.

-   **[Granular configuration admin roles](https://www.servicenow.com/docs/access?context=roles-installed-with-public-sector-digital-services&family=australia&ft:locale=en-US)**

Several new granular admin roles enable admins to complete administrative configuration tasks on the Public Sector Digital Services platform without requiring the full admin role. These granular access roles enable a high-level administrator to define and assign custom roles that contain only the specific permissions a user needs, decreasing the number of users with full administrative power over the instance. For more information on granular admin roles, see [Granular admin roles](https://www.servicenow.com/docs/access?context=granular-admin-roles&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Public Sector Digital Services features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Enhancements to Grants Management: Program Setup](https://www.servicenow.com/docs/access?context=psds-using-grants-management-playbook&family=zurich&ft:locale=en-US)**

In the Grants Management: program setup, grant program managers can now add new points of contact for the applicants to the grants program in the Define Program stage. In the Publish Program stage, new fields have been added for program announcement removal. Grants program managers can now set grants programs to auto-remove at a defined date, and set application close to disable new applications from being submitted through the Grants Management portal.

-   **[Enhancements to Grants Management portal](https://www.servicenow.com/docs/access?context=psds-gmp-using-grants-mgmt-portal&family=zurich&ft:locale=en-US)**

Enable grant program managers to turn off new grant proposal submissions after the proposal close date. Applicants can no longer submit proposals after the proposal close date, keeping the process on schedule and helping prevent late submissions from being reviewed.

Enable applicants to review and download the results letter and merit review summary \(where applicable\) of their grants application, as well as accept or decline their award, all within the new **Results** tab of the Grants Management portal. Notify constituents about a pending award decision through the portal.


-   **[Constituent Service Dashboard Migration to Platform Analytics](https://www.servicenow.com/docs/access?context=constituent-services-dashboard&family=zurich&ft:locale=en-US)**

The Constituent Service Dashboard has been migrated to Next Experience Platform Analytics. Next Experience is a ServiceNow AI Platform® feature that is active by default when you load or upgrade to the Zurich release. The dashboard migration to Next Experience enables you to visualize historical and real-time process statistics in role-based dashboards. Access the new dashboard by navigating to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.


</td></tr><tr><td>

Australia

</td><td>

-   **[Large language models on the ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=australia&ft:locale=en-US)**

/

-   **[Now Assist &gt; ServiceNow Otto® announcement](https://www.servicenow.com/docs/access?context=sn-ai-implementation-landing&family=australia&ft:locale=en-US)**



-   **[Enhancements to Grants Management: Program Setup](https://www.servicenow.com/docs/access?context=psds-using-grants-management-playbook&family=australia&ft:locale=en-US)**
    -   [Grants Management Program Budget activity](https://www.servicenow.com/docs/access?context=psds-using-grants-management-playbook&family=australia&ft:locale=en-US)

Use the restructured Program Budget step that is now organized into three sections: Program Budget, Budget Categories, and Award Allocation. Grant Program Managers can select from three award models—Single Award, Multiple Equal Awards, or Multiple Variable Awards—with budgets automatically derived from the Awards category. Real-time calculations update the Budget allocated and Balance left fields as you enter category percentages. This enhancement prevents completion until all of the program budget is allocated across the categories.

    -   [Grants Management Setup](https://www.servicenow.com/docs/access?context=psds-using-grants-management-playbook&family=australia&ft:locale=en-US)

Disable the six-step grant program lifecycle stepper at the instance level, reducing ambiguity about grant program state. By default, the stepper indicating the Preparing Program, Accepting Proposals, Evaluating, Awarding, Post-Award, and Closed states is hidden in the Grant Program record page and admins can enable it if required for deployments that follow a batch or competitive grant lifecycle. When turned off, program state is conveyed through existing status fields.

-   **[Enhancements to Grants Management: Proposal Playbook](https://www.servicenow.com/docs/access?context=psds-using-grants-management-playbook&family=australia&ft:locale=en-US)**
    -   [Grants Management Screen activity](https://www.servicenow.com/docs/access?context=psds-using-grants-management-playbook&family=australia&ft:locale=en-US)

Flag and route a document back to the applicant while reviewing the proposal details in the screening step. The document persists in the Flagged section with all metadata intact. Grant program managers and Grant program directors can reverse the flag by selecting the reset status icon to move it back to Requires Verification with no data loss. Select Request Documents at the bottom of the Verify Documents screen to route flagged documents back to applicants automatically; this action creates a case task assigned to the applicant, sends a notification in the applicant portal prompting re-upload, and changes the document status to Pending Resubmission. Once the applicant uploads the corrected document, the Upload Additional Documents activity closes and you can continue verification, maintaining a complete audit trail throughout the process.

-   ****

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Public Sector Digital Services features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Public Sector Digital Services features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Public Sector Digital Services.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Install Public Sector Digital Services applications by requesting them from the ServiceNow Store. For details on installing the applications, see [Configure](https://www.servicenow.com/docs/access?context=configuring-public-sector-digital-services&family=zurich&ft:locale=en-US). 

</td></tr><tr><td>

Australia

</td><td>

Install Public Sector Digital Services by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Public Sector Digital Services we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Public Sector Digital Services we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Public Sector Digital Services, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   ****

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Public Sector Digital Services we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Public Sector Digital Services we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   Create funding programs to establish top-level budgets and timelines that flow down to associated grant programs.
-   Simplify and streamline the grant application decisions​ with Grants Management:​ Evaluation &amp; Decision.
-   Enable merit reviewers to track, score, and monitor grant applications via a dedicated Reviewer Service portal.
-   Enable applicants to review and download the results letter and merit review summary of their grants application, and accept or decline their award, all within the new **Results** tab of the Grants Management portal.
-   Define fees for and autonomously assess fee waivers against agency-defined criteria for information requests with the Help manage public information requests agentic AI Agent, part of the Public Sector Digital Services AI Agent Collection application.

 See [Public Sector Digital Services](https://www.servicenow.com/docs/access?context=bun-public-sector-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Manage field operations and view/create investigative tasks directly within the case context using the Tasks tab, found within an ICM investigative case record. Use the **Create Work Order** button to allow a case to be escalated to an Field Service Management work order without leaving the ICM workspace.
-   ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Public Sector Digital Services \(PSDS\). Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.
-   Control the visibility of the grant program lifecycle stepper on the Grant Program record page by disabling or enabling it per instance.
-   Route flagged documents back to applicants, prompting re-upload of the corrected document, maintaining a complete audit trail within the system. Flagged documents now persist in the system rather than being deleted immediately.
-   Enter award information and allocate budget across categories using the restructured Program Budget activity. The new three-section workflow separates total program budget, budget categories, and award allocation types for a clearer, more intuitive budget configuration experience. Budget allocations and balances update in real-time as you enter percentages across categories.
-   Enable other governments to launch citizen-facing services using the GOV.UK Developer Toolkit, a library of reusable portal widgets that follow UK GDS guidelines, enabling ServiceNow developers to build compliant service portals for UK government customers.

-   Submit funding and decline recommendations, as a Grant Program Manager for any scored subset of proposals as a Funding Allocation Request, enabling incremental funding decisions without waiting for the entire portfolio to complete review. The Grant Program Director can approve or reject each request, with rejected proposals returning to the working queue for future consideration.
-   Release result letters per proposal as each Funding Allocation Request decision is approved, rather than waiting for all decisions across the program to be finalized. This enables rolling notification of award, decline, or ineligibility outcomes in Grants Management.

-   Consolidate the case narrative, evidence, entities, team assignments, investigative tasks, and related cases into a single record page with Investigative Case Management Foundation.
-   Manage persons, property, vehicles, organizations, locations, and events, including specialized entity types like firearms with detailed identification, specifications, origin, and ballistic information, and link them to cases and to each other with Investigative Case Management Entity Management.
-   Manage physical and digital evidence tied to investigative cases, with structure fields for collection details, source and context, security classification, and links to related entities such as persons, vehicles, locations, and organizations using Investigative Case Management Evidence Management.
-   Create Chain of custody documentation in every evidence record, capturing each transfer from the moment of collection.
-   Synthesize narratives, entities, evidence, and activity history into a structured summary using Investigative Case Management Case Summarization.
-   Validate large volumes of uploaded documents, verify information, flag issues, and highlight key details for case agents with the Document Screening Al Skill, used with ServiceNow Otto for Public Sector Digital Services \(PSDS\).

 See [Public Sector Digital Services \(PSDS\)](https://www.servicenow.com/docs/access?context=bun-public-sector-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

