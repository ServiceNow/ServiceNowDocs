---
title: Use Employee Profile with HR Service Delivery
description: Learn how the Employee Profile plugin works with HR Service Delivery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/employee-profile.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Employee Center, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Use Employee Profile with HR Service Delivery

Learn how the Employee Profile plugin works with HR Service Delivery.

On activating the Employee Profile plugin with HR Service Delivery, the following fields are pulled from the HR Profile \(sn\_hr\_core\_profile\) table to populate the Employee Profile \(sn\_employee\_profile\) table.

|Field|Description|
|-----|-----------|
|employment\_start\_date|Represents the employment start date.|
|employment\_end\_date|Represents the employment end date.|

**Sync employee profile from HR profile** is a one-time scheduled job that will pull all users with their corresponding employment\_start\_date and employment\_end\_date values from the HR Profile table upon plugin activation. Subsequent updates will be made by the **Synchronize fields to HR profile** and **Synchronize fields to employee profile** business rules.

**Note:** If you need to run the one-time scheduled job again, make sure to first activate the job and allow for the invalidated RCA before running it. Do not run the job on a scheduled basis.

**Parent Topic:**[Using Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/using-emp-center.md)

**Related topics**  


[Use the Employee Center topic pages]()

[Topic managers and contributors for topic page management]()

[Use the My To-dos page]()

[Use approval experience]()

[Manage approvals from Microsoft Teams]()

[Manage approvals from a Microsoft Outlook email]()

[Task filters on My tasks]()

[View the Recommended for you content]()

[Use Employee Center from Zoom]()

[View employee profile]()

[Use Personalized Answers]()

[Employee Profile org chart widget]()

[RTL support for Employee Center]()

[Manage favorites]()

[Access applications from App Launcher]()

[Use Guided Self-Service]()

