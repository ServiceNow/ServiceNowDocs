---
title: Service Operations Workspace Supervisor Dashboard release notes
description: Version history for the ServiceNow Service Operations Workspace Supervisor Dashboard application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-sow-supervisor-dashboard.html
release: store
topic_type: reference
last_updated: "2026-07-09"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Service Operations Workspace Supervisor Dashboard release notes

Version history for the ServiceNow® Service Operations Workspace Supervisor Dashboard application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.1.0 - July 2026**
    -   Changed:
        -   Express List accessibility improvements. The Express List is now fully accessible to users with low vision, expanding the user base and ensuring compliance with international accessibility standards and regulations.
        -   Consolidated ACLs for access control management. Access control lists have been consolidated to better follow security best practices, reducing risks and simplifying management.
        -   Link View topology visualization accessibility. Link View topology visualization now meets accessibility standards while maintaining usability and performance.
    -   Fixed:
        -   The Express List layout has been corrected to properly adapt for narrow viewports and no longer breaks at certain screen sizes.
        -   Unintended double scrollbars in accessibility reflow mode have been eliminated.
        -   The Express List columns now display correctly in Japanese and CJK languages, resolving translation and layout issues.
        -   The Express List live list functionality now properly triggers and updates in real time.
        -   The "update available" banner no longer appears incorrectly when resuming the live list.
        -   Saving an Alert Management Rule with "Create Incident Advanced" now works in all scenarios.
        -   Operators with more than five assignment groups can now see their created Enrich automations in the Enrich module.
        -   Alerts manually removed from a group are no longer automatically re-added.
        -   A broken documentation link in the alert automation configuration has been fixed.
        -   Dynatrace Monitor setup instructions in the Launchpad have been updated to match the current Dynatrace console.
        -   The "Tags" label in the Launchpad is now correctly translated across contexts.
        -   Concatenated strings causing grammatical issues in certain languages have been separated for correct localization.
        -   Launchpad forms now match the approved design at 400% zoom.
        -   Dotted connection lines in Link View now appear when connected CIs are returned from the backend.
        -   The Simulation UI now displays "This automation" or the saved automation name instead of "MIXED" or "CMDB" labels for Mixed or CMDB group types.
        -   The "All Time \(Last 180 days\)" option now shows as selected in the time range picker and is correctly translated.
        -   Service health percentages now display correctly in locales using a comma as the decimal separator.
        -   Ellipsis menu items in the Log Viewer now display in the user's language setting.
        -   Backspace behavior in Extended mode is now correct.
        -   The evt\_mgmt\_admin role now has write access to Express List properties.
-   **Version 1.0.11 - June 2026**
    -   The AIOps Supervisor Homepage is a role-tailored workspace designed for NOC supervisors and AIOps managers overseeing AI-driven IT operations. It provides a unified, real-time view of both active operational work and autonomous AI activity across the environment.
    -   A key metric on the page — Time Saved Using AI — gives supervisors a tangible signal of AIOps value, calculated from the volume of alerts resolved and analyzed autonomously versus what would have required manual effort.
    -   The homepage is available as part of the Service Operations Workspace and targets organizations running Event Management with Alert Automation and Autonomous Grouping enabled.

**Parent Topic:**[ServiceNow Store - IT Operations Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itom.md)

