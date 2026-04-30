---
title: Retail applications release notes
description: The ServiceNow retail applications optimize operations efficiently at retail locations. Retail applications were enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
---

# Retail applications release notes

The ServiceNow® retail applications optimize operations efficiently at retail locations. Retail applications were enhanced and updated in the Zurich release.

## Retail highlights for the Zurich release

-   Use the store inquiry AI agent to help retail store support agents quickly find clear, traceable answers, flag uncertain cases for human review, and benefit from tailored suggestions that improve with every resolved inquiry.
-   Simplify frontline staff access for faster response times and improved accuracy with the Retail Mobile application.
-   Initiate and coordinate large-scale actions across multiple stores with the HQ Communications case type.
-   Standardize the reporting, tracking, and resolution of in-store issues with the Retail In-store Operations case type.
-   Resolve customer complaints quickly and accurately with the Retail Customer Complaint case type.
-   Bridge the gap between stores and HQ with an intuitive request and support system using the Store Inquiry case type for stores.

See [Retail](https://www.servicenow.com/docs/access?context=rahi-retail-operations-overview&version=zurich&pubname=zurich-retail-industry&ft:locale=en-US) for more information.

**Important:** Retail applications are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Retail to Zurich

Starting with this release onwards, the retail base case has been made abstract. \(An abstract case or abstract case type is a base configuration of a case that is intended to be extended by specialized case types rather than used directly.\) After upgrading to the Zurich release and for any version updates beginning with the Yokohama release, if you are using the retail base case table you will no longer be able to create new cases or update existing cases. Use the following case types instead:

-   Store Inquiry
-   Retail Customer Complaint
-   In-store Operations
-   HQ Communications

You can also extend your own case types. For more information on these changes, see the [Impact analysis and guidance: Retail case table updates \[KB2216547\]](https://support.servicenow.com/nav_to.do?uri=%2Fkb_knowledge.do%3Fsys_id%3Da312916e978aa650f03d739c1253af88%26sysparm_view%3D%26sysparm_domain%3Dnull%26sysparm_domain_scope%3Dnull) article in the Now Support Knowledge Base.

## New in the Zurich release

**Note:** The new Retail Mobile application and the new case types are available in the Yokohama release.

-   **[Retail mobile application](https://www.servicenow.com/docs/access?context=rahi-retail-retail-mobile&version=zurich&pubname=zurich-retail-industry&ft:locale=en-US) Retail Mobile application**

    As a store manager or a store associate, boost productivity by managing operations and accessing key tools on the go with the Retail Mobile application.

-   **[Customer complaint case](https://www.servicenow.com/docs/access?context=rahi-retail-retail-customer-complaint&version=zurich&pubname=zurich-retail-industry&ft:locale=en-US) Customer complaint**

    Help ensure quick and efficient customer service resolutions by capturing store-related complaints from customers using the customer complaint case type in the Retail customer complaint plugin.

-   **[Store inquiry case](https://www.servicenow.com/docs/access?context=rahi-retail-retail-store-services&version=zurich&pubname=zurich-retail-industry&ft:locale=en-US) Store inquiry**

    Streamline the process for contacting HQ for store-to-HQ cases with the store inquiry case type in the Retail Store Services plugin, which provides a clearly defined workflow for resolution at HQ.

-   **[In-store operations case](https://www.servicenow.com/docs/access?context=rahi-retail-retail-in-store-operations&version=zurich&pubname=zurich-retail-industry&ft:locale=en-US)In-store operations**

    Standardize the reporting, tracking, and resolution of in-store issues with the in-store operations case type in the Retail in-store operations plugin. This case type contributes to structured task assignments and tracking, reducing the time to resolution.

-   **[HQ communications case](https://www.servicenow.com/docs/access?context=rahi-retail-retail-hq-operations&version=zurich&pubname=zurich-retail-industry&ft:locale=en-US) HQ communications**

    Initiate and coordinate large-scale actions across multiple stores with the HQ communications case type in the Retail HQ operations plugin. Using this case type as a parent case for in-store operations simplifies coordination efforts.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Activation information

Install the Retail applications by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    The ServiceNow ® Customer Service Management \(CSM\) application provides the foundation for the Retail Core application. Leverage the functionality of CSM application to provide support to customers as well as retail sites.

-   **[Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

    The ServiceNow ® Field Service Management application aligns with Retail Core by providing capabilitie, such as work orders for use by each retail location that uses the Retail Core application.


-   **[Now Assist for Retail Service Management \(RSM\) release notes](now-assist-retail-service-management-rn.md)**  
The ServiceNow® Now Assist for Retail Service Management \(RSM\) application supports retail personas in efficiently managing and resolving cases. Now Assist for RSM is a new application in the Zurich release.

**Parent Topic:**[Features and changes by product](../new-features-changes.md)

