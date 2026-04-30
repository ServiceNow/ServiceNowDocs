---
title: Policy and Compliance Management release notes
description: The ServiceNow Policy and Compliance Management application provides a centralized process for creating and managing policies, standards, and internal control procedures that are cross-mapped to external regulations and benchmarks. Policy and Compliance Management was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
---

# Policy and Compliance Management release notes

The ServiceNow® Policy and Compliance Management application provides a centralized process for creating and managing policies, standards, and internal control procedures that are cross-mapped to external regulations and benchmarks. Policy and Compliance Management was enhanced and updated in the Zurich release.

## Policy and Compliance Management highlights for the Zurich release

-   Association of citations to controls feature enables users to associate controls with citations directly to avoid duplicated controls and ensure accurate compliance reporting.
-   Multiple enhancements to control objectives rationalization process, including improvements including automatic rationalization process creation, simplified two-step workflow for recommendations, skipped approvals for owner-reviewers, comment capabilities, and improved UI.
-   Now Assist for IRM includes skills and AI agent to identify affected control objectives when citation descriptions change and to provide suggested updates for review and approval.
-   Enhancements to control objectives and controls, including control objective requirements for granular statements, automatic control requirement generation, and attestation at control requirement level.
-   Enhancements to policy exception and extension requests, including approver pop-ups with key details, no indicator tasks for exempt controls, Send Information button for requesters, and expanded linking requirements for issue-based policy exceptions.

See [Privacy Management](https://www.servicenow.com/docs/access?context=privacy-management&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** Policy and Compliance Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Association of citations to controls](https://www.servicenow.com/docs/access?context=citation-to-control-mapping&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    In many compliance frameworks, a single control objective may be referenced by multiple citations across different standards, regulations, or policy requirements. Without proper association management, organizations risk duplicating controls, misinterpreting coverage, or inaccurately reporting compliance. The association of citations to controls feature addresses this challenge by enabling users to associate controls with citations directly. When this feature is enabled, compliance scores update dynamically based on the status of directly associated active controls.


-   **[Enhancements to control objectives rationalization process](https://www.servicenow.com/docs/access?context=take-actions-on-the-recommendations-for-similar-control-objectives&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The following enhancements have been introduced to the rationalization process of control objectives:

    -   Rationalization process is now automatically created when selecting the Rationalize button in the control objective page. 
    -   The recommendation workflow has been simplified into a two-step process: Step 1 identifies duplicates by accepting or dismissing recommendations; Step 2 finalizes by retaining one recommendation or creating a new common control objective.
    -   Approvals for the rationalization process are skipped for owners who are reviewers, and levels where all reviewers are owners are automatically approved. 
    -   Owners and approvers can add comments and justifications directly on recommendation cards and reply to existing comments. 
    -   The user interface has been updated with better navigation, quick summaries, visual improvements, and clear error messages.

-   **[Citation impact analysis and updates with Now Assist for IRM](https://www.servicenow.com/docs/access?context=control-objective-change-agent&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    When a citation’s description or supplemental guidance is updated, Now Assist identifies related control objectives that might be affected. It reviews these control objectives to determine whether the descriptions or guidance need changes and provides suggested updates. Users can review, provide feedback, and approve these updates directly in the Now Assist panel, ensuring that citation changes are reflected in associated control objectives.


-   **[Enhancements to control objectives and controls](https://www.servicenow.com/docs/access?context=co-overview-pc-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The following enhancements have been introduced to control objectives and controls:

    -   The Control objective requirements option provides a granular layer under a control objective. When each control objective has multiple statements, each statement becomes a control objective requirement.
    -   The Create control requirements option generates control requirements automatically for every control generated under an entity type.
    -   The Attestation at control requirement level enables attestation at a granular level for individual control requirements within a control.

-   **[Enhancements to policy exception and extension requests](https://www.servicenow.com/docs/access?context=review-policy-ext-and-extension-req-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The following enhancements have been introduced:

    -   For policy exception and extension requests, approvers can now view key details, such as justification, reason, and validity period, within a pop-up before approving or rejecting a policy exception or policy exception extension.
    -   For manual indicators, if the associated control is marked as exempt, no indicator task is generated.
    -   When a policy exception is in the Analyze state and the Awaiting Requested Information sub-state, the interface now includes a Send Information button that allows the requester to provide additional details or clarifications requested by the approver.
    -   Previously, an issue-based exception required a linked policy or control objective for additional approvals. Now, it requires any one of the following: a linked policy, control objective, or control. The control must be linked to the policy exception itself, not just to the issue.

-   **[GRC Approval Configurator](https://www.servicenow.com/docs/access?context=grc-approval-configurator-for-policy-extension-and-exception&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The GRC Approval Configurator can now be used to manage both policy exception and extension approvals. It allows verification, approval, and extension rules to be defined based on state, sub-state, and other filter conditions, with support for multiple user groups and multi-level approvals. This enhancement provides greater flexibility in assigning appropriate approvers at each level based on defined conditions, facilitating structured and collaborative reviews. For extension approvals, users can now configure multiple approvers, overcoming the previous limitation of a single default approver \(Compliance Manager\).


-   **[Common Control Objective Creation](https://www.servicenow.com/docs/access?context=take-actions-on-the-recommendations-for-similar-control-objectives&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Use Generative AI to merge similar control objectives into a single, consolidated common control objective. The system automatically populates the name, description, and guidance fields from the accepted duplicates, eliminating the need to manually select a primary control objective.


-   **[Entity based record access rules to secure new records](https://www.servicenow.com/docs/access?context=c_GRCControls&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    When entity based record access rules are enabled on the Entity Based Access Configuration Properties page, any newly created controls, control attestations, indicators, and indicator tasks associated with a configured entity will automatically inherit the entity-based access \(EBA\) value from that entity. Previously, users had to run bulk access updates to apply EBA restrictions whenever new objects were created.

    Additionally, when a standard control is converted to a common control, the **Entity based access restriction** option is inactive by default. Users can manually enable the EBA option for common controls directly from the Access Settings section in the Details tab of the respective control.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


-   **[Improved widget presentation and page layouts](https://www.servicenow.com/docs/access?context=compliance-manager-compliance-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    As part of the Coral theme enhancements, rounded card containers with drop shadows have been introduced for widgets across Compliance pages, and the gray background has been removed from the Compliance home page to simplify the interface.


-   **[Tasks panel in Compliance Home page](https://www.servicenow.com/docs/access?context=compliance-manager-compliance-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The Tasks section has been removed from the Compliance Workspace to improve page performance.


## Changed in this release

-   **[Improvements to the rationalization process of control objectives](https://www.servicenow.com/docs/access?context=take-actions-on-the-recommendations-for-similar-control-objectives&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Several enhancements have been made to the rationalization process:

    -   Redesigned the rationalization UI with a reordered layout and highlighted primary actions.
    -   Validations added for deactivated and deleted control objectives. Introduced the “Restart Analyze” option to support reevaluation of recommendations.
    -   Introduced support for Azure OpenAI, Amazon Bedrock, and Google Gemini for recommendations of control objectives.
    -   Updated the Consolidate state UI to show the recommendation panel with retained and accepted control objectives and their associated items.

## Activation information

Install Policy and Compliance Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Browser requirements

Policy and Compliance Management supports the latest public release and the two preceding versions of the following web browsers:

-   Google Chrome
-   Firefox and Firefox Extended Support Release \(ESR\)
-   Microsoft Edge Chromium
-   Safari 12.0 and later versions

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

