---
title: Combined Third-party Risk Management release notes for upgrades from Washington DC to Yokohama
description: Consolidated page of all release notes for Third-party Risk Management from Washington DC to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-washingtondc-yokohama/yokohama-washingtondc-thirdpartyriskmanagement-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-24"
reading_time_minutes: 13
breadcrumb: [Products combined by family]
---

# Combined Third-party Risk Management release notes for upgrades from Washington DC to Yokohama

Consolidated page of all release notes for Third-party Risk Management from Washington DC to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Third-party Risk Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Third-party Risk Management to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

If you are a VRM user upgrading to TPRM, when upgrading to Vancouver or later from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. This means upgrading from Utah to Vancouver, Vancouver to Washington DC, and so on. If the scripts do not run in the correct order, it can result in data inconsistencies, broken functionalities, and conflicts.

 For more information on upgrading from VRM to TPRM, see [Third-party Risk Management upgrade information](https://www.servicenow.com/docs/access?context=grc-tprm-upgrade-info&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

Xanadu

</td><td>

If you are a VRM user upgrading to TPRM, when upgrading to Vancouver or later from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. This means upgrading from Utah to Vancouver, Vancouver to Washington DC, and so on. If the scripts do not run in the correct order, it can result in data inconsistencies, broken functionalities, and conflicts.

 For more information on upgrading from VRM to TPRM, see [Third-party Risk Management upgrade information](https://www.servicenow.com/docs/access?context=grc-tprm-upgrade-info&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Starting with the Vancouver release, if you’re a VRM user upgrading to TPRM, from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. This means upgrading from one release to the next rather than skipping to the latest release. Not running scripts in the correct order can result in data inconsistencies, broken functionalities, and conflicts.

 For more information on upgrading from VRM to TPRM, see [Third-party Risk Management upgrade information](https://www.servicenow.com/docs/access?context=grc-tprm-upgrade-info&family=yokohama&ft:locale=en-US).

 For existing TPRM customers, after upgrading to version 20.2.4, data from the Industry column in the Company \[core\_company\] table is automatically migrated to the tprm\_industry column. Migration can take several hours depending on the number of records in the Company \[core\_company\] table. After migration, a system log message confirms that the migration is complete. Review the Company \[core\_company\] table content and update any customizations referencing the Industry field to use tprm\_industry. After verifying the migration and updating customizations, you can drop the Industry column.

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Third-party Risk Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Event-driven management — automate assessment processes](https://www.servicenow.com/docs/access?context=tprm-event-drvn-mgt-rule-create&family=washingtondc&ft:locale=en-US)**

Configure the rules that auto-generate and send questionnaires and document requests to engagements and third parties. For engagements and third parties that meet the criteria you define, you specify the schedule, questionnaire, and document request templates. You can automate all assessment types except onboarding.

-   **[New user group: Due diligence request assigners](https://www.servicenow.com/docs/access?context=tprm-groups-add-users-to&family=washingtondc&ft:locale=en-US)**

Enable each member of the Due diligence request assigners group to receive an email notification of the new requests for due diligence. For requests that are in the **New** or **Unassigned** state, you need to specify the owner. Any group member can assign the owner.

-   **[New reports on the Due diligence management dashboard](https://www.servicenow.com/docs/access?context=tprm-ws-dd-management-reports&family=washingtondc&ft:locale=en-US)**

Use the Due diligence management dashboard, as a third-party risk manager or assessor, to track, prioritize, and manage your responsibilities.

-   **[Tracking a managed activity](https://www.servicenow.com/docs/access?context=tprm-managed-activity&family=washingtondc&ft:locale=en-US)**

View managed activities in the usage analytics activities table for tracking and verification purposes in the Third-party Risk Management application.

-   **[New Standardized Information Gathering \(SIG\) questionnaire content](https://www.servicenow.com/docs/access?context=grc-sig-integration&family=washingtondc&ft:locale=en-US)**

Use the updated SIG templates for 2024 after upgrading to version 18.x as part of the Third-party Risk Management application.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Third-party element collection](https://www.servicenow.com/docs/access?context=tprm-monitor-tp-elements&family=xanadu&ft:locale=en-US)**

Confirm that third-party elements adhere to the same security and compliance standards as an engagement by monitoring them through TPRM. Use this data to help identify, assess, and manage the risks that are related to your engagements that depend on third-party elements.

-   **[Risk intelligence report requests](https://www.servicenow.com/docs/access?context=tprm-riskintel-using&family=xanadu&ft:locale=en-US)**

Make informed decisions about working with an engagement or third party by requesting and managing risk intelligence reports or scores from external risk intelligence content providers using the Third-party Risk Management application.

-   **[Third-party risk management data model](https://www.servicenow.com/docs/access?context=tprm-data-model&family=xanadu&ft:locale=en-US)**

Take full advantage of Third-party Risk Management by viewing its data model to see how you can best use it to assess, monitor, and mitigate the risks that are required for your risk management program.

-   **[Digital resilience third-party registers](https://www.servicenow.com/docs/access?context=tprm-dora&family=xanadu&ft:locale=en-US)**

Create, update, and track records for digital resilience third-party registers by using the Digital resilience third-party registers application within the Vendor Management Workspace Vendor Management Workspace. You can bulk create or edit individual records for assessments, branches, contracts, functions, legal entities, supply chains, third parties, or third-party engagements using the Excel download/upload requests feature. This application helps you maintain records with information and communication technology \(ICT\) third-party service providers, helping ensure compliance with the Digital Operational Resilience Act \(DORA\).


</td></tr><tr><td>

Yokohama

</td><td>

-   **[TPRM personalized dashboards](https://www.servicenow.com/docs/access?context=tprm-monitor-dashboards&family=yokohama&ft:locale=en-US)**

Improve your decision-making process by exploring and analyzing your assessment data at various levels by using the Third-party insights dashboard and the TPRM custom analytics dashboard. If you have the Third-party risk manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] or Third-party risk assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role, you can create and share your own dashboards and reports. If you're a third-party risk manager, you can also customize the report layouts, widgets, and data views to prioritize key metrics and workflows that align with your individual roles and risk programs.

-   **[New Standardized Information Gathering \(SIG\) questionnaire content](https://www.servicenow.com/docs/access?context=grc-sig-integration&family=yokohama&ft:locale=en-US)**

Use the updated SIG templates for 2025 after upgrading to version 20.1.x as part of the Third-party Risk Management application. The latest SIG questionnaires help your organization stay aligned with stricter regulatory compliance and emerging third-party risk governance, covering a wide range of security and privacy concerns.

-   **[Quick start tests for TPRM](https://www.servicenow.com/docs/access?context=quick-start-tests-grc-vrm&family=yokohama&ft:locale=en-US)**

Verify that TPRM works as expected after upgrades and deployments of new applications or integrations by running quick start tests. If you customized TPRM, copy the quick start tests and configure them for your customizations.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Third-party Risk Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Terminated third parties are now available for new DD requests for onboarding](https://www.servicenow.com/docs/access?context=tprm-ws-request-dd-for-engagement&family=washingtondc&ft:locale=en-US)**

You can now reactivate a third party that is in the **Terminated** status. You can select a terminated third party when you’re creating due diligence requests for onboarding new engagements. If such a request is accepted and closed, the third party's status is changed to **Active**.

-   **[New \[sn\_svdp.allow\_assessor\_edit\] property of Third-Party Risk Assessor role](https://www.servicenow.com/docs/access?context=tprm-roles&family=washingtondc&ft:locale=en-US)**

The default setting for the \[sn\_svdp.allow\_assessor\_edit\] property enables Third-party risk assessors \[sn\_vdr\_risk\_asmt.vendor\_assessor\] to answer questions or modify responses in third-party questionnaires. For instructions on setting this property, see [Configure TPRM properties](https://www.servicenow.com/docs/access?context=tprm-properties-configure&family=washingtondc&ft:locale=en-US).

-   **[New \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\] role](https://www.servicenow.com/docs/access?context=tprm-roles&family=washingtondc&ft:locale=en-US)**

The new \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\] role can create and edit questionnaire templates and contains all the permissions of the \[vendor\_risk \_manager\] and \[assessment\_admin\] roles. The permissions for creating and editing questionnaire templates have been removed from the \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\]. For more information, see [Roles in Third-party Risk Management](https://www.servicenow.com/docs/access?context=tprm-roles&family=washingtondc&ft:locale=en-US).

-   **[New Active option](https://www.servicenow.com/docs/access?context=create-tier-based-risk-submission&family=washingtondc&ft:locale=en-US)**

The new Active option enables Third-party risk managers \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] to turn a tier-based assessment submission rule on or off. When all rules are turned off, third-party risk assessments aren’t automatically generated by tier changes. For more information, see [Create an automated risk assessment when the assigned risk tier changes—Legacy process](https://www.servicenow.com/docs/access?context=create-tier-based-risk-submission&family=washingtondc&ft:locale=en-US).

-   **[New configurations automatically attach external questionnaires to assessments](https://www.servicenow.com/docs/access?context=tprm-setup-eq-irq&family=washingtondc&ft:locale=en-US)**

You can now add questionnaires automatically to third-party risk assessments based on the final risk tiers that are calculated at the IRQ assessment or engagement level. This change is in addition to the existing feature that adds questionnaires to the third-party risk assessments in the due diligence workflow based on the responses from the IRQ questionnaire. The level at which the risk tier is calculated can be configured.

-   **[Vendor Risk dashboard in Next Experience UI Framework](https://www.servicenow.com/docs/access?context=using-legacy-ui&family=washingtondc&ft:locale=en-US)**

Starting with version 18.1.3 of the Third-party Risk Management application, the Vendor Risk dashboard is no longer supported as part of the Next Experience UI Framework. The Vendor Risk dashboard is available for existing users that have installed Third-party Risk Management prior to 18.1.3.


</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Pre-populate responses using questionnaires](https://www.servicenow.com/docs/access?context=tprm-assessing-tpr&family=yokohama&ft:locale=en-US)**

If you have the Third-party risk assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] or Third-party risk manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] role, you can enable third-party and engagement contacts to review and update responses only if necessary by pre-populating questionnaires for engagements and entities with responses from completed questionnaires that are associated with the same third party. The attachment, duration, and signature type responses are excluded. This feature also helps ensure data consistency and accuracy.

-   **[Microsoft Excel questionnaire template](https://www.servicenow.com/docs/access?context=tprm-excel-template-support&family=yokohama&ft:locale=en-US)**

Streamline the due diligence process by enabling third-party and engagement contacts to respond to questionnaires using a Microsoft Excel template by downloading the questionnaire as a template, completing it according to the included instructions, and importing the final version into the Third-party portal. This feature update enhances flexibility by enabling third-party and engagement contacts to provide information outside the third-party portal. Third-party risk assessors \[sn\_vdr\_risk\_asmt.vendor\_assessor\] and Third-party risk managers \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] can access this feature and respond to questionnaires on behalf of Third-party and engagement contacts through the Vendor Management Workspace.

-   **[Codes and additional identification information for ICT third-party service providers](https://www.servicenow.com/docs/access?context=tprm-create-ICT-thirdparty-serv-prov-form&family=yokohama&ft:locale=en-US)**

If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\], help ensure compliance with DORA regulations by adding additional code types and a legal name to third-party and third-party engagement records in the digital resilience third-party registers within the Vendor Management Workspace. Include this information when the legal name of a third party differs from its commonly recognized name, or when you need to record multiple identification codes like a EUID, LEI, or Country code. When supply chain, assessment, or contract records are associated with a third party or third-party engagement using the EUID code type, all relevant fields will be automatically populated.

-   **[Function types for ICT third-party service providers](https://www.servicenow.com/docs/access?context=tprm-create-new-function-form&family=yokohama&ft:locale=en-US)**

If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\], help ensure compliance with DORA regulations by using Business capability as an additional function type for function records in the digital resilience third-party registers within the Vendor Management Workspace.

-   **[Multiple legal entities making use of the services for contracts](https://www.servicenow.com/docs/access?context=tprm-drtp-reg-contract&family=yokohama&ft:locale=en-US)**

If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\], add multiple legal entities that are using services as part of a contract record in the digital resilience third-party registers within the Vendor Management Workspace. Including all entities that are using services associated with a contract is essential for maintaining transparency, helping ensure compliance, and enhancing operational resilience.


</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Third-party Risk Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Third-party Risk Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

-   **[Reminder workflows](https://www.servicenow.com/docs/access?context=tprm-workflow-in-workspace&family=xanadu&ft:locale=en-US)**

Starting with version 19.1.x of the Third-party Risk Management application, the tiering questionnaire and external assessment reminders workflows are deprecated and migrated to Workflow Studio. If you have customized these workflows, they won’t be deprecated or migrated as part of this change.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Third-party Risk Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Install TPRM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=washingtondc&ft:locale=en-US).

 [Quick start tests for TPRM.](https://www.servicenow.com/docs/access?context=quick-start-tests-grc-vrm&family=washingtondc&ft:locale=en-US) After upgrades and deployments of new applications or integrations, run quick start tests to verify that TPRM works as expected. If you customized TPRM, copy the quick start tests and configure them for your customizations.

</td></tr><tr><td>

Xanadu

</td><td>

Install Third-party Risk Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

 [Quick start tests for TPRM](https://www.servicenow.com/docs/access?context=quick-start-tests-grc-vrm&family=xanadu&ft:locale=en-US). After upgrades and deployments of new applications or integrations, run quick start tests to verify that TPRM works as expected. If you customized TPRM, copy the quick start tests and configure them for your customizations.

</td></tr><tr><td>

Yokohama

</td><td>

Install Third-party Risk Management by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Third-party Risk Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Third-party Risk Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Third-party Risk Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

Accessibility improvements for the Third-party Risk Management application include the following updates.

-   Keyboard focus: Improved visual accessibility in the Third-party portal by increasing contrast between the focus border and white background.
-   Screen reader support has been extended to announce the following:
    -   Completed status after all questions have been completed in a section of an external questionnaire in the Third-party portal.
    -   Correct labels and other relevant information for controls, images, card regions, menu items, and links in the Vendor Management Workspace.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Third-party Risk Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Third-party Risk Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Automate assessments with the event-driven management feature.
-   View new reports on the Due diligence management dashboard.
-   Track and verify a managed activity.
-   Use the new Standardized Information Gathering \(SIG\) questionnaire content available for 2024.
-   Add questionnaires to third-party risk assessments based on the final risk tiers that were calculated at the IRQ assessment or engagement level.

 See [Third-party Risk Management](https://www.servicenow.com/docs/access?context=third-party-risk-mgt-landing-page&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Collect, monitor, and assess third-party elements for engagements.
-   Request risk intelligence reports \(RIR\) and scores so that you can manage and monitor your RIR requests all within TPRM.
-   View the Third-party Risk Management data model.
-   Use the Digital resilience third-party registers application to create, update, and track records for digital resilience third-party registers.

 See [Third-party Risk Management](https://www.servicenow.com/docs/access?context=third-party-risk-mgt-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Pre-populate questionnaires for entities and engagements that are associated with the same active third party by using responses from complete questionnaires.
-   Respond to questionnaires by using a Microsoft Excel questionnaire template.
-   Explore and analyze assessment data at various levels by using the Third-party insights dashboard and the TPRM custom analytics dashboard.
-   Stay aligned with stricter regulatory compliance and emerging third-party risk governance by using the new Standardized Information Gathering \(SIG\) questionnaire content available for 2025.

 See [Third-party Risk Management](https://www.servicenow.com/docs/access?context=third-party-risk-mgt-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-washingtondc-yokohama/rn-combined-intro.md)

