---
title: smart-assessment-designer release notes
description: Version history for the ServiceNow smart-assessment-designer application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-grc-sn-smart-assessment-designer.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance version history release notes, ServiceNow Store version history release notes]
---

# smart-assessment-designer release notes

Version history for the ServiceNow® smart-assessment-designer application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 23.0.5 - September 2026 \(Zurich, Australia\)**
    -   NEW:
        -   Question Bank:
            -   Build a centralized library of reusable questions with full lifecycle management. Questions move seamlessly through Draft → Ready to Publish → Published → Retired states, enabling version control and compliance tracking across all assessment templates.
        -   Independent Question Copies
            -   Published questions remain isolated when added to templates. Edit a question in your template without affecting the original, and vice versa—full customization freedom with zero cross-contamination.
    -   CHANGED:
        -   Unsaved Changes Across Tabs
            -   Your work is preserved instantly. Draft changes now persist across all workspace tabs—General, Questions, Automations, and Scoring. A visual dirty-state indicator on the workspace selector shows pending changes at a glance, so you never lose progress.
-   **Version 22.3.1 - June 2026 \(Australia\)**
    -   New:
        -   Template Versioning Support — Users can create new versions of assessment templates without affecting existing assessments or processes. All existing templates are automatically assigned version 1 during the upgrade. Trigger flow/API is backward compatible with previous template reference records. We retire the already published templates upon publishing the new templates. Template version number follows an incremental approach. Only one template can be in published state and only one template can be in draft state
        -   A couple of important field changes at the section, question, and response option changes will determine whether the change is structural or not. Structural change will delink the question from the previous version.
        -   Important consideration: Assessment targets, Purpose and Template name can't be changed from the second version
        -   Delete functionality: Introduced a Delete functionality if the template is in draft state
    -   Changed:
        -   Version indicator: Landing page only shows the latest template, and users can navigate to previous versions using the version indicator after opening the template designer page
        -   Version details in the Details tab form
        -   Fixes for Security defects and UX issues
        -   Localization changes
-   **Version 22.0.1 - March 2026 \(Yokohama, Zurich, Australia\)**

    New: Quick Edit allows template managers to make controlled updates to published templates, including inline changes to titles, descriptions, and reader roles.

-   **Version 21.0.3 - July 2025 \(Yokohama, Zurich\)**
    -   New:
        -   Added support for score normalization at question, section, subsection, and assessment levels using configurable strategies and input parameters.
        -   Added support for QR/barcode-type questions in assessments.
        -   "Template category" field on assessment template is now labeled as "Purpose".
-   **Version 20.1.1 - May 2025 \(Yokohama, Zurich\)**
    -   New: Template managers can now add descriptive images to questions in smart assessment templates, providing assessors with informative visuals for better guidance.
    -   Changed:The Automation tab is now hidden while the template copy is in progress in the Assessment Template Builder.
    -   Fixed:
        -   Resolved accessibility issues to improve user experience and compliance.
        -   Fixed minor localization issues.
-   **Version 20.0.2 - January 2025 \(Yokohama, Zurich\)**
    -   New:
        -   Search for text within assessment sections, subsections, or questions, enabling you to locate specific information or keywords. This feature enhances navigation and enables you to find relevant content without manually scrolling through the entire assessment.
        -   Create a copy of an existing smart assessment template, including all questions, sections, and existing configurations. This feature enables you to duplicate a fully configured assessment, so you don't need to recreate the content. You can then customize the copied template to fit new requirements or scenarios.
    -   Changed:
        -   The "Field to display in dropdown selection" for the selected table in reference-type questions now defaults to the display field defined in the table's sys\_dictionary.
        -   For choice-type questions, automatically added choices now use a placeholder "Choice" instead of pre-filled labels.
        -   In the Question tab of an assessment template, you can now add questions and subsections without having to click on a specific section each time. Additionally, sections are added at a more intuitive location rather than always being appended as the last section.
-   **Version 19.1.4 - November 2024 \(Yokohama\)**

    By using the ServiceNow Smart Assessment Designer application, you can easily create assessment templates and add instructions, questions, and reference information to an assessment template.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

