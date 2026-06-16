---
title: Interaction Control Component release notes
description: Version history for the Interaction Control Component application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-interaction-control-component.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Customer Service Management release notes, ServiceNow Store release notes]
---

# Interaction Control Component release notes

Version history for the Interaction Control Component application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.6.0 - June 2026 \(Australia\)**
    -   New in this release:
        -   Agent-initiated Call Wrap-Up:
        -   Overflow menu for active calls:
    -   Fixed in this release: Initiating an outbound call from the Active Call window now populates the caller\_phone\_number field with the dialed number on the interaction record. This is an ARIA accessibility fix.
-   **Version 4.3.1 - May 2026 \(Australia\)**

    New in this release: Accessibility improvements for phone directory, phone search, and supervisor actions.

-   **Version 3.2.3 - May 2026 \(Zurich\)**
    -   Fixed in this release:
        -   The following features have been enhanced to improve user experience:
            -   Global Call page – The phone number field now clears automatically after a call is placed, reducing manual steps between calls.
            -   Outbound Call page – The Enter key initiates a call only when outbound calling is available, preventing accidental dial attempts.
            -   Accessibility – The phone icon inside the "Enter a Number" field is no longer read out by screen readers in browse mode, improving navigation for assistive technology users.
-   **Version 4.2.0 - April 2026 \(Australia\)**
    -   New in this Release:
        -   The Transfer and Phone Directory agent target lists now display real-time agent status and call handling data.
        -   The Transfer target list and Phone Directory now support hiding individual target types \(Agent, Queue, or External\) based on CCaaS platform capabilities.
        -   When event tracking is enabled, agent interactions with voice controls are captured as event metrics for Active Call Components and available in Usage Insights under Platform Analytics.
    -   Fix in this Release:
        -   Resolved an issue where events were not published when agents cleared the outbound queue selection.
        -   Resolved an issue where the dial pad Phone Directory was missing the Call button for each contact.
-   **Version 3.2.2 - April 2026 \(Zurich\)**

    Fixed in this Release: Resolved an issue where events were not published when an agent cleared the outbound queue selection.

-   **Version 4.1.0 - March 2026 \(Australia\)**

    New in this Release: Help requested feature - Agents can now request supervisor assistance during an active call directly in the Active Call component. Upon accepting the help request, supervisors can monitor, coach, or barge-in to the call in real time.

-   **Version 3.2.0 - January 2026**
    -   New in this Release:
        -   New user interface on the keypad and phone directory for outbound queue selection.
        -   New option for Agent to mark the selected queue as default for all outbound calls.
        -   Enhanced click-to-dial feature to include outbound queue if queue selection is enabled.
-   **Version 3.1.0 - December 2025**
    -   New in this release:
        -   Supervisor Flow: Supervisors gain comprehensive call management capabilities directly within the ICC listing view, ensuring seamless oversight and intervention.
            -   NVC Active Call Component: Real-time monitoring, coaching, and barge-in via dedicated buttons.
            -   Global Call List: Extended monitoring, coaching, and barge-in capabilities, even in non-interactive pages or non-supported workspaces.
            -   CCaaS Context Integration: Dynamic enablement of supported supervisor actions based on call context.
-   **Version 2.2.3 - November 2025**
    -   Fixed in this release:
        -   The Phone Number field in the keypad now automatically initiates a call when the user presses the Return key.  Previously, users were required to click thePhone icon to start dialing.
        -   ThePhone Number field in the keypad now automatically clears once a call has been initiated.
-   **Version 3.0.2 - September 2025**

    Fixed in this release: Phone Directory and Transfer Target list now correctly retrieves and displays data from CCaaS.

-   **Version 3.0.1 - August 2025**
    -   New in this release:
        -   Interaction Controls Component support for Global call list
            -   Global call list for managing one or more calls when user moves away from the Interaction tab.
            -   Phone directory in the Global Call Component allowing outbound dialing. Directory contains queues, agents, and external numbers stored in CCaaS.
            -   "Open interaction" link in the global call list allows quick access to Interaction records.
        -   Interaction Controls Component support for callback functionality.
            -   List of callback numbers agents can choose to dial back the customers.
            -   Dial customer action allows callback to the customer.
            -   Close callback action enables agents to wrap up callback requests.
            -   Retry call action helps agents retry dialing the customer if the customer does not answer the phone call.
            -   Countdown timer indicates to agents that begin and end of callback happens automatically.
-   **Version 2.2.0 - May 2025**
    -   New in this release:
        -   A new tab on the Transfer UI for External \(Transfer\) when user invokes the transfer feature from an active call.
        -   The ability to transfer to a phone number directly when there is no match in the destination type \(queue, agent, or external\).
        -   A new system property \(icc\_search\_limit\) to set the number of records returned in the target list for transfer. The default minimum value is 10 and the maximum value is 25.
-   **Version 1.0.3 - March 2025**

    Fix in this release: Internal fix for UX standard naming convention.

-   **Version 1.0.0 - February 2025**

    The Interaction Controls Component is a framework that enables a Contact Center Platform to integrate with the ServiceNow Configurable Workspace. This framework provides a set of native voice call controls.


**Parent Topic:**[ServiceNow Store - Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-csm.md)

