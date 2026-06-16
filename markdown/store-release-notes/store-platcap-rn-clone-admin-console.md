---
title: Clone Admin Console release notes
description: Version history for the Clone Admin Console application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-clone-admin-console.html
release: store
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Other ServiceNow AI Platform Capabilities applications, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Clone Admin Console release notes

Version history for the Clone Admin Console application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.2.0 - May 2026**
    -   New:
        -   Instance Overview Page: The Instance Overview page now displays last-cloned timestamps for each instance, enabling you to quickly identify stale environments and prioritize update activities.
        -   Multi-Instance View: View clone activity across connected instances from a single console. Opt in from Configuration &gt; Multi-Instance View to begin monitoring multiple instances simultaneously.
        -   Clone FAQ Agent \(via Now Assist\): Get answers to clone questions directly in the console, powered by curated ServiceNow clone documentation. This AI-assisted capability streamlines the learning experience for new users.
        -   Requirement: Requires a Now Assist license. If Now Assist is installed after the Clone Admin Console, reinstall the console from the Store to enable the skill.
        -   Help Page: The static FAQ section on the Homepage has been replaced with a dedicated Help page. Links to curated clone help articles are now consolidated in a single location, alongside version information and details about the Now Assist AI skill.
        -   Clone Request Estimated Completion: The Clone Request page now displays an estimated completion time beneath the selected Date/Time. A relative time indicator \(for example, "in 2 hours" or "in 2 weeks"\) helps you plan activities accordingly.
    -   Changed:
        -   Configuration Menu: All clone-related settings are now grouped under a single Configuration menu item for improved organization and discoverability.
        -   Clone Home Renamed to Clone Activity: The Clone Home menu item has been renamed to Clone Activity to be more descriptive of the page's purpose and improve navigation clarity.
    -   Fixed:
        -   Clone Profile Script Updates: Fixed an issue where setting a script in the clone\_cleanup\_script table to active=false or active=true did not apply consistently across all clone profiles the script was listed on. Changes now propagate correctly.
        -   Clone Profile Duplication: Fixed an issue where duplicating a clone profile pulled in all existing scripts, preservers, and exclusions from the original profile. Duplicating a profile now correctly creates a new profile containing only the intended scripts, preservers, and exclusions from the source.
    -   Removed:
        -   Static FAQ Content: Static FAQ content has been removed from the landing page and consolidated into the new dedicated Help page for a streamlined user experience.
-   **Version 2.1.7 - March 2026**
    -   Fixed:
        -   Instance Registration: Resolved an issue where adding a new instance \(Configurations &gt; Instances &gt; Add New\) would fail if the instance name contained trailing spaces or a forward slash. Both characters are now handled correctly.
        -   Accessibility: Resolved several accessibility issues to improve compliance and usability.
        -   Localization: Resolved several localization issues to ensure accurate translations and regional formatting.
    -   Enhancements:
        -   Clone Request Form: Added a hyperlink to the selected profile field, allowing users to navigate directly to the profile from the clone request form.
        -   Security enhancements.
-   **Version 2.1.6 - January 2026**
    -   Users can now submit clone requests to a target instance that has another scheduled clone, provided the requests are more than 7 days apart
    -   Left nav menu consolidation
    -   Usability, security fixes
    -   Resolved an issue where the Cancel button on the calendar time slot selection did not close the modal.
-   **Version 2.1.2 - December 2025**
    -   Accessibility fixes
    -   Usability enhancements
    -   Menu item consolidation
    -   Security enhancements
    -   Admin experience theme updates
-   **Version 2.0.1 - August 2025**
    -   Performance improvement on the clone request page
    -   Dark theme support
    -   Internationalization and localization fixes
    -   Home page UI improvements and fixes
    -   External email support fix
    -   Bug fixes and other improvements
-   **Version 1.0.18 - May 2025**
    -   Ability to add external email addresses to receive clone notifications
    -   Performance improvements
    -   Clones are sorted by recency on the homepage
    -   A new target instance can be registered from the clone request page
    -   UI and usability improvements
-   **Version 1.0.17 - February 2025**
    -   Preserve Theme support for Next Experience themes
    -   Improvements to cross-scope scope warnings
    -   Improvements to refresh intervals and clone progress reporting
    -   Default clone profile pre-populated onto the clone request page
    -   Performance and usability improvements
-   **Version 1.0.16 - November 2024**
    -   New: Ability to view granular restore progress
    -   Fixed: UI Improvements; Internationalization
-   **Version 1.0.15 - August 2024**
    -   Fixed:
        -   Clone Duration Display Fixes
        -   Date/Time Format Fix
        -   UI Improvements
-   **Version 1.0.12 - May 2024**
    -   New:
        -   Ability to duplicate clone profile
        -   Ability to add a target instance on the clone request form
        -   Column picker for definitions
    -   Fixed: Clone progress bar improvements on the clone status page
-   **Version 1.0.11 - February 2024**
    -   New: Localization support for multiple languages; UI improvements on Clone Home, incl. column picker for List View; UI improvements on Clone Request Page; Clone Logs on Clone Status page; Clone pre-submission warning to save unpublished development work; Added a preview within the recurring clones feature.
    -   Changed: Simplified the recurring clone feature; Backup selection can now be made via a dropdown.
    -   Fixed: List view on Clone Home now remembers user preferences for selected columns and the preferred column order; Clone can be successfully placed with a custom clone profile that has just OOB definitions \(preservers, exclusions, and scripts\).
-   **Version 1.0.9 - November 2023**

    The Clone Admin Console provides a streamlined user experience for cloning data between instances, one of ServiceNow's most-used automations. It features a unified cloning experience, updated visibility, and several key features informed by customer needs.


