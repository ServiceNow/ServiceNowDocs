---
title: Included health and safety requirements
description: Employee Readiness Core provides pre-built requirements.
locale: en-US
release: xanadu
product: Employee Readiness Core
classification: employee-readiness-core
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Employee Health and Safety Status, Employee Readiness Core, Safe Workplace, Health and Safety, Employee Service Management]
---

# Included health and safety requirements

Employee Readiness Core provides pre-built requirements.

Requirements are not active by default. A requirement must be activated before you can track whether employees or visitors have fulfilled the requirement. Pre-built requirements provided by Employee Readiness Core are ready to activate without any modifications. However, you can choose to edit them to meet your company's needs.

-   **Employee Health Verification Requirement**

    This requirement checks that employees have submitted their health verification. To fulfill the requirement, the health verification must have been submitted within the past seven days. Employees who don't have a record in the Employee Health Verification table \[sn\_imt\_monitoring\_health\_verification\] have a default requirement status of **Not Cleared**. This requirement uses data from the Employee Health Screening application. For more information, see [Employee Health Screening](../../employee-health-screening/concept/employee-health-screening.md).

-   **Self Report Requirement**

    This requirement checks that employees have submitted a self report with a status of **Returning to work**. Employees who don't have a record in the Crisis Task table \[sn\_imt\_quarantine\_crisis\_task\] have a default requirement status of **Not Cleared**. This requirement uses data from the Emergency Self Report application. For more information, see [Emergency Self Report](../../business-continuity/concept/emergency-self-report.md).

-   **Visitor Invitation Requirement**

    This requirement checks that visitors have agreed to follow the company safety policies outlined in their invitation email. To fulfill the requirement, the agreement must have been submitted within the past two days. Visitors who don't have a record in the Health and Safety Visitor Invitation table \[sn\_imt\_core\_visitor\_invitation\] have a default requirement status of **Not Cleared**. This requirement uses data from the Employee Readiness Core application.

-   **Exposed Contacts Requirement**

    This requirement checks the status of employees who have been added to the potentially exposed contacts list of a contact tracing case and sets their health and safety requirement status. Employees with the status of Cleared in the Exposed Contacts table \[sn\_imt\_tracing\_exposed\_contact\] have the requirement status of Cleared. Otherwise, their status is Not Cleared. This requirement uses data from the Contact Tracing application. For more information, see [Contact Tracing](../../contact-tracing/concept/contact-tracing.md).

-   **Privacy Consent Requirement**

    This requirement checks that employees have responded to the privacy consent request. Employees who responded to the privacy consent as **I Agree** have the requirement status of Cleared. Otherwise, their status is Not Cleared. This requirement uses data from the Contact Tracing application. For more information, see [Contact Tracing](../../contact-tracing/concept/contact-tracing.md).

-   **Testing Requirement Satisfied**

    This requirement checks the most recently submitted COVID-19 diagnostic test result for employees. Employees with a negative test result have a status of Cleared and employees with a positive test result have a status of Not Cleared. Employees without a test result or an inconclusive test result have a status of Cleared if they aren't a potentially exposed individual in a contact tracing case and Not Cleared if they are a potentially exposed individual. However, submitting an inconclusive test result will not change an employee’s status if they have already submitted a positive or negative result. This requirement uses data from the Health and Safety Testing and Contact Tracing applications. For more information, see [Health and Safety Testing](../../health-safety-testing/concept/health-safety-testing.md).

-   **COVID-19 Vaccine Requirement**

    This requirement checks that employees have received their COVID-19 vaccine. Employees who don't have a record in the Vaccine profile table \[sn\_imt\_vaccine\_vaccine\_profile\] have a default requirement status of **Not Cleared**. This requirement uses data from the Vaccination Status application. For more information, see [Vaccination Status](../../vaccination-status/concept/vaccination-status.md).


**Parent Topic:**[Employee Health and Safety Status](../concept/employee-health-safety-status.md)

