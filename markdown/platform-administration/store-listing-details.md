---
title: ServiceNow Store application listing details
description: The listing details page for a ServiceNow Store application shows information about the app and its features, as well as technical information about the versions available.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-08-12"
reading_time_minutes: 3
breadcrumb: [Explore, ServiceNow Store, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# ServiceNow Store application listing details

The listing details page for a ServiceNow Store application shows information about the app and its features, as well as technical information about the versions available.

You can view an app's listing details by selecting an app in the ServiceNow Store. Listing details include a header with procurement options, app details, and version details.

## Header

The listing details header shows procurement options, as well as basic information like the application name and the provider. For partner applications, you can select the provider name to view the seller profile.

![Now Assist Admin Console header displaying Accept Terms procurement option.](../image/store-details-header.png)

There are a number of possible procurement options and additional statuses that can be found in the listing details header. For a description of the different procurement options, see [ServiceNow Store procurement options](../reference/store-procurement-ops.md).

Procurement options might be updated or replaced with status messages depending on what actions you take. For example, once you request a trial, the button with that option is replaced with a status message letting you know the trial has been requested. After the trial has been approved, the message will be replaced with an option to start the 30-day trial.

Application status messages in the ServiceNow Store are based only on the procurement status of an application. After an application is fully procured, a message that it's available for installation is displayed. Installation can be managed through the Application Manager. For more information, see [Application Manager](../../application-manager/concept/application-manager.md).

## App details

The app details section includes the following information:

-   **Summary**

    An overview of key information about the application, including the following:

    -   Rating
    -   Pricing
    -   Custom table count \(the number of unallocated custom tables this application requires\)
    -   Latest version
    -   Compatibility
-   **Description**

    An overview of what the application can help you accomplish on your ServiceNow AI Platform instance.

-   **Key features**

    A list of features and capabilities the application can add to your ServiceNow AI Platform instance.

-   **Ratings and reviews**

    A summary of ratings on a five-star scale, where five stars is the best, and a list of user reviews. For more information about leaving reviews, see [Reviewing apps](reviewing-apps.md).

-   **Links and documents**

    Additional information made available by the provider. Links and documents might include product documentation, release notes, installation guides, case studies, and more.

-   **Licensing requirements**

    A description of custom table requirements, AI usage, and subscription considerations for applications on the ServiceNow Store.

-   **Terms and conditions**

    Downloadable ServiceNow Store terms of use and any terms and any other conditions applicable for the application.

-   **Contacts**

    For partner applications, this shows contact information for the application provider. For applications built by ServiceNow, contact your account administrator or a sales agent.


## Version details

The version details section includes the following information:

-   **Version summary**

    Displays release date, custom table count, and platform release compatibility for the selected version. Select available platform release versions and application versions using the drop-down menus at the beginning of the version summary.

-   **Release notes**

    Information about what's been added, removed, or fixed in the selected application version.

-   **Requirements**

    Hardware and software requirements for the application.

-   **Dependencies**

    Lists of application dependencies and plugin dependencies that are required for the application to function correctly. For more information about dependencies, see [Evaluating version requirements and dependencies](versions-dependencies.md).


