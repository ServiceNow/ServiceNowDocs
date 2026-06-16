---
title: Service Bridge release notes
description: Version history for the Service Exchange application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-telecom-service-bridge.html
release: store
topic_type: reference
last_updated: "2023-11-02"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Technology Provider Service Management release notes, ServiceNow Store release notes]
---

# Service Bridge release notes

Version history for the Service Exchange application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.2.4 - November 2023 \(Legacy\)**

    Fixed: Various stability fixes around entitlements, attachments, and cross-scope issues.

-   **Version 3.2.2 - August 2023**
    -   Fixed
        -   Remote Task
            -   Fixed issue where inbound field changes were not getting written to work notes on the parent task.
            -   Fixed an issue where duplicate remote tasks could be created for a single parent and connection.
-   **Version 3.2.0 - May 2023**
    -   New:
        -   Support for Glide List field types in Remote Task mappings
        -   Global transforms added that work across all connected accounts
    -   Changed: Attachments now sync to the parent record of a Remote Task instead of just writing a comment.
-   **Version 3.1.2 - February 2023**
    -   New: Added field dependencies to Remote Choice fields
    -   Fixed:
        -   Updated column labels to all use sentence case
        -   Providers can no longer create configurations before completing provider setup
-   **Version 3.1.1 - December 2022**

    Fixed: Domain Separation - Tasks not getting inserted with the correct domain

-   **Version 3.1.0 - November 2022**
    -   New:
        -   Remote Choice- Enables a customer to read the choice list for a reference variable directly from the providers instance. Remote Choice can eliminate the need for many replication-type integrations.
        -   Transform Framework- Enables a provider to transform inbound and outbound data for Remote Task connections with their customers. e.g. simple matching transforms like state-to-state or advanced transforms like converting references to correlated IDs.
    -   Fixed: The Provider task field on the Provider Request table now gets updated on the customer instance for proactive cases.
-   **Version 3.0.0 - August 2022**
    -   New:
        -   Service Bridge: Authorized User: Add and manage user access to create requests and orders from the published items in the service catalog on the customer's ServiceNow instance. This feature also allows the customer to manage the list of users within the criteria provided by the provider from their own instance.
        -   Service Bridge: Remote Task: Resolve and fulfill multiple customer tasks, such as incidents, cases, and service requests. This feature eases the synchronization and configuration of tasks in between the instances of provider and customer. Remote Task Outbound Assignment enables the sender to provide more relevant information for the incident or case or request. Remote Task Inbound Assignment enables the receiver to take action on the incident or case or request.
    -   Changed:
        -   Only one active group for administrative tasks and automated emails: In previous versions of the Service Bridge application, there were two admin groups, Service Bridge Admins for the automated email notifications and Service Bridge Admin Group for all administrative tasks. Starting with the Tokyo release, the Service Bridge Admins group is removed and all of its users are moved to the group Service Bridge Admin Group. Service Bridge Admin Group has been renamed to Service Bridge Admins. This group is now used to manage both administrative tasks and email notifications.
        -   Creation of cases through a new Service Bridge channel in CSM: Starting with the Tokyo release of Service Bridge, case tasks in the provider's instance are now created with the channel set to Service Bridge instead of eBonding.
-   **Version 2.0.1 - May 2022**
    -   Fixed:
        -   Comments sync on Provider request will be synchronous to avoid sync issues
        -   Support for work notes sync on Provider request
        -   Fixed state sync issues on Provider request
-   **Version 2.0.0 - February 2022**
    -   New:
        -   Ability to directly publish remote record producers from one instance to another
        -   Ability to automatically keep items up to date across all customers
-   **Version 1.2.0 - July 2021**

    Changed: Application Name changes and bug fixes.

-   **Version 1.1.3 - May 2021**

    Changed: Minor release to remove an internal application dependency.

-   **Version 1.1.0 - March 2021**

    New: This release incorporates an update to the new service catalog state model which extends to remote record producers in eBonding applications.

-   **Version 1.0.1 - December 2020**

    New: Added support to replicate Product Offerings and Customer Orders triggered from those Product Offerings

-   **Version 1.0.0 - September 2020**

    Enables enterprise customers to request services from their telecommunications service provider and track delivery of those services from their own IT Service Portal.


