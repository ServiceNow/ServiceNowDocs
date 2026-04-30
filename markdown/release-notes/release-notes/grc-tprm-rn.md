---
title: Third-party Risk Management release notes
description: The ServiceNow Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk, and performing remediation. TPRM was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
---

# Third-party Risk Management release notes

The ServiceNow® Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk, and performing remediation. TPRM was enhanced and updated in the Yokohama release.

## Third-party Risk Management highlights for the Yokohama release

-   Pre-populate questionnaires for entities and engagements that are associated with the same active third party by using responses from complete questionnaires.
-   Respond to questionnaires by using a Microsoft Excel questionnaire template.
-   Explore and analyze assessment data at various levels by using the Third-party insights dashboard and the TPRM custom analytics dashboard.
-   Stay aligned with stricter regulatory compliance and emerging third-party risk governance by using the new Standardized Information Gathering \(SIG\) questionnaire content available for 2025.

See [Third-party Risk Management](https://www.servicenow.com/docs/access?context=third-party-risk-mgt-landing-page&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** Third-party Risk Management is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Third-party Risk Management to Yokohama

Starting with the Vancouver release, if you’re a VRM user upgrading to TPRM, from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. This means upgrading from one release to the next rather than skipping to the latest release. Not running scripts in the correct order can result in data inconsistencies, broken functionalities, and conflicts.

For more information on upgrading from VRM to TPRM, see [Third-party Risk Management upgrade information](grc-tprm-upgrade-info.md).

For existing TPRM customers, after upgrading to version 20.2.4, data from the Industry column in the Company \[core\_company\] table is automatically migrated to the tprm\_industry column. Migration can take several hours depending on the number of records in the Company \[core\_company\] table. After migration, a system log message confirms that the migration is complete. Review the Company \[core\_company\] table content and update any customizations referencing the Industry field to use tprm\_industry. After verifying the migration and updating customizations, you can drop the Industry column.

## New in the Yokohama release

-   **[TPRM personalized dashboards](https://www.servicenow.com/docs/access?context=tprm-monitor-dashboards&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Improve your decision-making process by exploring and analyzing your assessment data at various levels by using the Third-party insights dashboard and the TPRM custom analytics dashboard. If you have the Third-party risk manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] or Third-party risk assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role, you can create and share your own dashboards and reports. If you're a third-party risk manager, you can also customize the report layouts, widgets, and data views to prioritize key metrics and workflows that align with your individual roles and risk programs.

-   **[New Standardized Information Gathering \(SIG\) questionnaire content](https://www.servicenow.com/docs/access?context=grc-sig-integration&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Use the updated SIG templates for 2025 after upgrading to version 20.1.x as part of the Third-party Risk Management application. The latest SIG questionnaires help your organization stay aligned with stricter regulatory compliance and emerging third-party risk governance, covering a wide range of security and privacy concerns.

-   **[Quick start tests for TPRM](https://www.servicenow.com/docs/access?context=quick-start-tests-grc-vrm&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Verify that TPRM works as expected after upgrades and deployments of new applications or integrations by running quick start tests. If you customized TPRM, copy the quick start tests and configure them for your customizations.


## UI changes

-   **[TPRM personalized dashboards](https://www.servicenow.com/docs/access?context=tprm-monitor-dashboards&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    The Third-party insights dashboard and the TPRM custom analytics dashboard are now available from the Dashboards page of the Vendor Management Workspace.

-   **[Third-party portal import modal](https://www.servicenow.com/docs/access?context=tprm-excel-template-support&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    The import modal now enables you to respond to questionnaires by using a Microsoft Excel template. You can download the questionnaire, complete it according to the included instructions, and import the final version into the Third-party portal.


## Changed in this release

-   **[Pre-populate responses using questionnaires](https://www.servicenow.com/docs/access?context=tprm-assessing-tpr&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    If you have the Third-party risk assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] or Third-party risk manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] role, you can enable third-party and engagement contacts to review and update responses only if necessary by pre-populating questionnaires for engagements and entities with responses from completed questionnaires that are associated with the same third party. The attachment, duration, and signature type responses are excluded. This feature also helps ensure data consistency and accuracy.

-   **[Microsoft Excel questionnaire template](https://www.servicenow.com/docs/access?context=tprm-excel-template-support&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Streamline the due diligence process by enabling third-party and engagement contacts to respond to questionnaires using a Microsoft Excel template by downloading the questionnaire as a template, completing it according to the included instructions, and importing the final version into the Third-party portal. This feature update enhances flexibility by enabling third-party and engagement contacts to provide information outside the third-party portal. Third-party risk assessors \[sn\_vdr\_risk\_asmt.vendor\_assessor\] and Third-party risk managers \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] can access this feature and respond to questionnaires on behalf of Third-party and engagement contacts through the Vendor Management Workspace.

-   **[Codes and additional identification information for ICT third-party service providers](https://www.servicenow.com/docs/access?context=tprm-create-ICT-thirdparty-serv-prov-form&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\], help ensure compliance with DORA regulations by adding additional code types and a legal name to third-party and third-party engagement records in the digital resilience third-party registers within the Vendor Management Workspace. Include this information when the legal name of a third party differs from its commonly recognized name, or when you need to record multiple identification codes like a EUID, LEI, or Country code. When supply chain, assessment, or contract records are associated with a third party or third-party engagement using the EUID code type, all relevant fields will be automatically populated.

-   **[Function types for ICT third-party service providers](https://www.servicenow.com/docs/access?context=tprm-create-new-function-form&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\], help ensure compliance with DORA regulations by using Business capability as an additional function type for function records in the digital resilience third-party registers within the Vendor Management Workspace.

-   **[Multiple legal entities making use of the services for contracts](https://www.servicenow.com/docs/access?context=tprm-drtp-reg-contract&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\], add multiple legal entities that are using services as part of a contract record in the digital resilience third-party registers within the Vendor Management Workspace. Including all entities that are using services associated with a contract is essential for maintaining transparency, helping ensure compliance, and enhancing operational resilience.


## Activation information

Install Third-party Risk Management by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Operational Resilience](https://www.servicenow.com/docs/access?context=grc-opres-landing-page&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Operational Resilience helps organizations respond to adverse operational events by anticipating, preventing, recovering from, and adapting to such events.

-   **[Operational Resilience Workspace](https://www.servicenow.com/docs/access?context=working-in-opres-ws&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Use Operational Resilience Workspace to manage your resilience tasks and monitor resilience metrics from a single dashboard.

-   **[GRC Risk Management](https://www.servicenow.com/docs/access?context=grc-risk-overview&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Use Risk Management with the ServiceNow® Advanced Risk application to identify and monitor high-impact risks, improve your risk-based decision-making, and reduce your reaction time from days to minutes.

-   **[GRC Risk Workspace](https://www.servicenow.com/docs/access?context=risk-workspace&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    The Risk Workspace in the ServiceNow® Advanced Risk application provides a simplified user experience with a single-pane view for risk-related activities.


-   **[Third-party Risk Management upgrade information](grc-tprm-upgrade-info.md)**  
ServiceNow® Third-party Risk Management application upgrade information for the Yokohama release.

**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

