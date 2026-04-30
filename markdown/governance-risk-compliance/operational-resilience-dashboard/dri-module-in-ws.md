---
title: Explore Digital resilience incident reporting
description: The Digital resilience incident reporting module in the Operational Resilience Workspace is used to log and report incidents data to the regulators.
locale: en-US
release: zurich
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Explore Digital resilience incident reporting

The Digital resilience incident reporting module in the Operational Resilience Workspace is used to log and report incidents data to the regulators.

## Key features of Digital resilience incident reporting

The Digital resilience incident reporting application module in the Operational Resilience Workspace offers the following key features.

-   Creates reporting cases automatically from major incidents reported in the Incident Management and Security Incident Response applications.
-   Initiates a structured assessment process, including Regulatory reporting assessment to determine if the incident is reportable.
-   Tracks the status of reports and assessments, ensuring timely submission and compliance with regulatory timelines.
-   Uses automated reporting workflow to generate reports within regulatory reporting timelines:
    -   Regulatory reporting assessment of IT incidents
    -   Initial Report \(within 24 hours\)
    -   Intermediate Report \(every three days until resolved\)
    -   Final Report
-   Allows users to export incident reports for further analysis in the format specified by regulatory authorities.

## Integration with Incident Management or Security Incident Response

The Digital resilience incident reporting module is available in the Operational Resilience Workspace by default. If you are using the Incident Management or Security Incident Response applications, you can report critical incidents from these Workspaces into the Digital resilience incident reporting module.

## Auto-populating the responses in the Assessment Workspace

For the reported DIR case task, an assessment action task is created and assigned to a DIR user. Smart assessment in the Assessment Workspace is used for auto-populating the responses to the assessment. The Assessment Workspace is available to the Digital resilience incident reporting users by default.

## Incident classification

When an incident is detected, it is determined whether critical business services are affected. The following approach is followed to classify the incident.

![Classification approach.](../image/inci-classi-approach.png)

## Digital resilience incident reporting workflow

To classify major incidents, the Digital resilience incident reporting \(sn\_dri\_inc\_rptg\) automatically initiates reporting cases.

Reporting cases are triggered and reported in Digital resilience incident reporting by using one of the following conditions:

1.  Incident Management
    -   The incident is classified as critical in the Service Operations Workspace.
    -   Incident duration: The incident has been open for more than 24 hours and it is still in the **Work in progress** or **Analysis** stage.
    -   The incident involves a critical business service where the business criticality value is 1.
2.  Security Incident Response:
    -   The incident is classified as critical in the SIR workspace.
    -   Incident duration: The incident has been open for more than 24 hours and it is still in the Work in progress or Analysis stage.
3.  Manual: The incident has been reported manually in the Digital resilience incident reporting module.

## States of the case task

1.  **Draft**: Any DIR user can create a DIR case task and assign it to the DIR managers group. A notification is sent to the managers group to assign it to one of the managers. DIR case task can also be created automatically from the IM incidents or SIR incidents if they meet the criteria defined in the creation flow \(Integration with IM or SIR\)
2.  **In progress**:
    1.  An action task is created for the DIR case task and assigned to a DIR user. The breach status of the DIR case task is updated based on the response.
    2.  The DIR case task is classified as Parked for Monitoring, Not Reportable, or Reportable based on the assessment response. If it is initially marked as Parked for Monitoring, further updates on the source incident can lead to additional assessments, which may change the status to Reportable if the impacts or breach status warrant it.
    3.  If the DIR case task is identified as Reportable, a new action task is created for the initial report assessment with a due date of 24 hrs and is assigned to any DIR user by the DIR manager handling the case.
    4.  After the initial report action task is completed and submitted, a new action task for the intermediate report is created with a due date as three days.
    5.  Intermediate report assessments are generated every three days until the source incident is closed \(Incident Management or Security Incident Response\).
    6.  A final report action task is created with a due date of 30 days from the closing date of the source incident.
3.  **Pending approval** and **Approved**: Once the reports are completed, the DIR case task is approved and closed.

## Data displayed in Digital resilience incident reporting

The Digital resilience incident reporting modules display the following data on the reporting cases:

-   All incident reporting cases
-   My incident reporting cases
-   Unassigned incident reporting cases

## My tasks

The **My tasks** page in the Operational Resilience Workspace displays all the reporting cases and action tasks that have been assigned to the signed-in user. This section includes the following information for the signed-in user:

-   **My pending tasks**
-   **My items**
-   **Watchlist**

## Roles, Scripts, and Tables used for reporting

For information on the roles, scripts, and tables used in [Roles installed with Digital resilience incident reporting](../reference/roles-with-drir.md), see [Digital resilience incident reporting reference](../reference/drir-ref.md).

