---
title: Third-party Risk Management release notes
description: The ServiceNow Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk and performing remediation. TPRM was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
---

# Third-party Risk Management release notes

The ServiceNow® Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk and performing remediation. TPRM was enhanced and updated in the Australia release.

## Third-party Risk Management highlights for the Australia release

-   Enhance DORA Register of Information reporting with optional currency conversion and third‑party expense aggregation to generate consistent, regulator‑ready reports.
-   Review the simplified third‑party elements process in the due diligence workflow.
-   Access the unified content management module in the Vendor Management Workspace to view a centralized library of smart assessment templates.

[Early availability](../quality/australia-all-other-fixes.md)

Use generative AI to recommend TPRM issues for reviewer validation.

[Australia Patch 1](../quality/australia-patch-1.md)

Review the updated AI experience with three licensing tiers.

See [Third-party Risk Management](https://www.servicenow.com/docs/access?context=third-party-risk-mgt-landing-page&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** Third-party Risk Management is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Third-party Risk Management to Australia

If you’re a VRM user upgrading to TPRM and upgrading to Australia from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. For example, you must upgrade from Xanadu to Yokohama, Yokohama to Zurich, and so on. If the scripts don’t run in the correct order, you can get data inconsistencies, broken functionalities, and conflicts.

After upgrading to version 21.0.x, you can enable the Smart Assessment Engine \(SAE\) by setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property. After setting this property, Smart Assessment Engine \(SAE\) becomes the default assessment engine and replaces the legacy experience. The transition isn’t reversible.

**Warning:**

Set this property in your non-production instances and conduct thorough testing before changing your production instances. Failure to do so may result in unexpected issues.

For more information on upgrading from VRM to TPRM and the differences between the Smart and Classic Assessment engines, see [Third-party Risk Management upgrade information](grc-tprm-upgrade-info.md).

For existing TPRM customers, after upgrading to version 21.0.3, data from the Industry column in the Company \[core\_company\] table is automatically migrated to the tprm\_industry column. Migration can take several hours depending on the number of records in the Company \[core\_company\] table. After migration, a system log message confirms that the migration is complete. Review the Company \[core\_company\] table content and update any customizations referencing the Industry field to use tprm\_industry. After verifying the migration and updating customizations, you can drop the Industry column.

## New in the Australia release

-   **[Generate aggregate regulatory reports in local currencies](https://www.servicenow.com/docs/access?context=tprm-dora-currency-aggregation&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

    After upgrading the Digital Resilience Third-party Information Register application to version 22.0.3, third‑party risk \(TPR\) managers  \[sn\_vdr\_risk\_asmt.vendor\_manager\] can standardize annual expense values during Register of Information report generation by enabling currency conversion and third‑party total expense aggregation. To support this process, the generated reporting package includes summary and detail reports that indicate successful conversions, aggregation results, and any skipped providers.

-   **[Centralized repository for TPRM SAE templates](https://www.servicenow.com/docs/access?context=tprm-integrating-ucm&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

    After upgrading to version 22.0.2 and installing the Unified Content Management application, TPR managers \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] can help ensure consistent and comprehensive assessments by activating and updating ready‑to‑use Smart Assessment Engine questionnaire templates through a single, managed repository in the Vendor Management Workspace.


-   **[Generate issue recommendations for TPRM](https://www.servicenow.com/docs/access?context=create-recommendation-tprm-issue&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

    After upgrading to version 22.0.8 if you have the third‑party assessment reviewer role \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] and have installed the Now Assist for Third-party Risk Management \(TPRM\) application, you can use generative AI to automatically identify and recommend issues based on assessment responses. The TPRM issue management recommendation skill recommends issues with rationalized summaries. Recommended issues are presented for review and are created as standard TPRM issues only after user confirmation.


## UI changes

-   **[Fields added to Create New Excel download/upload request form](https://www.servicenow.com/docs/access?context=tprm-create-report-aggregate-expenses&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

    After upgrading the Digital Resilience Third-party Information Register application to version 22.0.3, the **Enable currency conversion** and **Enable third‑party total expense aggregation** fields are available on the Excel download/upload request page. When creating Excel Master Template or Plain‑CSV Reporting Package requests, you can configure these options directly on the form.

-   **[TPRM Unified content management page](https://www.servicenow.com/docs/access?context=tprm-ws-ucm-page&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

    After upgrading to version 22.0.2 and installing the Unified Content Management application, the unified content management module is available in the Vendor Management Workspace.


## Changed in this release

-   **[Simplified third-party element process](https://www.servicenow.com/docs/access?context=tprm-workflow-in-workspace&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

    After upgrading to version 22.0.1, third‑party elements are now linked to a single third party and can no longer be shared across third parties. Scoring rollups calculate results from element‑level assessments rather than entity records.


-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


## Removed in this release

Assessments using entities are no longer supported.

## Activation information

Install Third-party Risk Management by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Operational Resilience](https://www.servicenow.com/docs/access?context=grc-opres-landing-page&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

    Operational Resilience helps organizations respond to adverse operational events by anticipating, preventing, recovering from, and adapting to such events.

-   **[Operational Resilience Workspace](https://www.servicenow.com/docs/access?context=working-in-opres-ws&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

    Use Operational Resilience Workspace to manage your resilience tasks and monitor resilience metrics from a single dashboard.

-   **[GRC Risk Management](https://www.servicenow.com/docs/access?context=grc-risk-overview&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

    Use Risk Management with the ServiceNow® Advanced Risk application to identify and monitor high-impact risks, improve your risk-based decision-making, and reduce your reaction time from days to minutes.

-   **[GRC Risk Workspace](https://www.servicenow.com/docs/access?context=risk-workspace&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

    The Risk Workspace in the ServiceNow® Advanced Risk application provides a simplified user experience with a single-pane view for risk-related activities.

-   **[Smart Assessment Engine](https://www.servicenow.com/docs/access?context=smart-asmnt-engine-landing-page&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

    The ServiceNow® Smart Assessment Engine \(SAE\) application helps you to reduce the manual burden and costs of your assessment processes through automation.


-   **[Third-party Risk Management upgrade information](grc-tprm-upgrade-info.md)**  
ServiceNow® Third-party Risk Management application upgrade information for the Australia release.

**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

