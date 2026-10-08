---
title: Persona precedence in Employee Works journeys
description: When a user is both the subject person and the opened-for user on a journey or lifecycle event case, Employee Works shows them the employee view.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/journey-designer/persona-precedence-ew.html
release: australia
product: Journey Designer
classification: journey-designer
topic_type: concept
last_updated: "2026-09-18"
reading_time_minutes: 1
keywords: [persona precedence, subject person, opened for, Employee Works]
breadcrumb: [Journeys in EmployeeWorks Web App, AI in Journey designer, Journey designer, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Persona precedence in Employee Works journeys

When a user is both the subject person and the opened-for user on a journey or lifecycle event case, Employee Works shows them the employee view.

## Precedence rules

Employee Works determines which persona — employee or manager - to show a user based on their relationship to the journey or lifecycle event record:

-   If the current user is the subject person, they see the employee persona.
-   If the current user is the opened-for user \(and not the subject person\), they see the manager persona.
-   If the current user is both the subject person and the opened-for user, they see the employee persona subject person takes precedence.

## Where this applies

This precedence rule is applied consistently across the Journey Home Page widget, the Journey List page, and the Journey Details page header.

