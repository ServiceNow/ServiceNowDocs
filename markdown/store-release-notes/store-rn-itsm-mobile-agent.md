---
title: ITSM Mobile Agent release notes
description: Version history for the ITSM Mobile Agent on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-mobile-agent.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - IT Service Management release notes, ServiceNow Store release notes]
---

# ITSM Mobile Agent release notes

Version history for the ITSM Mobile Agent on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.2.1 - June 2026**

    Fixed: Major incident management notification redirect defect fix

-   **Version 10.2.0 - December 2025**
    -   Changed: Properties related to displaying number of events in Future &amp; past in shift calendar can now be updated by users having sn\_shift\_planning.admin role.
    -   Fixed:
        -   Close task and Snooze actions are now visible for incident communication task in the Major incident Management section.
        -   The start and end date time field is now visible to the user in dashboard when the user has a time format like: dd/MM/YYYY
        -   Users can view Gaps/Conflicts for On-Call Schedules Under My Team.
-   **Version 10.1.0 - August 2025**

    Fixed: On-call user information is properly displayed in agent app.

-   **Version 10.0.0 - February 2025**
    -   Starting this release, you can do the following:
        -   Summarize the incident record and activity information when adding work notes in an incident record or while reassigning an incident.
        -   Set different alert tones for incidents with different priority.
        -   Set the incident impact and urgency levels to automatically set the incident priority level.
        -   Seamlessly redirect from mobile web browser to the ITSM Mobile Agent app for opening and viewing different task records.
-   **Version 9.0.1 - November 2024**
    -   Changed:
        -   Starting in version 9.0, you can do the following:
            -   Experience the new data visualizations for the analytics on the My team and Major incidents applets.
            -   My team applet: View the Performance metrics, My team's weekly opened incidents, and My team dashboard.
            -   Major incidents applet: View the Major incident dashboard, and Major incidents opened graph.
            -   Enable dark theme or mode for active calls on the Collaborate section of the My work applet.
    -   These changes are available in the base system for both the new or upgrade customers. You can also view mobile analytics in Platform analytics workspace to configure or create new data visualization.
    -   For the upgrade customers who have already customized the analytics sections of the applets, the data visualizations changes are not available by default. You must enable the new analytics section records from the Mobile Agent section of the Mobile App Builder to view the visualized changes.
-   **Version 8.2.2 - August 2024**

    Receive critical alerts on Mobile with an alerting ringtone, even when the user has enabled DND. \(Requires to be configured and alerts send only post user permission\).

-   **Version 8.1.3 - May 2024**

    Changed: If an Agent's phone is in Do Not Disturb \(DND\) mode, critical alerts will now be able to override the DND setting. Support has been added for On-call notifications.

-   **Version 8.0.0 - February 2024**

    New: If an Agent's phone is in DND, critical alerts will now be able to override the DND setting. This feature will work once permission is granted by the end user.

-   **Version 7.0.0 - August 2023**
    -   New: Support for Dark Theme.
    -   Changed: Updated calendar component for performance improvement.
    -   Fixed: Some minor bugs.
-   **Version 6.0.0 - February 2023**
    -   New:
        -   Next Experience theme support and accessibility improvements for input form screen and icon section.
        -   AI search with intelligent query features to help agents quickly find the required answers.
-   **Version 5.0.2 - March 2022**
    -   Fixed:
        -   Fix is provided for an itil user not being able to initiate a conference call from ITSM Mobile Agent v5.0.1 and lower in the San Diego instance. For information about this fix, see [KB1005864](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1005864).
        -   Fix is provided for an issue in the Approval assigned to me flow for the sc\_req\_item table.
        -   Fix is provided for the time displayed in the shift swap request.
        -   Fix is provided for the count mismatch in the Breached Incidents report under the My teams applet launcher.
-   **Version 5.0.1 - March 2021**
    -   New \(these features are available with the Workforce Optimization for ITSM Enterprise License\):
        -   Managing schedules using the ITSM Mobile Agent application
        -   ITSM Mobile Agent notifications for Workforce Optimization for ITSM
        -   Properties to retrieve events in the ITSM Mobile Agent application
-   **Version 4.0.0 - January 2021**

    New: The new ITSM Mobile Agent app delivers mobile-first experiences for agents to triage and resolve incidents on the go.

-   **Version 3.0.1 - September 2020**
    -   New:
        -   Domain separation support on mobile: Your users can now have faster onboarding, meet compliance, and protect their data using domain separation. The mobile view includes the separated data you have setup on platform through logical grouping called domains. You control who sees and accesses what content.
        -   Actionable notifications: Include actions with your push notifications. Now, users can perform push notification actions without opening the app.
-   **Version 2.0.0 - April 2020**
    -   New:
        -   Twilio Support for conference calling
        -   Create Incidents
-   **Version 1.1.1 - January 2020**

    The new ITSM Mobile Agent app delivers out of the box mobile-first experiences designed for agents to triage, act on, and resolve incidents on the go. ITSM Mobile Agent improves productivity with an intuitive interface to manage all the work, view schedules, check who is on-call, respond to major incidents, and more.


**Parent Topic:**[ServiceNow Store - IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itsm.md)

