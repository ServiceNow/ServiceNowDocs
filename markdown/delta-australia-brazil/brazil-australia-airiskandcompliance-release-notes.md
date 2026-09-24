---
title: Combined AI Risk and Compliance release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for AI Risk and Compliance from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-airiskandcompliance-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined AI Risk and Compliance release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for AI Risk and Compliance from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family AI Risk and Compliance release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading AI Risk and Compliance to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Upgrade information**

If you're upgrading from an earlier release, upgrade sequentially through each release rather than skipping versions. Upgrade scripts depend on running in order, and skipping releases can cause data inconsistencies or broken functionality.


</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for AI Risk and Compliance.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Continuous controls monitoring](https://www.servicenow.com/docs/access?context=airc-continuous-controls-monitoring&family=australia&ft:locale=en-US)**

Use Continuous Controls Monitoring to automate control verification and gather real-time visibility into control health. After upgrading to version 22.5.x, users with the AI Risk and Compliance Manager \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager\] role can create a compliance evaluation configuration. Indicators that use metrics from ServiceNow or Traceloop, can run on a schedule and evaluate whether a control associated with the asset is compliant or non-compliant. When an indicator fails, a GRC issue is created so that the product owner of the affected asset can remediate it. Users with the AI Risk and Compliance Analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\] role can access the configurations but can't make changes.

-   **[Risk and compliance tasks for Asset owners in Activity center](https://www.servicenow.com/docs/access?context=aict-activity-center&family=australia&ft:locale=en-US)**

After upgrading to version 22.5.x, if you have the AI Asset Owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role, you can access and act on risk and compliance life cycle tasks, such as impact assessments and control attestations, from the Activity Center in AI Control Tower. The Activity Center surfaces AI asset tasks, issues, policy exceptions, and AI cases for the asset owner. On the asset record page, all life cycle tasks specific to the assigned assets can be accessed and performed.

-   **[AI Risk and Compliance lifecycle tasks in AI Governance](https://www.servicenow.com/docs/access?context=risk-compliance-lifecycle-tasks-aict&family=australia&ft:locale=en-US)**

After upgrading to version 22.5.x, if you have the AI Steward \[sn\_ai\_governance.ai\_steward\] and AI Risk and Compliance Analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\] roles, you can take and manage risk assessments directly from the playbook within the AI Control Tower workspace, without switching between workspaces.


 -   **[Exploring Now Assist in AI Risk and Compliance](https://www.servicenow.com/docs/access?context=airc-exploring-now-assist&family=australia&ft:locale=en-US)**

Use Now Assist for AI Risk and Compliance to get AI-powered assistance throughout the AI asset lifecycle. After upgrading to version 22.4.x, users with the AI Risk and Compliance AI user \[sn\_airc\_gen\_ai.airc\_ai\_user\] and AI Risk and Compliance AI agent user \[sn\_airc\_gen\_ai.airc\_ai\_agent\] roles can access the following capabilities:

    -   Create and document governance, risk, and compliance issues with guided assistance from the employee center.
    -   Generate concise summaries of complex GRC issues for faster review and decision-making.
    -   Create executive summaries of risk assessments to communicate findings to stakeholders.
    -   Generate responses to assessment questions based on past assessments and reference documentation.
    -   Identify related control objectives from your controls library to reduce duplication.
Use these capabilities to capture AI risk context early in the development process and address compliance requirements throughout the system lifecycle.


 -   **[Risk‑based classification during intake](https://www.servicenow.com/docs/access?context=request-ai-system&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.3, if you have the AI risk and compliance business user \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user\] role, you can now classify AI systems using a risk‑based approach at intake, enabling organizations to capture AI risk context early and align governance workflows with regulatory and internal risk requirements. This improvement to the AI use case request form supports more accurate AI oversight throughout the system life cycle.

-   **[Report an AI case anonymously](https://www.servicenow.com/docs/access?context=report-ai-case-anon&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.3, if you have the AI Case Management \(sn\_ai\_case\_mgmt\) application installed and the AI case business user \[sn\_ai\_case\_mgmt.ai\_case\_business\_user\] role, you can navigate to the Employee Center to access the Anonymous Reporting Center and submit AI cases anonymously, enabling broader participation in AI governance while protecting the identity of reporters. No additional role is required to submit an anonymous report directly through the Anonymous Reporting Center. Broader participation helps organizations identify potential AI risks earlier by removing barriers to case submission.

-   **[Offboard AI models and datasets](https://www.servicenow.com/docs/access?context=airc-offboarding-ai-assets&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.3, if you have the AI risk and compliance analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\] or AI risk and compliance manager \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager\] role you can manage AI asset offboarding life cycle tasks. Managing these tasks supports completion of governance-related activities, such as risk and impact assessments, conformity reviews, issue closure, and audit documentation, when an AI asset is retired or removed from active use.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing AI Risk and Compliance features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **AI record labels**

The AI assets \(sn\_grc\_ai\_gov\_ai\_system\) table has been renamed to AI records \(sn\_grc\_ai\_gov\_ai\_system\). Two field labels on AI system, AI model, and dataset record pages in the AI Risk and Compliance Workspace have changed. The **Record type** field now displays **AI record** instead of the previous asset-specific labels. On AI system records, the **Asset type** field has been replaced by **Parent category**, which displays **AI system**.


 -   **[Smart Assessment Engine template versioning](https://www.servicenow.com/docs/access?context=airc-assessment-templates&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.5, if you have the AI risk and compliance admin \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_admin\] role, you can use Smart Assessment templates that support versioning. A new version is created automatically when you edit and save a template. Publishing a new version retires the previously published version. Existing templates are set to Version 1.

-   **[Assessment scope context in task and work queue lists](https://www.servicenow.com/docs/access?context=tasks-ai-risk-compliance&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.5, if you have the AI risk and compliance analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\] or AI risk and compliance manager \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager\] role, assessment task list and work queue views display additional columns that show the governance scope \(related entity such as AI asset, model, or dataset\) of each control attestation-based assessment. These columns let you identify which AI asset, entity, and control an assessment belongs to without opening the individual record.

-   **[Impact assessment field auto-population](https://www.servicenow.com/docs/access?context=airc-intake&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.5, if you have the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] or AI risk and compliance business user \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user\] role, the screening question responses that capture the AI system's intended use and operational context from the Use and Purpose section of the AI use case request form are automatically populated in the corresponding Use and Purpose fields of a new impact assessment. This synchronization reduces manual entry and helps ensure that impact assessment responses are consistent with the information submitted at intake.

-   **[AI Risk and Compliance Content Pack regulatory frameworks](https://www.servicenow.com/docs/access?context=airc-content-pack&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.0, if you have the AI Risk and Compliance Content application installed and the admin role, the AI Risk and Compliance content pack includes additional authority documents, agency mappings, and citations for the following regulatory frameworks: the Transparency in Frontier Artificial Intelligence Act \(SB 53\) and the Colorado Artificial Intelligence Act \(SB 205\). When at least one regulatory framework is activated, control objective records display citations from all activated authority documents in the **Citations** tab. This enables you to assess cross-framework regulatory coverage from a single control objective record without navigating each framework separately.


 -   **[Operations tab](https://www.servicenow.com/docs/access?context=operations-tab&family=australia&ft:locale=en-US)**

On the Operations tab in the AI Risk and Compliance Workspace, the AI systems by state section includes an Offboard state to track AI systems in retirement or offboarding and the AI systems by department section now supports grouping by Risk classification from the Show by drop-down list to view the distribution of AI systems in each department.

-   **[AI use case request form](https://www.servicenow.com/docs/access?context=airc-intake&family=australia&ft:locale=en-US)**

A Use and Purpose section containing screening questions has been added to the AI use case request form to capture contextual information about how an AI system will be used and supports automated risk‑based classification during submission.

-   **[AI system record page](https://www.servicenow.com/docs/access?context=ai-system-airc&family=australia&ft:locale=en-US)**

A Use and Purpose section has been added to the AI system record page, which you can access from the AI asset inventory list in the AI Risk and Compliance Workspace.

-   **[Anonymous AI case reporting](https://www.servicenow.com/docs/access?context=airc-cases-inquiries&family=australia&ft:locale=en-US)**

A Visit Anonymous Reporting Center card is available in the Support resources section of the AI assets page in the Employee Center, enabling you to navigate to the Anonymous Reporting Center to submit an anonymous AI case.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some AI Risk and Compliance features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some AI Risk and Compliance features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate AI Risk and Compliance.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Activation information**

Install AI Risk and Compliance by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Important:** AI Risk and Compliance is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install AI Risk and Compliance by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=brazil&ft:locale=en-US).


**Note:** AI Risk and Compliance is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for AI Risk and Compliance we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for AI Risk and Compliance we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for AI Risk and Compliance, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for AI Risk and Compliance we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for AI Risk and Compliance we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   Manage Smart Assessment templates with versioning support. Create, publish, and delete template versions to support consistent assessment governance.
-   View the related entity \(AI record, model, or dataset\) and control for each control attestation-based assessment directly in task and work queue lists, without opening the individual record.
-   Access authority documents, agency mappings, and citations for additional AI regulatory frameworks in the AI Risk and Compliance content pack.
-   Classify AI systems based on regulatory risk at intake by applying a configured Risk Assessment Methodology \(RAM\), enabling early risk identification and consistent AI governance decisions across the system life cycle.
-   Submit AI cases anonymously to report potential AI risks or concerns without disclosing your identity, helping improve early risk visibility and participation in AI governance.
-   Offboard AI assets with structured life-cycle tasks to support completion of governance and risk activities when systems are retired or replaced.

 See [AI Risk and Compliance](https://www.servicenow.com/docs/access?context=ai-risk-and-compliance&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Assess, score, and monitor risk across your AI assets, from onboarding through deployment, until retirement.
-   Centralize regulatory risk assessments, impact assessments, issue tracking, and remediation in a single workspace.
-   Manage risk and compliance scores for AI assets throughout their life cycle with workflows for ongoing oversight and risk management.
-   Manage conformity of AI assets with global regulations and frameworks.
-   Identify and address potential impacts on privacy, non- discrimination, and other human rights.

 See [Version 23.0.3](https://www.servicenow.com/docs/access?context=airc-rn-2026-09&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

