---
title: Domain separation for Emergency Outreach
description: This application fully supports domain separation service provider \(SP\) use cases. The following table lists the domain separation use cases for service providers \(SPs\) using this application.
locale: en-US
release: zurich
product: Emergency Outreach
classification: emergency-outreach
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Emergency Outreach, Emergency Response Management, Workplace Service Delivery, Employee Service Management]
---

# Domain separation for Emergency Outreach

This application fully supports domain separation service provider \(SP\) use cases. The following table lists the domain separation use cases for service providers \(SPs\) using this application.

|Use case|Functions|Limitations|
|--------|---------|-----------|
|SP Internal - SP check-in admin uses the application to contact internal employees by email or through Now Mobile App.|Yes|None|
|SP External - SP check-in admin uses the application to contact tenant employees by email or through Now Mobile App.|Yes|None|
|Tenant - Tenant check-in admin uses the application to contact their employees \(in their domain only\) by email or through Now Mobile app.|Yes|None|

Some modules in the Emergency Outreach application are affected by domain separation.

-   **SEND OUTREACH module \(Create New for employee check-in table\)**
    -   Notification can be configured to target users, groups, departments, locations or customized for conditional criteria
    -   Email is standard HTML
    -   Domain column exists
-   **RESPONSE OPTIONS module \(Notification responses table\)**
    -   Domain column exists
    -   Shows response links that appear in notifications
-   **VIEW OUTREACHES module \(Employee check-in table\)**
    -   Domain column exists
    -   Shows notification structure and a related list that contains all responses \(Table: Check-In Acknowledgement\); the response table has domain column row and business logic protections
    -   Can output an Excel spreadsheet that displays current responses and status
-   **DASHBOARD module**

    Reporting dashboard, shows aggregate of all notifications and their acknowledgment status.


**Parent Topic:**[Emergency Outreach](../concept/emergency-outreach.md)

