---
title: Policy and Compliance Management release notes
description: The ServiceNow Policy and Compliance Management application provides a centralized process for creating and managing policies, standards, and internal control procedures that are cross-mapped to external regulations and benchmarks. Policy and Compliance Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# Policy and Compliance Management release notes

The ServiceNow® Policy and Compliance Management application provides a centralized process for creating and managing policies, standards, and internal control procedures that are cross-mapped to external regulations and benchmarks. Policy and Compliance Management was enhanced and updated in the Yokohama release.

## Policy and Compliance Management highlights for the Yokohama release

-   View the compliance score at the entity level based on the hierarchy of entities.
-   Eliminate duplicate citations associated with the authority documents when you download UCF content.
-   Revise your policies and update the policy text periodically by integrating with Microsoft SharePoint.
-   Enable policy owners and reviewers to collaborate, review, and redline policies by using policy authoring and the redlining feature.
-   The Issues widget has been removed from the Compliance Workspace landing page to enhance the performance.
-   Enable data access by implementing Entity-Based Access controls.
-   Recommend similar control objectives using generative AI. You can then retain, dismiss, or merge duplicate control objectives.

See [Policy and Compliance Management](https://www.servicenow.com/docs/access?context=r_PolicyComplianceMgmt&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** Policy and Compliance Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Calculate compliance score and roll up to entity](https://www.servicenow.com/docs/access?context=compliance-score-calculation-pc-ws&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    View a comprehensive compliance score at the entity level that includes all the child entities rolled up to the parent entity along with the compliance score of the parent entity's direct controls.

-   **[Elimination of duplicate citations from UCF Shared list download](https://www.servicenow.com/docs/access?context=ucf-deduplication-pc&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Eliminate duplicate citations associated with the authority documents when you download UCF content. You can retain one citation as active and mark the duplicate citations as inactive. Move the control objectives of the duplicate citations to the active citation, and update the duplicate citation records with the Source ID of the active citation.

-   **[Improve compliance workspace performance](https://www.servicenow.com/docs/access?context=compliance-manager-compliance-ws&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Improved the performance of the compliance workspace by removing the issue widget to ensure a faster and smoother user experience. You can still access issue details from the "Issues Overview" section.

-   **[Entity based access](https://www.servicenow.com/docs/access?context=c_GRCControls&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Entity based access aims to provide a more granular approach to data access, ensuring that users can only access data through entity-based access. The entity-based access has been enabled for controls, attestations and policy exception to control mappings. Administrators can grant access to an entity's related records by adding users or user groups, or by using entity user fields for entity-based access configuration.

-   **[Deduplication of control objectives](https://www.servicenow.com/docs/access?context=now-assist-for-irm&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Using Generative AI, identify and recommend similar control objectives. You can choose to accept a control objective as duplicate, dismiss those that are not similar, or retain a control objective as primary in which details from all other similar control objectives are merged. Additionally, the system automatically copies related records, including policies and risk statements, to ensure comprehensive information is maintained in one location after retiring the accepted control objectives.


## Changed in this release

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


## Deprecations

GRC DevOps Accelerator is now deprecated and no longer supported or available for new activation. For details, see the [Deprecation process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Activation information

Install Policy and Compliance Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Browser requirements

GRC: Policy and Compliance Management requires the latest public release and two previous release versions of the following browsers:

-   Google Chrome
-   Firefox and Firefox Extended Support Release \(ESR\)
-   Microsoft Edge Chromium
-   Safari 12.0 and later versions

**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

