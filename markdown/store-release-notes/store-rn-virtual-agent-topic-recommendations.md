---
title: Virtual Agent Topic Recommendations release notes
description: Version history for the Virtual Agent Topic Recommendations on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-virtual-agent-topic-recommendations.html
release: store
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Conversational Interfaces, ServiceNow Store release notes]
---

# Virtual Agent Topic Recommendations release notes

Version history for the Virtual Agent Topic Recommendations on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.5.5 - August 2024 \(Xanadu\)**

    Dependency update for security.

-   **Version 4.5.3 - November 2023**

    Fixes.

-   **Version 4.5.2 - August 2023 \(Vancouver\)**

    Fixed: Translation and internationalization issues.

-   **Version 4.4.2 - May 2023**
    -   Fixed:
        -   After selection of a topic to link screen reader is reading extra information ""0 results found.""
        -   Keyboard focus is getting lost after activating ""Last 90 days"" button and dialog is not accessible under ""Get Recommendations"" dialog.
        -   Keyboard focus is getting lost when user activate ""Remove this condition"" button in ""Get Recommendation"" dialog.
        -   Report Vidoe ACL warning updates.
-   **Version 4.3.0 - November 2022**
    -   Fixed: Accessibility-related issues.
    -   Removed: Removed "Recommendation Settings" from the Next Experience Unified Navigation All menu; Topic Recommendations Settings can now be accessed through Conversational Interfaces Settings.
-   **Version 4.2.0 - August 2022**
    -   New:
        -   Surface the most relevant recommendations with new filter options to display/hide previously added or ignored recommendations; when a user is reviewing the individual recommendation in the popover window, they can mark that recommendation to be selected or ignored.
        -   A new system property can be set to limit how many topic recommendations are displayed \(default 30\); where there are more,See more links display additional recommendations.
        -   Updated summary status box that provides confirmation of new topics or intents that were successfully added, along with links to customize the newly added topics/intents or to tune the NLU model\(s\). The Customize these topics link opens VA Designer with the category filter set to Recommended. The Tune NLU Model link opens NLU Workbench.
-   **Version 2.1.0 - September 2021**

    Fixed: Show error when NLU validation fails \(models must have at least 2 intents and 5 utterances each\).

-   **Version 2.0.0 - August 2021**
    -   New:
        -   NLU model grouping support
            -   Create new model group for a topic
            -   Map the topic to an existing model group
            -   Map the topic to a standalone model
        -   One-click NLU intent binding after training
        -   Link/unlink a recommendation to an existing topic
        -   Improved user interface
            -   Edit data filters for a report directly in Topic Recommendations
            -   Collating data by taxonomy
            -   Improved status indicators for topics: New, Added/Linked, Active/Inactive
            -   Topic completion chart for active topics
-   **Version 1.0.4 - April 2021**

    Fixed: Bug fixes and performance changes.

-   **Version 1.0.2 - February 2021**

    Fixed: Minor fixes.


**Parent Topic:**[ServiceNow Store - Conversational Interfaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-conversational-interfaces-landing.md)

