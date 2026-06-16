---
title: Recommended Actions for Security Operations release notes
description: Version history for the Recommended Actions for Security Operations application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-sir-recommened-actions-sec-ops.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Recommended Actions for Security Operations release notes

Version history for the Recommended Actions for Security Operations application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.2.1 - June 2026**

    Changed: Updated the Query range ACL.

-   **Version 2.1.1 - March 2026**

    Fixed: \[AWS Claude\]: Error response is shown before actual results for Recommended Actions Skill.

-   **Version 2.1.0 - December 2025**
    -   New: Added support for Now LLM LTS.
    -   Changed: Recommended Actions for Security Operations skill will be active out-of-the-box.
-   **Version 2.0.0 - October 2025**

    Changed: Updated the dependent applications "Now Assist for Platform" versions to 9.2.2v \(performance optimizations\).

-   **Version 1.1.41 - September 2025**

    Changed: Defined ACLs for the Recommended Actions skill.

-   **Version 1.1.31 - August 2025**

    New: Support for Recommended Actions skill with all 4 models \(Azure Open AI, Now LLM, Google Gemini, Amazon Bedrock.\)

-   **Version 1.1.2 - June 2025**

    Fixed: A JSON parsing failure that impacted initiating the skill, generating recommended actions from a security incident, and creating a response task.

-   **Version 1.1.0 - May 2025**
    -   New:
        -   Feedback mechanism for the recommended actions.
        -   Display the top number \(n\) of recommendation cards.
-   **Version 1.0.2 - February 2025**
    -   Generate recommended actions to help you investigate incidents using information from matching KB articles and closed security incidents.
        -   Review the generated recommended actions for accuracy. You can edit and save them to work notes or create a response task.
        -   Recommended actions is supported for security incidents in the Security Incident Response Workspace and in UI16 \(legacy\).
-   **Version 1.0.0 - November 2024**

    This application leverages GenAI capabilities to generate recommended actions for resolving incidents efficiently, eliminating the need to consult multiple closed incidents or KB articles.


**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)

