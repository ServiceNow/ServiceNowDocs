---
title: Third-party Risk Management release notes
description: The ServiceNow Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk, and performing remediation. TPRM was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
---

# Third-party Risk Management release notes

The ServiceNow® Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk, and performing remediation. TPRM was enhanced and updated in the Xanadu release.

## Third-party Risk Management highlights for the Xanadu release

-   Collect, monitor, and assess third-party elements for engagements.
-   Request risk intelligence reports \(RIR\) and scores so that you can manage and monitor your RIR requests all within TPRM.
-   View the Third-party Risk Management data model.
-   Use the Digital resilience third-party registers application to create, update, and track records for digital resilience third-party registers.

See [Third-party Risk Management](https://www.servicenow.com/docs/access?context=third-party-risk-mgt-landing-page&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** Third-party Risk Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Third-party Risk Management to Xanadu

If you are a VRM user upgrading to TPRM, when upgrading to Vancouver or later from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. This means upgrading from Utah to Vancouver, Vancouver to Washington DC, and so on. If the scripts do not run in the correct order, it can result in data inconsistencies, broken functionalities, and conflicts.

For more information on upgrading from VRM to TPRM, see [Third-party Risk Management upgrade information](grc-tprm-upgrade-info.md).

## New in the Xanadu release

-   **[Third-party element collection](https://www.servicenow.com/docs/access?context=tprm-monitor-tp-elements&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Confirm that third-party elements adhere to the same security and compliance standards as an engagement by monitoring them through TPRM. Use this data to help identify, assess, and manage the risks that are related to your engagements that depend on third-party elements.

-   **[Risk intelligence report requests](https://www.servicenow.com/docs/access?context=tprm-riskintel-using&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Make informed decisions about working with an engagement or third party by requesting and managing risk intelligence reports or scores from external risk intelligence content providers using the Third-party Risk Management application.

-   **[Third-party risk management data model](https://www.servicenow.com/docs/access?context=tprm-data-model&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Take full advantage of Third-party Risk Management by viewing its data model to see how you can best use it to assess, monitor, and mitigate the risks that are required for your risk management program.

-   **[Digital resilience third-party registers](https://www.servicenow.com/docs/access?context=tprm-dora&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Create, update, and track records for digital resilience third-party registers by using the Digital resilience third-party registers application within the Vendor Management Workspace Vendor Management Workspace. You can bulk create or edit individual records for assessments, branches, contracts, functions, legal entities, supply chains, third parties, or third-party engagements using the Excel download/upload requests feature. This application helps you maintain records with information and communication technology \(ICT\) third-party service providers, helping ensure compliance with the Digital Operational Resilience Act \(DORA\).


## UI changes

-   **[Using digital resilience third-party registers](https://www.servicenow.com/docs/access?context=tprm-dora&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    The Digital resilience third-party registers module is now included in the List view of the Vendor Management Workspace.


## Deprecations

-   **[Reminder workflows](https://www.servicenow.com/docs/access?context=tprm-workflow-in-workspace&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Starting with version 19.1.x of the Third-party Risk Management application, the tiering questionnaire and external assessment reminders workflows are deprecated and migrated to Workflow Studio. If you have customized these workflows, they won’t be deprecated or migrated as part of this change.


## Activation information

Install Third-party Risk Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

[Quick start tests for TPRM](https://www.servicenow.com/docs/access?context=quick-start-tests-grc-vrm&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US). After upgrades and deployments of new applications or integrations, run quick start tests to verify that TPRM works as expected. If you customized TPRM, copy the quick start tests and configure them for your customizations.

## Accessibility information

Accessibility improvements for the Third-party Risk Management application include the following updates.

-   Keyboard focus: Improved visual accessibility in the Third-party portal by increasing contrast between the focus border and white background.
-   Screen reader support has been extended to announce the following:
    -   Completed status after all questions have been completed in a section of an external questionnaire in the Third-party portal.
    -   Correct labels and other relevant information for controls, images, card regions, menu items, and links in the Vendor Management Workspace.

## Related ServiceNow applications and features

-   **[Operational Resilience](https://www.servicenow.com/docs/access?context=grc-opres-landing-page&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Operational Resilience helps organizations respond to adverse operational events by anticipating, preventing, recovering from, and adapting to such events.

-   **[Operational Resilience Workspace](https://www.servicenow.com/docs/access?context=working-in-opres-ws&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Use Operational Resilience Workspace to manage your resilience tasks and monitor resilience metrics from a single dashboard.

-   **[GRC Risk Management](https://www.servicenow.com/docs/access?context=grc-risk-overview&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Use Risk Management with the ServiceNow® Advanced Risk application to identify and monitor high-impact risks, improve your risk-based decision-making, and reduce your reaction time from days to minutes.

-   **[GRC Risk Workspace](https://www.servicenow.com/docs/access?context=risk-workspace&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    The Risk Workspace in the ServiceNow® Advanced Risk application provides a simplified user experience with a single-pane view for risk-related activities.


-   **[Third-party Risk Management upgrade information](grc-tprm-upgrade-info.md)**  
ServiceNow® Third-party Risk Management application upgrade information for the Xanadu release.

**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

