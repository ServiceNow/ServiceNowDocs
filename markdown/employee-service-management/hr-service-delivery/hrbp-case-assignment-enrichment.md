---
title: HR case assignment and enrichment for HR business partners
description: One or more HR business partners are assigned to an HR case through data access rule or manual assignment. The enrichment process then adds an urgency, a summary, and a recommended resolution to the case. This sequence determines which HR business partner is assigned to a case and why the summary is generated after the assignment rather than with it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/hr-service-delivery/hrbp-case-assignment-enrichment.html
release: brazil
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-09-21"
reading_time_minutes: 6
keywords: [case assignment, data access, AI enrichment, reconciliation, assignment engine]
breadcrumb: [Explore, HRBP productivity assistant, HR Service Delivery, Employee Service Management]
---

# HR case assignment and enrichment for HR business partners

One or more HR business partners are assigned to an HR case through data access rule or manual assignment. The enrichment process then adds an urgency, a summary, and a recommended resolution to the case. This sequence determines which HR business partner is assigned to a case and why the summary is generated after the assignment rather than with it.

Two processes prepare an HR case for an HR business partner. First, the data access rules or a manual assignment determine which HR business partner the case goes to. Then, if the HR Case Enrichment skill is active, the enrichment process adds an urgency, a summary, and a recommended resolution to the case.

## Employee coverage

A data access record defines the population of employees that an HR business partner covers. The rules associated with a data access record define the population by leaders, departments, and locations. Each of these dimensions produces its own set of employees.

-   **Leaders**

    A leader and all employees in the reporting chain of that leader, including indirect reports.

-   **Departments**

    All employees in the specified departments and their child departments.

-   **Locations**

    All employees at the specified locations and their child locations.


The **Match all** check box on the rule determines how the sets of employees combine.

-   When you select the check box, an employee must match every dimension set on the rule, which narrows the population.
-   When you clear the check box, an employee who matches any one dimension is included, which widens the population.

An assignment record connects an HR business partner to a data access record. A data access record can have multiple assignment records.

To create these records, see [Define HRBP data access and data access rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown).

## Case assignment

An HR business partner is assigned a case through a data access rule or through manual assignment. A data access rule assigns a case only when the case meets all of the following conditions:

-   The case is active.
-   The case has a subject person.
-   Auto-assignment is enabled on the HR service of the case.

For Employee Relations cases, data access rules match the involved parties on the case instead of the subject person. This matching applies only when the Employee Relations plugin \(com.sn\_hr\_employee\_relations\) is active.

A case can have more than one HR business partner. The case assignment for each HR business partner identifies whether a data access rule or a manual assignment added the HR business partner. When a data access rule assigns the case, that rule is also identified in the case assignment record. This record lets you trace why a case went to a specific HR business partner.

The following changes re-evaluate rule-based assignments in the background. Re-evaluation deactivates rule-based assignments that no longer match and leaves manual assignments unchanged.

-   **Case changes**

    When a case is created, or when the subject person or state of a case changes, a business rule re-evaluates the assignments for that case.

-   **Organizational changes**

    When the department, location, or manager of an employee changes, a business rule on the user record resynchronizes the active cases for that employee. A manager change affects everyone in that reporting chain, so the business rule also re-evaluates up to 1,000 of their direct and indirect reports. Weekly reconciliation picks up any employees beyond that limit. The re-evaluation runs in the background after the user record update completes.

-   **Data access changes**

    When someone changes a data access record, a data access rule, or a data access assignment, re-evaluation of the affected cases starts.

-   **Weekly reconciliation**

    Each week, a scheduled job resynchronizes the assignments for each active case on an HR service that has auto-assignment enabled. The job picks up changes that bypass the business rules, such as bulk imports, and changes that the business rule processed before the reporting hierarchy refreshed.


The reconciliation job runs every Sunday at 5:00 a.m. in the instance time zone. Each run has a time limit and a maximum number of case records to read. If the job doesn’t finish within those limits, it queues another run to continue instead of waiting until the next week. Only one reconciliation cycle runs at a time. To change these limits, see [System properties installed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/hrpb-system-properties-installed.md).

The weekly digest runs on a separate schedule and sends the email on Mondays. Reconciliation keeps assignments current, and the digest reports on them. For the digest content and schedule, see [Configure the HRBP weekly digest](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/configure-hrbp-weekly-digest.md).

## Enrichment process

Enrichment runs each time someone manually assigns an HR business partner or auto-assignment adds one. A case qualifies for enrichment when all of the following conditions are true:

-   The Generative AI Controller plugin is active.
-   The HR Case Enrichment skill is active.
-   The case is active and has at least one active HR business partner assignment.
-   That case has no enrichment in progress.

Enrichment checks whether a case is active rather than which state the case is in. Cases that use custom states, such as states that HR Core or other HR applications add, remain eligible for enrichment. Enrichment also covers cases on tables that extend the HR Case \[sn\_hr\_core\_case\] table.

The enrichment process sets the following values, which the assistant uses to prioritize and describe cases for the HR business partner:

-   Urgency
-   Confidence score
-   Sensitivity level
-   Summary, including the source records
-   Recommended resolution
-   Resolution track

The urgency is the higher of two results: the condition-based urgency rules that match the case, and the AI evaluation of your prompt-based urgency rules. If neither result sets an urgency, the urgency is Low. For more information, see [HR case urgency rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/hr-case-urgency-rules.md).

The resolution track indicates how much judgment a case needs from an HR business partner.

-   **Human led**

    The enrichment process flags the case for escalation, the confidence score is below 40, or the sensitivity level is Medium or higher.

-   **AI automated**

    The case doesn't qualify for Human led, the urgency is Low, and the confidence score is 80 or higher.

-   **AI assisted**

    The case doesn't qualify for either of the other tracks.


If the summary can't be generated, the enrichment process completes without a summary. If the enrichment process fails, it sets the resolution track to human led. For Employee Relations cases, the assistant doesn't display the recommended resolution.

If the enrichment process sets the urgency to critical, an email notifies each assigned HR business partner without waiting for the weekly digest.

Because assignment happens before enrichment, a newly assigned case can appear before its AI summary is available. Until enrichment finishes, the case page shows that AI analysis is in progress. To review assigned cases, see [Review and act on cases with the HRBP productivity assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/review-hr-cases-pa.md).

**Important:** Content that the enrichment process generates can be inaccurate. HR business partners should review each summary, urgency, and recommendation before acting on a case.

**Parent Topic:**[Exploring the HRBP productivity assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/hrbp-pa-explore.md)

