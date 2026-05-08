---
title: Migrate from the ServiceNow Classic mobile app to the ServiceNow Mobile Platform
description: Migrate from the Mobile Classic app to the Mobile Platform to take advantage of features such as rapid development, offline capabilities, and native mobile device feature integrations.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Plugins &amp; upgrades, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Migrate from the ServiceNow Classic mobile app to the ServiceNow Mobile Platform

Migrate from the Mobile Classic app to the Mobile Platform to take advantage of features such as rapid development, offline capabilities, and native mobile device feature integrations.

## Understand the benefits of migration to ServiceNow® mobile

ServiceNow Mobile Platform is a native, mobile-first design that introduces new capabilities that were not available in the ServiceNow Classic mobile app. For more information about the deprecation of the ServiceNow Classic mobile app and migration resources, see the ServiceNow Community website article [Mobile Classic Deprecation Effective September 2022](https://www.servicenow.com/community/mobile-apps-platform-articles/update-servicenow-classic-mobile-app-deprecation-effective/ta-p/2301729).

**Note:** You must have an account and password to access the above link to the ServiceNow Community website.

-   Rapid, low code application development using Mobile Platform and Mobile App Builder.
-   Base system applications including, but not limited to Customer Service Management, IT Service Management, and others as listed later in the topic.
-   Integration with native mobile device features, such as camera, phone, SMS, and map apps.
-   Offline capabilities, including offline read and write.
-   Enhanced security features including data loss prevention.

For more detail on ServiceNow® mobile, see [Mobile Configuration and Navigation](mobile-config-navigation.md).

## Evaluate your organization's current mobile use

Start off with a list of business goals and determine which features your users need most. Consider which screens, fields, and actions your users use frequently, as well as what functionality your users do not use.

There is no direct method of transferring the ServiceNow Classic mobile app components into the Mobile Platform. You can create the same functionality available to your users with base system applications and manually building mobile applications in the ServiceNow® mobile framework.

## Use base system applications when possible

ServiceNow provides several base system applications to get you started quickly with commonly used functionality. Base system applications are tested by ServiceNow, and receive updates automatically as you upgrade your instance. ServiceNow offers many base system store applications or plugins, some of which include experiences for:

-   Customer Service Management
-   Employee Experience Suite
-   Field Service Management
-   Incident Management
-   IT Operations Management
-   IT Asset Management
-   IT Service Management
-   Security Operations
-   Risk
-   HR
-   Finance

Use these applications right away, or customize them to suit your business needs using Mobile App Builder.

-   **Mobile experience for Customer Service Management**

    Manage customer service cases from a mobile device with the Customer Service Management mobile application. Stay connected and access information in real time to complete tasks quickly. For more detail, see Mobile experience for Customer Service Management.

-   **Mobile experience for Employee Experience Suite**

    Approve catalog requests, requested items, or change requests from anywhere using the ITSM Mobile Agent app. For more detail, see ITSM Mobile agent.

-   **Mobile experience for Field Service Management**

    Manage your field service tasks anywhere using the Field Service Management mobile application. With this application, you stay connected with your mobile device, can access important information, and complete your tasks quickly. For more detail, see Mobile experience for Field Service Management.


## Create your own applications

Use Mobile App Builder to make new applications, and give your users the ability to work in areas not covered by the current base system applications. For details on the components of ServiceNow® mobile and examples of application creation, see [Configuring the Mobile Platform](config-mobile-platform-landing.md) and [Building mobile apps](build-mobile-apps-landing.md).

## Understand the current limitations for ServiceNow® mobile

-   **General**
    -   Limited support for client scripts. Basic functionality can be addressed with Mobile UI Rules. See, [Mobile UI Rules](mobile-ui-rules.md).
    -   Geolocation and Offline mode is not supported in the Now Mobile app.
-   **Offline mode**

    Mobile apps do not automatically go into offline mode when internet connection is lost.


**Parent Topic:**[Mobile plugins and upgrades](plugins-upgrades.md)

