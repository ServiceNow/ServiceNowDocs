---
title: Proactive Prompts release notes
description: Version history for the Proactive Prompts application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hr-proactive-prompts.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - HR Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Proactive Prompts release notes

Version history for the Proactive Prompts application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.5.1 - June 2026**

    Fixed: Addressed security problems.

-   **Version 3.5.0 - March 2026**
    -   Changed: Enhanced prompt data review by the Manager.
    -   Fixed: Minor Defect fixes.
-   **Version 3.4.0 - December 2025**

    Fixed minor bugs.

-   **Version 3.3.4 - August 2025**
    -   Problem: Accessibility \(A11y\) issues were identified in the Proactive Prompt section for creating and updating growth plan prompts, affecting usability on the Career Hub page.
        -   New: Introduced accessibility improvements to the prompt UI for better screen reader and keyboard navigation support.
        -   Changed: Updated the markup and ARIA attributes in the prompt widgets to align with accessibility standards.
        -   Fixed: Resolved A11y errors that previously caused incorrect behavior when navigating the prompt section.
        -   Removed: Eliminated non-compliant HTML elements that interfered with assistive technologies.
    -   Problem: An RCA privilege issue was found in the Review Developing Skills widget, where the RCA status was incorrectly marked as Requested, causing test failures across multiple flows.
        -   New: Added the missing RCA entry to the inclusion list for the PromptUtils script include.
        -   Changed: Adjusted RCA privilege evaluation logic to correctly reflect the intended access level.
        -   Fixed: Corrected the RCA status to prevent test failures in skills review and enrollment flows.
        -   Removed: Removed the incorrect RCA privilege mapping that led to the misclassification.
    -   Problem: Tooltips were incorrectly displayed across the entire prompt container and modal, rather than only on the intended text elements.
        -   New: Introduced scoped tooltip behavior to limit hover effects to specific text elements.
        -   Changed: Modified the HTML structure and title attributes to prevent unintended tooltip propagation.
        -   Fixed: Resolved the issue where tooltips appeared across the entire container and modal overlays.
        -   Removed: Removed global title attributes from container elements that caused excessive tooltip display.
    -   Problem: Prompt notifications generated without actions in Now Assist for VA were missing the expected 'Dismiss' option due to lack of LLM-based action support.
        -   New: Introduced support for LLM-based 'Dismiss' actions in prompt notifications with no predefined actions.
        -   Changed: Updated the prompt generation logic to include both 'Mark as done' and 'Dismiss' actions when applicable.
        -   Fixed: Resolved the issue where notifications only displayed a single action, improving user interaction consistency.
        -   Removed: Removed the limitation that excluded LLM-based dismiss actions from prompts lacking explicit actions.
    -   Problem: The signal name was not appearing in the action modal for various prompt actions \(e.g., chat, email, meeting\), leading to confusion for end users.
        -   New: Added dynamic rendering of signal names in action modals across all supported prompt actions.
        -   Changed: Modified the modal template to include signal metadata for better context.
        -   Fixed: Corrected the UI behavior to ensure signal names are consistently displayed during user interactions.
        -   Removed: Removed the placeholder-only modal structure that previously omitted signal identifiers.
    -   Problem: The signal\_config\_field\_messages.jsdbx file was not cache-busted, leading to outdated content being served on UI pages.
        -   New: Appended glide.builddate to all relevant .jsdbx file references to enable cache busting.
        -   Changed: Updated UI scripts and client scripts to dynamically load the latest version of the configuration file.
        -   Fixed: Ensured that users always receive the most current configuration data by preventing stale caching.
        -   Removed: Removed static references to the .jsdbx file that bypassed cache validation.
    -   Problem: The Suggestions for you and your team widget in Manager Hub did not match the Coral theme styling, creating visual inconsistencies.
        -   New: Applied $brand-primary-opacity as the background color to align with Coral theme specifications.
        -   Changed: Updated the widget's CSS to reflect the correct theme variable for background styling.
        -   Fixed: Corrected theming discrepancies to ensure visual consistency with the Coral design system.
        -   Removed: Removed the previous hardcoded background color that conflicted with Coral theme guidelines.
    -   Problem: The background color for a section in Manager Hub did not comply with Coral theme standards, using an outdated color code.
        -   New: Introduced the correct Coral theme color \#E5F2F6 for the affected UI section.
        -   Changed: Replaced the previous color code \#BDDEE740 with the updated Coral-compliant value.
        -   Fixed: Resolved visual inconsistencies by aligning the UI with the approved Coral theme palette.
        -   Removed: Removed the deprecated color styling that was inconsistent with the latest design specifications.
-   **Version 3.3.2 - November 2024**
    -   Security fixes
    -   User prompt preferences at the delivery channel level
-   **Version 3.2.3 - August 2024**

    New: Added compatibility for mapping LLM-based actions/topics for Proactive Prompts.

-   **Version 3.1.0 - May 2024**
    -   New:
        -   Admin configuration to generate Prompts for a single user synchronously.
        -   Ability to generate day-wise Prompts \(insights for all upcoming days in the week\) in the calendar view for the workplace users.
-   **Version 3.0.0 - August 2023**
    -   New:
        -   Employees/Managers can opt-out or opt-in of receiving the prompts.;
        -   Support for additional out-of-the-box prompt content.
        -   Configuration to add a custom header on the prompt to indicate the type of prompt.
    -   Changed: Improved user experience by including links in the View details to the items/tasks/records based on the URL configured in the Script data source.
-   **Version 2.0.0 - May 2023**

    New:

    -   Proactive Prompts Dashboard - To understand Prompts usage analytics.
    -   Subflow data source type - Introduced a new data source type to support no code options in the decision framework.
    -   Expiring old Prompts before the next schedule generates new prompts.
    -   Support for Learning and Skills use cases as out-of-the-box content.
-   **Version 1.0.1 - February 2023**
    -   Proactive Prompts enables contextual and proactive engagement for managers and employees by bringing actionable insights as prompts into their flow of work.
    -   Following are a few key benefits of Proactive Prompts:
        -   Drive engagement
        -   Boost productivity
        -   Accessibility
    -   With Proactive Prompts along with ManagerHub, you can Proactively send Managers 'micro insights' based on current situations with the team in the 'Flow of work'.
    -   Includes OOB suggestions for Manager Hub portal with data driven triggers.

