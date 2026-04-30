---
title: Domain separation for Emergency Exposure Management
description: The following table lists the domain separation use cases for service providers \(SPs\) using this application.
locale: en-US
release: yokohama
product: Emergency Exposure Management
classification: emergency-exposure-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Emergency Exposure Management, Emergency Response Management, Workplace Service Delivery, Employee Service Management]
---

# Domain separation for Emergency Exposure Management

The following table lists the domain separation use cases for service providers \(SPs\) using this application.

**Note:** This information is subject to change: Limit use to SPs only.

|Use case|Functions|Limitations|
|--------|---------|-----------|
|SP Internal - SP uses the application for internal employees who might have collaborated with an affected internal employee.|Yes|None|
|SP External - SP uses the application to identify employees \(SP or tenant\) who might have collaborated with an affected employee \(SP or tenant\).|No|Without the domain column, there is no base system platform security that prevents an SP user who has access to the application from seeing tenant information they would otherwise be restricted from seeing. “Limiting” Application Properties for Outlook settings.|
|Tenant -Tenant uses the application to identify employees who might have collaborated with an affected employee.|No|Without the domain column, there is no base system platform security that prevents a tenant user with access to the application from seeing other tenant information they would otherwise be restricted from seeing. “Limiting” Application Properties for Outlook settings.|

Some modules in the Emergency Exposure Management application are affected by domain separation.

-   **CREATE NEW &amp; ALL module \(Diagnostic Request\)**

    -   No domain column row protections or business logic exist.
    -   Creates a Diagnostic Event based on Outlook meetings, exposure to an affected user, or the user's location, to identify users who might have been potentially exposed through collaboration.
    -   Results from the Diagnostic Event return back to the Diagnostic Request or can be manually added.
    **Note:** Because the Diagnostic Request record contains the User \(Table: Sys\_User\) and Location \(Table: Cmn\_Location\) fields, visibility to those reference fields is affected by domain separation. If a user is in a domain that does not have the appropriate visibilities granted, those fields appear empty in the Diagnostic Request even if they contain data.

-   **PROPERTIES module**

    Standard Application Properties Page, all settings are global for the application.

    **Note:** This property limits the ability of Outlook support in a domain-separated environment because tenants have different settings from the service provider.

    -   No domain column row protections or business logic exist.
    -   Captures the Outlook or Location responses and sends them back to the Diagnostic Request.
    -   Purely an admin function.

**Parent Topic:**[Emergency Exposure Management](../concept/emergency-exposure-management.md)

