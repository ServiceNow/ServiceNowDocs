---
title: AI Search for Next Experience release notes
description: Version history for the AI Search for Next Experience on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-ai-search-nextexperience.html
release: store
topic_type: reference
last_updated: "2026-02-05"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Other ServiceNow AI Platform Capabilities applications, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# AI Search for Next Experience release notes

Version history for the AI Search for Next Experience on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 5.0.2 - February 2026**
    -   Fixed:
        -   Read-only field remediation
        -   Improper logging when Zing to AIS migration fails to migrate search source with an invalid condition
-   **Version 5.0.0 - December 2025**
    -   Changed: Removed Search UX components to alternatively load them via a newly-created monorepo.
    -   Fixed:
        -   In Zing to AI Search migration, adding a search source creates a double entry for records that need to be migrated.
        -   Numerous translation issues.
-   **Version 4.1.1 - September 2025**
    -   Fixed:
        -   Zing Migration Tool does not let users select unused Search Application Configurations from OOTB migration records \(PRB1917747\)
        -   Improper use of current.update in Business Rule \(PRB1859890\)
        -   Regular catalog item results should use pencil icon for consistency \(PRB1857879\)
        -   Added configuration needed to control the "Hide filters" button visibility on sn-search-facet component \(PRB1920468\)
        -   Documents are opened in new browser tab instead of built-in NOW tab from search result if HTTP is in the search query \(PRB1910191\)
-   **Version 4.0.6 - March 2025**
    -   Fixed:
        -   Security bug for ACL bypass
        -   Enable/disable AI Search for Next Experience button correctly
-   **Version 4.0.4 - November 2024**
    -   Changed:
        -   Fixed Sandbox Access security issue
        -   Show Catalog Items in Recently Clicked Suggestions in Global Search
        -   Open par results by clicking on them from global search
-   **Version 4.0.0 - May 2024**

    New: Add three Platform Analytics tables \(Dashboards, Data Visualizations, and KPIs\) to global search results page.

-   **Version 3.0.7 - February 2024**
    -   Fixed:
        -   Unable to see facet filter even though configuration is correct
        -   Search application not available to migrate if searchEnabled property value has additional spaces
        -   Zing to AIS migration failing when there are invalid search sources
        -   I18n issue: Zing to AI search contains hardcoded string
-   **Version 3.0.5 - September 2023**
    -   Fixed:
        -   sys\_ux\_section file removed from the AI Search for Next Experience app
        -   Migration tool now considers child tables during migration
-   **Version 3.0.1 - May 2023**
    -   New in v3.0:
        -   Support Genius Results in AI Search for Next Experience. To learn about Genius Results and the existing Genius Result configurations that AI Search supports, please visit https://docs.servicenow.com/en-US/bundle/utah-platform-administration/page/administer/ai-search/concept/genius-results-ais.html.
        -   Support cross-table facets in AI Search for Next Experience to allow faceting search results on cross-table fields such as tags. To learn about how to configure cross-table facets, please visit https://docs.servicenow.com/bundle/utah-platform-administration/page/administer/ai-search/task/create-facet-ais.html.
        -   Support search-based auto-complete suggestions in AI Search for Next Experience to get instant results matches based on title. To learn more about search-based auto-complete suggestions, please visit https://docs.servicenow.com/bundle/utah-platform-administration/page/administer/ai-search/concept/auto-complete-ais.html
-   **Version 2.1.0 - March 2023**
    -   New:
        -   Test
        -   Added Guided Setup module to walk customers through enablement.
            -   Verify that the instance satisfies all AI Search for Next Experience.
            -   Reduce time-to-value for customers who upgrade from Zing by providing guided and automated migration tools to convert Zing configuration to AI Search configuration.
            -   Allow one-click to turn on AI Search for Next Experience for global search and configurable workspaces.
        -   Added the Direct to List View to pass search query from search to the List View when viewing search results for one table.
-   **Version 2.0.2 - November 2022**
    -   New:
        -   Added Guided Setup module to walk customers through enablement:
            -   Verify that instance satisfies all AI Search for Next Experience prerequisites.
            -   Reduce time-to-value for customers who upgrade from Zing by providing guided and automated migration tools to convert Zing configuration to AI Search configuration.
            -   Allow one click to turn on AI Search for Next Experience for global search and configurable workspaces.
        -   Added Direct to List View to pass search query from search to the List View when viewing search results for one tabletest.
-   **Version 2.0.1 - November 2022**
    -   New:
        -   Added Guided Setup module to walk customers through enablement:
            -   Verify that instance satisfies all AI Search for Next Experience prerequisites.
            -   Reduce time-to-value for customers who upgrade from Zing by providing guided and automated migration tools to convert Zing configuration to AI Search configuration.
            -   Allow one click to turn on AI Search for Next Experience for global search and configurable workspaces.
        -   Added Direct to List View to pass search query from search to the List View when viewing search results for one tabletest.

**Parent Topic:**[ServiceNow Store - Other ServiceNow AI Platform Capabilities applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-platcap-rn-other-landing.md)

