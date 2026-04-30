---
title: Employee Return to Workplace lifecycle event
description: The Employee Return to Workplace lifecycle event helps to verify that your employees who are working from home are ready to return to the workplace.
locale: en-US
release: yokohama
product: Safe Workplace
classification: safe-workplace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Return to Workplace Location Readiness and Employee Return to Workplace lifecycle events, Enterprise Employee Experience Pack, Safe Workplace, Health and Safety, Employee Service Management]
---

# Employee Return to Workplace lifecycle event

The Employee Return to Workplace lifecycle event helps to verify that your employees who are working from home are ready to return to the workplace.

The Employee Return to Workplace lifecycle event provides you with preconfigured process flows, activity sets, activities, templates, and sample content items.

**Note:** Clone this lifecycle event prior to updating it with your company's specific information. For more information on cloning, see [Clone a lifecycle event](../../human-resources/task/clone-lifecycle-event.md).![Employee Return to Workplace - LIfecycle event](../images/employee-return-workplace.png)

## HR case

These HR cases start the Return to Workplace process.

-   Request for Employee to Return to Workplace
-   Request to prepare a workplace to reopen

Employees, managers, or HR agents can use the Employee Service Center or Service Portal to create the HR case.

HR agents can also use the HR case form.

After the HR case is created and in the Ready state, a survey is sent to the employee. The first activity in the Employee Return to Workplace lifecycle event is the Employee Readiness Assessment.

## Employee Return to Workplace - Lifecycle Event

Contains the following activity sets:

## Notify Employees - Activity Set

Contains the following activity:

Employee Readiness Assessment: An HR task for employees that collects feedback using the Employee Readiness Assessment HR survey.

-   The first question on the survey is: How do you feel about a possible return to your workplace?
-   The answer provided by the employee maps directly to the HR case form and HR profile of the employee.
-   If the employee answers **Yes** and provides a date of return, the Get ready to return activity set triggers. The employee becomes part of the **User has Return to Workplace date** audience.
-   If the employee answers **I'm not ready to return** or **I'm not sure**, an HR task is assigned to an HR agent. The employee becomes part of the **Employee Return to Workplace** audience.

## Get ready to return - Activity Set

Contains the following activities:

-   Review workplace health &amp; safety guidelines: An HR task for employees that provides a URL link to a knowledge base \(KB\) article. The KB article provides workplace health and safety guidelines.
-   Reactivate badges and parking passes: An HR task for agents to verify that work badges and parking passes are activated for employees.
-   Review employee's concerns about returning to the workplace: An HR task for agents to review the employee readiness assessments.
-   Self-service space reservation: An HR task for employees that provides a URL to select a shift or reserve space to work.

## Final Prep - Activity Set

Contains the following activities:

-   Packing checklist for returning to the workplace: An HR task for employees to confirm that a checklist of items is completed before returning to work.
-   Employee Health and Safety Prep activities:
    -   Request PPE: An optional HR task for employees requesting Personal Protective Equipment \(PPE\).
    -   Complete Health Verification: An HR task for employees to complete their health verification form prior to working on site.

## Back at the workplace - Activity Set

Contains the following activities:

-   Check in any borrowed equipment to IT: An HR task for employees to return any borrowed IT equipment while working from home.
-   Complete contact log: An HR task for the employee to complete their daily contact log after their first day back in the office.

## Follow Up - Activity Set

Contains the following activities:

Employee Feedback: An HR task assigned to employees that collects feedback using the Feedback on your Return to Workplace Experience survey.

**Parent Topic:**[Return to Workplace Location Readiness and Employee Return to Workplace lifecycle events](return-workplace-le.md)

