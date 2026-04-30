---
title: Working with Reliability metrics
description: Use the SRM reliability metrics to define service level indicators \(SLI\), service level objectives \(SLO\), and error budget policies to track your service health and take necessary actions.
locale: en-US
release: xanadu
product: Service Level Objective Management
classification: service-level-objective-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Using SLO Management, Service Level Objective Management, ITOM Health, IT Operations Management]
---

# Working with Reliability metrics

Use the SRM reliability metrics to define service level indicators \(SLI\), service level objectives \(SLO\), and error budget policies to track your service health and take necessary actions.

## High-level workflow

1.  SRM leverages integrations for signal aggregation.
2.  Reliability indicators containing SLIs and SLOs are created for the service in SRM.
3.  When a qualified alert is generated for a service, the cumulative breach and the error budget values are updated for the reliability indicators in SRM.
4.  An error budget policy is created for the service to trigger actions such as creating an incident or sending an email to remediate service issues. Error budgets are constrained by Category.

The key features of the SRM metrics are:

-   SLI signal aggregation
-   Create duration and count based service level objectives
-   Calculate error budgets \(EB\)
-   Error budget policies
-   Error budget visualization

Navigate to the **Services** &gt; **Overview** tab to view all associated critical data for Reliability and Error Budget metrics. See [Working with SRM services](../../service-reliability/concept/sr-work-services.md) for more information.

**Note:** Scores are only visible when SLIs and SLOs and Error budgets have been created and there are affected. See [Create SLO, SLI, and Error budget policies](../task/sr-create-slo-sli.md) for more detailed information.

## Reliability metrics tab

Navigate to the **Services** &gt; **Reliability metrics** tab to view the service level objectives \(SLO\) for a service.

![The reliability metrics tab shows a list of the service level objectives for a selected service.](../../service-reliability/image/sr-slo-list-view.png "SRM reliability metrics list view")

**Note:** Updating the SLO changes the state and results in retiring this SLO record and creating a new copy for accurate monitoring purposes.

## Reliability metrics

**Service Level Objectives** show the following details:

-   **Service level objective**: Name of the SLO. The SLO is a target value or the objective that your team must hit to meet your service level agreement \(SLA\).
-   **SLI type**: The real numbers on the performance of your service.

    The SLI types are:

    -   Availability: Percentage of time your service is available. Also called uptime. Availability is the basic metric for reliability. \(Default\).
    -   Errors: Measures the frequency of your service errors.
    -   Latency: Time it takes to service a request. The actual amount of time that elapsed.
    -   Saturation: Measures the “fullness” of your system, emphasizing the resources that are most constrained.
-   **Compliance period**:

    How long the SLO is set to last.

    -   **Month**: The duration is considered to be the current month. For example, if the current date is 26th January, the duration will be considered from 1st January until 31st January.
    -   **Rolling 7 days**: The duration is considered to be 7 days from the current date.
    -   **Rolling 30 days**: The duration is considered to be 30 days from the current date. For example, if the current date is 26th January, the duration will be considered from 25th December.
    -   **Rolling 90 days**: The duration is considered to be 90 days from the current date. For example, if the current date is 26th January, the duration will be considered from 25th October.
-   **State**:

    State of the SLO. Choices are:

    -   Draft: The SLO isn't running in your instance yet. You can add new SLIs or update existing SLIs and you can delete the SLO.
    -   Running: The SLO is active in your instance. You can edit, retire, or delete the SLO.

        **Note:** Editing an SLO in the running state retires it and a new copy is created.

    -   Retired: The SLO is no longer running in your instance. You can reactivate it.
-   **Objective \(%\)**: Percentage of the desired SLI performance.
-   **Limit occurrences**: Number of limit breaches that have occurred. \(Used by Count SLO types.\)
-   **Service level indicator**: Real numbers on the performance of your service. Measurable facts that indicate whether you’re meeting the customers’ expectations.
-   **Error budget**: How much error budget you can spend. When creating a SLO, the error budget is calculated based on the provided Compliance period and Objective \(%\).
-   **Remaining error budget**: How much error budget is left.
-   **Remaining breach occurrences**: Number of breaches left before the limit is reached.

**Note:** Service level objective history \[sn\_sow\_srm\_slo\_history\] and Service level indicator metric \[sn\_sow\_srm\_sli\_metric\] records are archived after one year and destroyed five years after that. Doing this is expected to result in greater performance along with equal longevity data retention. No queries are run against archived tables.

-   **[Create SLO, SLI, and Error budget policies](../task/sr-create-slo-sli.md)**  
Create SLO, SLI, and Error budget policies to help you and your team track your service health and take the necessary actions when required.
-   **[Edit a reliability indicator](../task/sr-edit-sli-slo.md)**  
Update the details of a reliability indicator when required.

**Parent Topic:**[Using SLO Management](../task/using-service-level-objective-management.md)

