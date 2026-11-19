---
title: Persona precedence in EmployeeWorks Web App journeys
description: When a user is both the subject person \(employee\) and the opened-for user \(Journey owner\) on a journey or lifecycle event case, employee view takes precedence.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/journey-designer/persona-precedence-ew.html
release: australia
product: Journey Designer
classification: journey-designer
topic_type: concept
last_updated: "2026-09-18"
reading_time_minutes: 1
keywords: [persona precedence, subject person, opened for, Employee Works]
breadcrumb: [Use the Journeys widget on the EmployeeWorks Web App home page, Journeys in EmployeeWorks Web App, Use, Journey designer, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Persona precedence in EmployeeWorks Web App journeys

When a user is both the subject person \(employee\) and the opened-for user \(Journey owner\) on a journey or lifecycle event case, employee view takes precedence.

## Precedence rules

EmployeeWorks determines which persona view — employee or manager - to show a user based on their relationship to the journey or lifecycle event record:

-   If the current user is the subject person or the employee, they see the employee persona view.
-   If the current user is the opened-for user \(and not the subject person\) or the journey owner, they see the manager persona view.
-   If the current user is both the subject person \(employee\) and the opened-for user \(Journey owner\), they see the employee persona view takes precedence.

## Where this applies

This precedence rule is applied consistently across the Journey Home Page widget, the Journey List page, and the Journey Details page.

**Parent Topic:**[Use the Journeys widget on the EmployeeWorks Web App home page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/journey-designer/use-journey-home-widget-ew.md)

