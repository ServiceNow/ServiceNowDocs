---
title: Email Interaction for CSM release notes
description: Version history for the Email Interaction for CSM application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-email-interaction-csm.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Customer Service Management release notes, ServiceNow Store release notes]
---

# Email Interaction for CSM release notes

Version history for the Email Interaction for CSM application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.0.0 - June 2026**
    -   Add knowledge article links from the Recommended Actions panel to display the article title alongside the article number as a hyperlink in the email body
    -   Automatically link customer email replies received on closed interactions to the correct existing interaction or case
    -   AI summarization of email interactions
    -   Transfer CCaaS or AWA-routed email interactions to another queue or agent
-   **Version 1.6.2 - May 2026**

    Minor defect fixes.

-   **Version 1.6.0 - March 2026**
    -   Releasing:
        -   Wrap-up for email interactions
        -   Agent-initiated email interactions
        -   Transfer email interactions
-   **Version 1.5.2 - March 2026**

    Fixed minor defect.

-   **Version 1.5.0 - December 2025**
    -   Enhancements to email interaction handling include the following:
        -   External routing of email interactions is enabled to reduce administrative effort.
        -   Creation of outbound interactions on case emails is no longer available. After the upgrade, run theClose all the outbound interactions created due to case emails scheduled job to close pre-existing outbound interactions generated from case emails, ensuring data consistency and preventing records from remaining indefinitely in an open state.
-   **Version 1.1.2 - September 2025**

    Minor bug fixes.

-   **Version 1.3.0 - August 2025**
    -   Several improvements have been made to the Email Interaction agent experience:
        -   A New Activity marker highlights the latest conversation.
        -   A modeless dialog allows email replies without disrupting workflow.
        -   A compact header emphasizes key message details.
        -   The activity stream now displays only the latest reply for each email.
-   **Version 1.1.0 - May 2025**
    -   Minor Enhancements:
        -   Agents can view Contact Card and Customer History on the Email Interaction page.
        -   First Response wait time on an interaction gets populated when agent replies for the first time on an email interaction.
-   **Version 1.0.0 - February 2025**

    Email Interaction for CSM enables creation of interactions from customer emails preventing the creation of duplicate and unnecessary cases. Email interactions provides a consistent experience for agents across omnichannel interactions.


