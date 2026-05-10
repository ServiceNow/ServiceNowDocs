---
title: Self-service portals
description: Self‑service portals are customer-facing websites in ServiceNow that provide an online place for customers to get information and support. They help customers help themselves by finding answers, submitting requests, and tracking progress, without needing to contact an agent for routine needs.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-28"
reading_time_minutes: 4
---

# Self-service portals

Self‑service portals are customer-facing websites in ServiceNow that provide an online place for customers to get information and support. They help customers help themselves by finding answers, submitting requests, and tracking progress, without needing to contact an agent for routine needs.

Four portals are available with the CRM products:

-   Customer Service Portal: supports B2B customers.
-   Business Portal: supports B2B customers.
-   Consumer Service Portal: supports B2C customers.
-   Consumer Portal: supports B2C customers.

These portals include ready-to-use structure and navigation with minimal setup required.

## Self-service portal applications

ServiceNow CRM includes four portal applications, each designed for a different customer relationship model. All four are built on the same Service Portal framework and draw on the same CRM data model that agents work with in the workspace. All portals offer the same self-service and Virtual Agent assistance features.

|Portal|Service model|What it provides|
|------|-------------|----------------|
|Customer Service Portal|B2B|Gives business contacts the ability to create and track cases, view sold products and install base items for their account, and access knowledge and the service catalog.|
|Business Portal|B2B \(extended\)|Extends the Customer Service Portal with a richer default layout, including taxonomy-based navigation, list views, and record detail pages. Installed automatically with the Customer Service Portal from version 24.0.0 onward.|
|Consumer Service Portal|B2C|Provides individual consumers with equivalent self-service capabilities, case creation and tracking, sold product visibility, knowledge access, and service catalog.|
|Consumer Portal|B2C \(extended\)|Extends the Consumer Service Portal with a richer default layout, including taxonomy-based navigation, list views, and record detail pages. Installed automatically with the Consumer Service Portal from version 24.0.0 onward.|

## Self-service portal capabilities

Default portal experiences help organizations provide information and support through a ready-to-use self-service portal with minimal setup. Organizations can tailor the portal to match their branding, navigation, content, and access settings.

All portals include list pages and record view pages for browsing and viewing records. The table describes what each capability provides and how the default portal supports it.

|Capability|What it provides|How the default portal supports it|
|----------|----------------|----------------------------------|
|Case and request management|Customers can submit requests, track case status in real time, and update open cases without contacting an agent.|Portals include list pages to browse, search, and filter records, and record view pages to see details, related actions, and links.|
|Knowledge base|Customers can search knowledge bases before submitting a case. Bases can be filtered by product entitlement so each customer sees relevant articles.|Portals unify knowledge and catalog browsing into a single, structured experience using taxonomy topics, with search enabling quick access to relevant knowledge articles across the portal.|
|Service catalog|Customers can browse and select catalog items to create a case automatically, without agent review or rerouting.|Portals unify knowledge and catalog browsing into a single, structured experience using taxonomy topics, with search enabling quick access to relevant catalog items across the portal.|
|Virtual Agent chat|AI-assisted conversations handle common requests, such as password resets, status updates, and routine service requests, without agent involvement.|Portals can be configured to include a Virtual Agent chat interface. The chat widget handles common requests without routing to an agent.|
|Configurable portal widgets|Admins can configure widget behavior, appearance, and content using instance options, without custom widget development.|Portals are built from configurable portal widgets. Admins configure each widget using instance options, which reduces setup time.|
|Extend with additional capabilities \(using plugins\)|Installing the relevant plugins adds the corresponding pages and widgets to the portal.|Portal list pages and record view pages display the experiences enabled by each installed plugin.|

## Self-service portal benefits

Self-service portals provide benefits to internal and external users across an organization.

-   **For administrators and implementation partners:** The default portals provide a ready-made experience tailored to your B2B or B2C use case, giving your team a head start rather than building from scratch. You can get to market faster, and because portal pages are built with configurable widgets, making changes and maintaining them over time, is significantly easier. Built‑in capabilities for case tracking, knowledge, catalog requests, and Virtual Agent reduce routine contacts from day one, reducing case volume.
-   **For customers:** When the portal is correctly configured, customers can find the information they need and resolve routine issues without contacting an agent. Whether they are tracking a case, browsing knowledge, or managing their account, customers get a relevant and consistent experience, making it easier for them to get help quickly and on their own terms.

## Use cases

-   **Enterprise software: consolidating multiple customer portals**

    A global enterprise software company supporting more than 20,000 customers had accumulated over 40 separate customer portals across its product lines. The implementation team consolidated the entire customer-facing support operation onto a single portal, with knowledge bases configured with product entitlements and Virtual Agent handling the most common request types. The outcome was a measurable shift toward self-service resolution, with improvements in first-response time, customer onboarding time, and CSAT scores.

-   **Government: citizen self-service for benefit applications**

    A state government department used ServiceNow CSM to replace a fragmented support model where citizens encountered separate support structures across multiple programs with no online self-service. Citizens can now submit applications, track status at each stage, and access information relevant to their situation from any device. The result was a shift from a program-centric service model to a citizen-centric one, with self-service replacing the majority of in-person and phone interactions for routine inquiries.


**Related topics**  


[Configure the Customer and Consumer Service Portals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-self-service-and-omnichannel-engagement/configure-csm-service-portals.md)

[Configure Business and Consumer Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-self-service-and-omnichannel-engagement/configure-business-portal.md)

