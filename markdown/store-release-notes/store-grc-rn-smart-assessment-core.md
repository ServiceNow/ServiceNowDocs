---
title: Smart Assessment Core release notes
description: Version history for the Smart Assessment Core application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-smart-assessment-core.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# Smart Assessment Core release notes

Version history for the Smart Assessment Core application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.2 - June 2026 \(Australia\)**
    -   New:
        -   Template Versioning Support — Users can create new versions of assessment templates without affecting existing assessments or processes. All existing templates are automatically assigned version 1 during the upgrade. Trigger flow/API is backward compatible with previous template reference records. We retire the already published templates upon publishing the new templates. Template version number follows an incremental approach
        -   Embedded Assessments — We support the embedding of assessments in the business workflow for certain use cases. We can enable embedded assessments at the template category level and control access using upstream application records. For example, if you embed control attestation in the control record.
        -   Support for Work Notes &amp; Comments, Flagging for assessments—
            -   A user who can read the assessment can also comment at the question level.
            -   Work notes are enabled at the question level and assessment level. Smart assessment can control visibility of this feature via Access settings in the Template category -&gt; General settings section
            -   Question level flag: to track questions which needs user attention. This feature is enabled by default for all users who can read the assessment, but it can be controlled in the same way.
        -   Public API's for Add/Remove Collaborators, Creating a template version
    -   Changed:
        -   Combined assessment via API: Customer-facing API for external scripts and integrations to create combined assessments via API. No admin action required, and it won't break existing implementations.
        -   Versioning in responder: Support for copy and combined assessments across different versions
        -   Support for Translations when copying the template, versioning a template
        -   Localization Updates
    -   Fixed:
        -   Critical security defects
        -   Ability to modify response automation for number type
        -   Combined assessment support only for the same primary owner
-   **Version 22.0.4 - March 2026**

    Changed: Improve access control by allowing template categories to support multiple roles instead of a single role. The single-select field Category Role is now replaced with multi-select field Category Roles.

-   **Version 21.1.1 - December 2025 \(Zurich\)**
    -   New: Combine assessments from different templates into a single, streamlined view. Eliminating the need to open each assessment separately, preserving context, and improving efficiency.
    -   Fixed: Security enhancement for read-only fields.
-   **Version 21.0.1 - August 2025**
    -   New:
        -   Added support for answering QR/barcode-type questions in assessments.
        -   Added support for score normalization at question, section, subsection, and assessment levels using configurable strategies and input parameters.
        -   Assessment owners can now add multiple contributors to collaborate on the same assessment.
    -   Fixed: Fixed incorrect 'Completed \(error skipped\)' status for the 'Trigger Smart Assessment' flow action by correcting error evaluation logic and action status codes.
-   **Version 20.2.2 - June 2025**

    New: Shipped query range ACLs for improved data security on key Smart Assessment tables:sn\_smart\_asmt\_instance, sn\_smart\_asmt\_combined\_assessment, sn\_smart\_asmt\_template, sn\_smart\_asmt\_m2m\_instance\_persona, and sn\_smart\_asmt\_template\_category.

-   **Version 20.1.1 - May 2025**
    -   New: Added support for descriptive images in assessment questions, enabling template managers to include instructional visuals to guide assessment respondents.
    -   Fixed:
    -   -   Fixed an issue where an error was incorrectly thrown when calling the "Trigger Smart Assessment" flow action via script without due date or duration parameters.
-   Fixed issue with displaying localized values for reference card description, and section name and description in assessment template.
-   Fixed issue where question labels were replaced with the localized equivalent of 'Untitled' in non-English languages during template copy.
-   **Version 20.0.2 - February 2025**
    -   New:
        -   Set up automatic responses for questions to enable assessors to complete assessments efficiently. You can either create default responses for all question types or define a script to fetch and map the values or data to responses.
        -   Introduced a new role, "sn\_smart\_asmt.reassign" for reassignment of assessments.
    -   Fixed:
    -   -   Validation logic for reference-type questions now applies the question configuration's filter condition in a case-insensitive manner.
-   The "Last Responded By" field now updates correctly for questions of type "Attachment."
-   **Version 19.1.0 - November 2024**
    -   Evaluate Sandbox Access for Client-Callable Script
    -   Radio \(Question Type\): The selected response option \(Choice\) is deselected when the user navigates to another question or moves away before the autosave process completes.
-   **Version 19.0.4 - August 2024**
    -   The ServiceNow Smart Assessment Engine \(SAE\) application streamlines the organization's assessment procedures through automation, reducing manual effort and increasing workforce efficiency. Using SAE, the Assessment Admins can create, view, and update assessments. Assessments Admins can then assign the assessments to gather essential information from diverse stakeholders and evaluate various workflow aspects. The assessments can apply to any context and are enabled for key Integrated Risk Management \(IRM\) workflows, including control attestation and risk identification. The SAE application provides an intuitive and user-friendly user interface, structured process for managing assessment templates, soliciting responses, and automating the entire workflow.
    -   Benefits:
        -   Efficiency: SAE automates repetitive and time-consuming assessment tasks, significantly reducing the time and effort needed for evaluations.
        -   Flexibility: SAE's high flexibility allows it to be tailored to specific use cases, making it adaptable for a wide range of organizational needs like Control Attestation and Risk Identification.
        -   Scalability: SAE handles assessments of varying scales, from small departmental evaluations to large enterprise-wide assessments, adapting to different organizational needs.
        -   Configurability: Extensive control over assessment parameters includes configuring question types, justification prompts, and conditional visibility based on previous responses. This enables creating more meaningful and contextually appropriate evaluations.
        -   Cost-effectiveness: By serving multiple assessment needs with one software solution, organizations can reduce costs associated with purchasing and maintaining multiple specialized tools.
        -   User Experience: SAE focuses on providing a user-friendly interface for both administrators and business users. Features like progress indicators, automatic saving, and clear navigation lead to higher engagement and more effective assessments.

