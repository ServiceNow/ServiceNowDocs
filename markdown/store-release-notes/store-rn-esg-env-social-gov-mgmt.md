---
title: Operational Sustainability Management release notes
description: Version history for the Operational Sustainability Management Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-esg-env-social-gov-mgmt.html
release: store
topic_type: reference
last_updated: "2025-09-10"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Operational Sustainability Management release notes, ServiceNow Store release notes]
---

# Operational Sustainability Management release notes

Version history for the Operational Sustainability Management Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 21.0.4 - September 2025**

    Fixed: Security vulnerabilities and minor issues related to metrics

-   **Version 19.1.5 - November 2024**
    -   Fixed:
        -   Improved workspace experience for users with low vision or those who rely on assistive technology, such as screen readers. This includes optimizing zoom capabilities.
        -   Security fixes.
-   **Version 18.1.0 - June 2024**
    -   Changed:
        -   Updated dependency of this app to latest version \(18.1.1\) of GRC: Metrics.
        -   Updated dependency of this app to latest version \(18.1.3\) of GRC: Common Workspace Elements.
        -   Updated dependency of this app to latest version \(18.1.4\) of GRC: Policy and Compliance Management.
        -   Updated event mappings of declarative actions with Form controller
-   **Version 18.0.3 - February 2024**
    -   Changed:
        -   Roles updated in the ESG Management application
            -   Several roles such as ESG administrator, ESG data owner, and ESG program manager have been updated in the ESG Management.
        -   Material topic table updated
            -   The State field in the sn\_esg\_material\_topic table has been updated to include states for risk assessment. The Review state of a material topic has also been renamed to Approval.
    -   Added:
        -   The following new tables are added to the application:
            -   sn\_esg\_disclosure\_detail
            -   sn\_esg\_disclosure\_related\_documents
            -   sn\_esg\_disclosure\_template
            -   sn\_esg\_m2m\_disclosure\_metric\_data\_by\_entity
    -   Removed:
        -   The following tables are deprecated:
            -   sn\_esg\_m2m\_risk\_goal
            -   sn\_esg\_m2m\_risk\_statement\_goal
-   **Version 17.0.1 - August 2023**
    -   Changed
    -   -   Streamline page creation, simplify maintenance, and minimize the cost of page ownership using the new record page template.
-   Exposed Metric list view to Reporting Disclosure Manager
-   Disclosure reporting capability is updated to perform aggregation of data for the period selected
-   Workspace record pages now extend new record page template which in turn extends standard record page template.
-   **Version 16.1.2 - May 2023**
    -   New:
        -   Enables disclosure reporting for ESG using Microsoft 365 add-in
    -   Changes:
        -   Authority documents and citations are segregated by functional domain 'Environment, Social, Governance'
        -   The following roles are added to ESG admin
            -   report\_user
            -   sn\_esg\_msoff\_intg.admin
        -   The following roles are added to ESG disclosure manager:
            -   report\_user
            -   sn\_esg\_msoff\_intg.reader
-   **Version 16.0.5 - February 2023**
    -   New:
        -   The following new roles are added on core tables in this application to modularize and grant granular access:
            -   sn\_esg.internal\_disclosure\_manager
            -   sn\_esg.internal\_manager
            -   sn\_esg.internal\_admin
    -   Changed:
        -   The following persona roles are modified to inherit the granular roles added:
            -   Program manager \(sn\_esg.program\_manager \)
            -   Data owner \(sn\_esg.data\_owner\)
            -   Business user \(sn\_esg.reader\)Reporting Manager\(sn\_esg.reporting\_disclosure\_manager\)
            -   Admin\(sn\_esg.admin\)
    -   Fixed: The translations are included for missing form labels and messages
-   **Version 15.1.1 - November 2022**
    -   Fixed:
        -   Translation issues
        -   Role configuration on workspace landing pages
    -   New: ESG admin role introduced
-   **Version 15.0.2 - August 2022**

    The ServiceNow ESG Management and Reporting application helps customers manage their ESG programs by providing them with a common platform to track and report goals and performance across the Environmental, Social, and Governance \(ESG\) pillars.


**Parent Topic:**[ServiceNow Store - Operational Sustainability Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-esg-highlight.md)

