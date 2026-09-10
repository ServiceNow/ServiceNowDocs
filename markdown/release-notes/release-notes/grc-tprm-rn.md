---
title: Third-party Risk Management release notes
description: The ServiceNow Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk, and performing remediation. TPRM was enhanced and updated in the Yokohama release.ServiceNow Third-party Risk Management application upgrade information for the Yokohama release.The ServiceNow Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk, and performing remediation. TPRM was enhanced and updated in the Yokohama release.The ServiceNow Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk, and performing remediation. TPRM was enhanced and updated in the Yokohama release.The ServiceNow Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk, and performing remediation. TPRM was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: topic
last_updated: "2025-01-30"
reading_time_minutes: 8
---

# Third-party Risk Management release notes

The ServiceNow® Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk, and performing remediation. TPRM was enhanced and updated in the Yokohama release.

## About Third-party Risk Management

-   Pre-populate questionnaires for entities and engagements that are associated with the same active third party by using responses from complete questionnaires.
-   Respond to questionnaires by using a Microsoft Excel questionnaire template.
-   Explore and analyze assessment data at various levels by using the Third-party insights dashboard and the TPRM custom analytics dashboard.
-   Stay aligned with stricter regulatory compliance and emerging third-party risk governance by using the new Standardized Information Gathering \(SIG\) questionnaire content available for 2025.

See  for more information.

## Activation and other requirements

**Important:** Third-party Risk Management is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Third-party Risk Management by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    Starting with the Vancouver release, if you’re a VRM user upgrading to TPRM, from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. This means upgrading from one release to the next rather than skipping to the latest release. Not running scripts in the correct order can result in data inconsistencies, broken functionalities, and conflicts.

    For more information on upgrading from VRM to TPRM, see [Third-party Risk Management upgrade information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/grc-tprm-rn.md).

    For existing TPRM customers, after upgrading to version 20.2.4, data from the Industry column in the Company \[core\_company\] table is automatically migrated to the tprm\_industry column. Migration can take several hours depending on the number of records in the Company \[core\_company\] table. After migration, a system log message confirms that the migration is complete. Review the Company \[core\_company\] table content and update any customizations referencing the Industry field to use tprm\_industry. After verifying the migration and updating customizations, you can drop the Industry column.


**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/grc-rn-landing.md)

## Third-party Risk Management upgrade information

ServiceNow® Third-party Risk Management application upgrade information for the Yokohama release.

### Important information for upgrading Vendor Risk Management to Yokohama

Starting with the Vancouver release, if you’re a VRM user upgrading to TPRM, from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. This means upgrading from one release to the next rather than skipping to the latest release. Not running scripts in the correct order can result in data inconsistencies, broken functionalities, and conflicts.

### Plugin requirements

TPRM

-   Activate the Third-party Risk Management application \[com.sn\_vdr\_risk\_asmt\].
-   Activate the Third-party Risk Due Diligence application \[com.sn\_tprm\_dd\].
-   Activate the Vendor Risk Management Workspace application \[sn\_vrm\_ws\] if you want to use the Vendor Risk Management workspace.

VRM

-   Activate the Vendor Risk Management application \[com.sn\_vdr\_risk\_asmt\].
-   Activate the Vendor Risk Management Workspace application \[sn\_vrm\_ws\] if you want to use the Vendor Risk Management workspace.

For more information on licensing or metering, see , [Third-party Risk Management \(TPRM\) Licensing](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1431058) and [Vendor Risk Management \(VRM\) Licensing](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1362674).

### VRM to TPRM changes

-   The name of the application changed from Vendor Risk Management to Third-party Risk Management as part of the Vancouver release.
-   The internal assessment \[sn\_vdr\_asmt\_internal\_assessment\] table is introduced, extending the tiering assessment \[sn\_vdr\_risk\_asmt\_vdr\_tiering\_assessment\] table.
-   The Due Diligence Review \(DDR\) workflow is introduced, which uses both the internal assessment and the external \(VRA\) assessment.

    **Note:** If you have customizations on the Tiering assessment \[sn\_vdr\_risk\_asmt\_vdr\_tiering\_assessment\] and VRA \[sn\_vdr\_risk\_asmt\_assessment\] tables, they might need modifications to work with the DDR workflow.

-   The Third-party Scores \[sn\_vdr\_risk\_asmt\_security\_score\] table has been relabeled to Risk Intelligence Scores \[sn\_vdr\_risk\_asmt\_security\_score\] to reduce confusion.
-   All instances of “vendor” are changed to “third party” in the user interface, though some global instances might remain unchanged.

    **Note:** If you don’t want to use the due diligence workflow, your original workflow \(Tiering assessment and External assessments \(VRAs\) should be the same\).


### VRM and TPRM data model

The Vendor Risk Management data model primarily uses the term “vendor” and includes the Tiering assessment \[sn\_vdr\_risk\_asmt\_vdr\_tiering\_assessment\] and VRA \[sn\_vdr\_risk\_asmt\_assessment\] tables.

The Third-party Risk Management data model uses the term “third-party” in most user interface elements and introduces the DDR workflow, which uses both internal \[sn\_vdr\_asmt\_internal\_assessment\] and \[sn\_vdr\_risk\_asmt\_assessment\] external assessments.

The following models show VRM's and TPRM's capabilities.

\[Omitted image "vrm-data-model.png"\] Alt text: Relationship Vendor risk management main tables. For a text description, see the text that preceded and follows this data model.

The components included in the Vendor Risk Management data model are as follows:

-   Tiering assessment \[sn\_vdr\_risk\_asmt\_vdr\_tiering\_assessment\]
-   Company \[core\_company\]
-   Vendor risk assessment \[sn\_vdr\_risk\_asmt\_assessment\]
-   Vendor engagement \[sn\_vdr\_risk\_asmt\_vendor\_engagement\]
-   Vendor contact \[vm\_dr\_contact\]
-   Assessment metric type \[asmt\_metric\_type\]
-   Assessment template \[sn\_vdr\_risk\_asmt\_assessment\_template\]
-   Engagement risk scoring rule \[sn\_vdr\_risk\_asmt\_engagement\_risk\_scoring\_rule\]
-   Engagement level risk rating \[sn\_vdr\_risk\_asmt\_engagement\_level\_rating\]

\[Omitted image "tprm-data-model-upgrade.png"\] Alt text: Relationship between due diligence, and third-party management main tables. For a text description, see the text that preceded and follows this data model.

The components included in the Third-party Risk Management data model are as follows:

-   Risk intelligence score \[sn\_vdr\_risk\_asmt\_security \_score\]
-   Internal assessment \[sn\_vdr\_asmt\_internal\_assessment\]
-   Tiering assessment \[sn\_vdr\_risk\_asmt\_vdr\_tiering\_assessment\]
-   Event-driven management history \[sn\_tprm\_dd\_rule\_execution\_history\]
-   Third-party due diligence request \[sn\_tprm\_dd\_request\]
-   Company \[core\_company\]
-   Event-driven management rule \[sn\_tprm\_dd\_generation\_rule\]
-   Third-party risk assessment \[sn\_vdr\_risk\_asmt\_assessment\]
-   Third-party engagement \[sn\_vdr\_risk\_asmt\_vendor\_engagement\]
-   Vendor contact \[vm\_dr\_contact\]
-   Assessment metric type \[asmt\_metric\_type\]
-   Assessment template \[sn\_vdr\_risk\_asmt\_assessment\_template\]
-   Third-party risk issue \[sn\_vdr\_risk\_asmt\_issue\]
-   Engagement risk scoring rule \[sn\_vdr\_risk\_asmt\_engagement\_risk\_scoring\_rule\]
-   Engagement level risk rating \[sn\_vdr\_risk\_asmt\_engagement\_level\_rating\]

## May 2025

The ServiceNow® Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk, and performing remediation. TPRM was enhanced and updated in the Yokohama release.

### What's new

-   **New Standardized Information Gathering \(SIG\) questionnaire content**

    Use the updated SIG templates for 2025 after upgrading to version 20.1.x as part of the Third-party Risk Management application. The latest SIG questionnaires help your organization stay aligned with stricter regulatory compliance and emerging third-party risk governance, covering a wide range of security and privacy concerns.


### What's changed

-   **Multiple legal entities making use of the services for contracts**

    If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\], add multiple legal entities that are using services as part of a contract record in the digital resilience third-party registers within the Vendor Management Workspace. Including all entities that are using services associated with a contract is essential for maintaining transparency, helping ensure compliance, and enhancing operational resilience.


## Yokohama General Availability

The ServiceNow® Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk, and performing remediation. TPRM was enhanced and updated in the Yokohama release.

### What's changed

-   **Codes and additional identification information for ICT third-party service providers**

    If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\], help ensure compliance with DORA regulations by adding additional code types and a legal name to third-party and third-party engagement records in the digital resilience third-party registers within the Vendor Management Workspace. Include this information when the legal name of a third party differs from its commonly recognized name, or when you need to record multiple identification codes like a EUID, LEI, or Country code. When supply chain, assessment, or contract records are associated with a third party or third-party engagement using the EUID code type, all relevant fields will be automatically populated.

-   **Function types for ICT third-party service providers**

    If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\], help ensure compliance with DORA regulations by using Business capability as an additional function type for function records in the digital resilience third-party registers within the Vendor Management Workspace.


## Yokohama

The ServiceNow® Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk, and performing remediation. TPRM was enhanced and updated in the Yokohama release.

### What's new

-   **TPRM personalized dashboards**

    Improve your decision-making process by exploring and analyzing your assessment data at various levels by using the Third-party insights dashboard and the TPRM custom analytics dashboard. If you have the Third-party risk manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] or Third-party risk assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role, you can create and share your own dashboards and reports. If you're a third-party risk manager, you can also customize the report layouts, widgets, and data views to prioritize key metrics and workflows that align with your individual roles and risk programs.

-   **Quick start tests for TPRM**

    Verify that TPRM works as expected after upgrades and deployments of new applications or integrations by running quick start tests. If you customized TPRM, copy the quick start tests and configure them for your customizations.


### What's changed

-   **TPRM personalized dashboards**

    The Third-party insights dashboard and the TPRM custom analytics dashboard are now available from the Dashboards page of the Vendor Management Workspace.

-   **Third-party portal import modal**

    The import modal now enables you to respond to questionnaires by using a Microsoft Excel template. You can download the questionnaire, complete it according to the included instructions, and import the final version into the Third-party portal.


-   **Pre-populate responses using questionnaires**

    If you have the Third-party risk assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] or Third-party risk manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] role, you can enable third-party and engagement contacts to review and update responses only if necessary by pre-populating questionnaires for engagements and entities with responses from completed questionnaires that are associated with the same third party. The attachment, duration, and signature type responses are excluded. This feature also helps ensure data consistency and accuracy.

-   **Microsoft Excel questionnaire template**

    Streamline the due diligence process by enabling third-party and engagement contacts to respond to questionnaires using a Microsoft Excel template by downloading the questionnaire as a template, completing it according to the included instructions, and importing the final version into the Third-party portal. This feature update enhances flexibility by enabling third-party and engagement contacts to provide information outside the third-party portal. Third-party risk assessors \[sn\_vdr\_risk\_asmt.vendor\_assessor\] and Third-party risk managers \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] can access this feature and respond to questionnaires on behalf of Third-party and engagement contacts through the Vendor Management Workspace.


