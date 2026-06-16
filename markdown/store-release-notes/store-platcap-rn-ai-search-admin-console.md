---
title: AI Search Admin Console release notes
description: Version history for the AI Search Admin Console application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-ai-search-admin-console.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Other ServiceNow AI Platform Capabilities applications, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# AI Search Admin Console release notes

Version history for the AI Search Admin Console application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 9.0.5 - June 2026**
    -   New:
        -   Added support for auto-enabling hybrid search using the hybrid search attribute, with status visibility surfaced on the AI Search Admin Console home page.
        -   Added buttons and links to open the Now Assist Panel \(NAP\) for agentic search configuration directly from the Admin Console.
        -   Integrated the Search Status Page into the AI Search Admin Console for centralized visibility into search health.
        -   Embedded Clear Indexing Status functionality within the Admin Console.
        -   Added support for multi-modal captioning per indexed source, configurable through the Knowledge table advanced configuration settings.
        -   Added the ability to enable or disable multi-modal search \(MMS\) via search properties.
        -   Updated AI skills to use the latest available models.
        -   Migrated AI skills from GAIC to Mosaic, including an impact study for out-of-the-box skill migration.
    -   Fixed:
        -   Fixed a permissions error \("You do not have permissions to edit assistants in this domain."\) that appeared when creating assistants from the AI Search Admin Console.
        -   Security fixes.
        -   Resolved multiple hard-coded strings as part of an internationalization review to improve localization support.
        -   Fixed an issue where table retry was unavailable due to Virtual Agent topics not being published.
        -   Fixed an issue where AI Search Internal Agent observations were not being correctly handled for the Now LLM Model integration.
        -   Fixed an issue preventing child tables in non-global scope from being added to an indexed source.
        -   Fixed accessibility issues on the AI Search Admin Console App Configuration main page.
        -   Fixed an issue where the AI Search Adoption Blueprints page was inaccessible to admin users in maint-only mode.
-   **Version 8.0.4 - May 2026 \(Zurich, Australia\)**
    -   Fixed:
        -   Fixed an ASCII \\n character in the script editor that was triggering false positive internationalization \(i18n\) warnings.
        -   Fixed an issue where AI Search Internal Agent observations were not being correctly handled for Claude and Gemini integrations.
        -   Fixed incorrect documentation links from the production environment that were pointing to pre-release content with inaccurate information.
        -   Fixed a keyboard navigation issue on the AI Search Admin Console home page where right/left arrow keys could only advance one tab at a time before focus shifted to the top of the page.
        -   Fixed an issue where semantic index entries in search sources with hybrid search enabled did not navigate to the correct table.
        -   Fixed missing semantic ingestion embedding stats on the AI Search Admin Console.
        -   Security fixes.
-   **Version 8.0.3 - April 2026**
    -   New: AI Agent: AI Search Internal Sources – Implementation and Configuration Agent
    -   Fixed:
        -   Filters on the Applications tab of the Admin Console that returned blank lists in error.
        -   Page title on the Application tab of the AI Search Admin Console that did not include the name of the application being configured.
        -   Unidentified main page headings in the AI Search Admin application configuration page.
        -   Incorrect focus order for the Configure application button relative to application information on the Applications page.
        -   Hybrid search toggle appearing even when semantic search was not installed.
        -   Multiple issues with the AI Search Internal Agent when using Azure OpenAI.
        -   Issues uncovered during end-to-end testing of the AI Search Agent.
        -   Frequent instance logouts when configuring AI Search for tables with child tables.
        -   GlideRecordSecure ACL security warning flagged in the release readiness report.
        -   Broken link to AI Search documentation from the Search Admin Console.
        -   Localization \(L10N\) warnings.
        -   AI Search certification failure caused by query generation tool files not scoped under the AIS assist conditional.
-   **Version 7.1.2 - March 2026**
    -   Fixed:
        -   An issue where multiple H1 headings were present when configuring a new profile.
        -   An issue where a button was announced as unavailable to screen readers when adding search sources.
        -   An issue where the Advanced Configuration element had an incorrect button role.
        -   An issue where multiple elements on the Admin page were truncated when text was resized.
        -   An issue where Index Sources, Configuration, and Semantic Index terms were not translated correctly.
        -   An issue where some ingestion statistics were missing for semantic indexing.
        -   Unlabeled buttons used for configuring search.
        -   Missing heading labels on the Search Profile page.
        -   A broken link to “Turn off AI Search” on the Now Assist for Playbook Recommendations panel.
        -   Application navigation that did not reflect re‑mappings introduced when Now Assist was enabled for a portal.
        -   An issue where a semantic fields warning message briefly appeared when hybrid search was enabled.
        -   An issue where the "Hybrid search" toggle was only available for portals instead of all search applications on the Application Configuration page.
        -   An incorrect success message shown when Result Improvement Rules were disabled.
        -   An incorrect translation for the "ais\_retention\_policy label" field.
        -   Missing descriptive labels for the “Create New” and “Select Existing” buttons on the App Configuration page.
        -   An issue where the “Indexed documents by month” widget did not display data on the AI Search Admin Home page.
        -   An issue where selected tabs were not announced as selected for the Home, Applications, and Shared Configurations tabs.
-   **Version 7.1.1 - February 2026**
    -   Fixed:
        -   Hybrid search toggle should be available for all search applications for Now Assist customers
        -   Corrected incorrect trigger condition for Search Personalization
        -   Automatically link newly created Search Sources
        -   After Hybrid Search is toggled in an application - an error message is displayed stating the source lacks semantic fields \(when the semantic fields are actually present\)
-   **Version 7.0.6 - December 2025**
    -   New:
        -   Support for enabling Now Assist Multi-Content Response genius results for global search and workspaces
        -   Support for enabling hybrid search for service portals
        -   Support for enabling search personalization in a single click
    -   Fixed:
        -   Applications - Genius Results Configuration: Now Assist multi-content Q&amp;A \(Recommended\) section loads after the rest of the page
        -   Display status as "Re-index is needed for configuration change to take effect" when new semantic configs are added to an index source
        -   The application tab has several elements that are truncated for reflow users
        -   Change Result Card modal lacks heading
        -   Continue Button functionality is not working
        -   Coral Theme refresh button misaligned
        -   Delete button is getting enabled while selecting and un-selecting all records in section
        -   Null value briefly appears while records are loading into some pages
        -   Suppress indexing required messages for external connectors
        -   Multiple translation issues
-   **Version 6.1.3 - September 2025**
    -   Fixed a number of bugs:
        -   GR created through admin console doesn't have order in the list form
        -   Numerous translations
        -   Search Application Configuration - Create new button position is not aligned correctly
        -   Remove indexing option for external indexed sources in admin console
        -   App not found/Link to Null error
        -   Migrate admin acls to a more granular role for ai-search-admin
-   **Version 6.0.4 - August 2025**
    -   AIS Admin can configure facets to be sorted by count or name \(alphabetically\)
    -   AIS Admin can configure the number of collapsible attachments per search result
    -   AI Search Admin landing page shows 4 search applications instead of 3
    -   Adjust AIS Admin Console to reflect the removal of tabs from search applications
    -   "Manage your search data" alert on AI Search Admin landing page
-   **Version 5.0.10 - May 2025**
    -   Configure synthesized Genius Results in portals
    -   Support test indexing for indexed source
    -   Improve UX for indexed source status overview
-   **Version 4.1.12 - February 2025**
    -   New:
        -   Create and manage indexed source from "shared configuration"
        -   Support custom semantic index creation for RAG developers in Now Assist
-   **Version 3.1.4 - November 2024**
    -   New:
        -   Configure result card interface from AI Search admin console: new UX to create and manage EVAM configurations
        -   Update Default Columns in Search Source: Allow excluding search sources from standard search or Genius Results

**Parent Topic:**[ServiceNow Store - Other ServiceNow AI Platform Capabilities applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-platcap-rn-other-landing.md)

