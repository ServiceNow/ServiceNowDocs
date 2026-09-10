---
title: Retail applications release notes
description: The ServiceNow retail applications optimize operations efficiently at retail locations. Retail applications were enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# Retail applications release notes

The ServiceNow® retail applications optimize operations efficiently at retail locations. Retail applications were enhanced and updated in the Zurich release.

## About Retail applications

-   Use the store inquiry AI agent to help retail store support agents quickly find clear, traceable answers, flag uncertain cases for human review, and benefit from tailored suggestions that improve with every resolved inquiry.
-   Simplify frontline staff access for faster response times and improved accuracy with the Retail Mobile application.
-   Initiate and coordinate large-scale actions across multiple stores with the HQ Communications case type.
-   Standardize the reporting, tracking, and resolution of in-store issues with the Retail In-store Operations case type.
-   Resolve customer complaints quickly and accurately with the Retail Customer Complaint case type.
-   Bridge the gap between stores and HQ with an intuitive request and support system using the Store Inquiry case type for stores.

See [Retail](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/retail-industry/rahi-retail-operations-overview.md) for more information.

## Activation and other requirements

**Important:** Retail applications are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install the Retail applications by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    Starting with this release onwards, the retail base case has been made abstract. \(An abstract case or abstract case type is a base configuration of a case that is intended to be extended by specialized case types rather than used directly.\) After upgrading to the Zurich release and for any version updates beginning with the Yokohama release, if you are using the retail base case table you will no longer be able to create new cases or update existing cases. Use the following case types instead:

    -   Store Inquiry
    -   Retail Customer Complaint
    -   In-store Operations
    -   HQ Communications
    You can also extend your own case types. For more information on these changes, see the [Impact analysis and guidance: Retail case table updates \[KB2216547\]](https://support.servicenow.com/nav_to.do?uri=%2Fkb_knowledge.do%3Fsys_id%3Da312916e978aa650f03d739c1253af88%26sysparm_view%3D%26sysparm_domain%3Dnull%26sysparm_domain_scope%3Dnull) article in the Now Support Knowledge Base.


## Accessibility and localization

-   **Accessibility information**
    -   **Dark theme**

        The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


-   **[ServiceNow Otto for Retail Service Management \(RSM\) release notes]()**  
The ServiceNow® ServiceNow Otto for Retail Service Management \(RSM\) application supports retail personas in efficiently managing and resolving cases. ServiceNow Otto for RSM is a new application in the Zurich release.

**Parent Topic:**[Features and changes by product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/new-features-changes.md)

