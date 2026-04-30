---
title: Run scheduled job to generate risk values
description: The risks on the product model and business application is time dependent. Based on the external and internal lifecycles the risk changes every day, hence the risk must be calculated daily. A scheduled job is created that runs daily and calculates the risks of the software model and the business application.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Run scheduled job to generate risk values

The risks on the product model and business application is time dependent. Based on the external and internal lifecycles the risk changes every day, hence the risk must be calculated daily. A scheduled job is created that runs daily and calculates the risks of the software model and the business application.

## Before you begin

**Important:**

Starting with the Xanadu release, the legacy Technology Portfolio Management module is moved to the Enterprise Architecture Workspace. To learn more, see [Managing the Technology Portfolio Management \(TPM\) in Enterprise Architecture Workspace](../concept/eaw-concept/eaw-tpm.md).

Role required: admin

## About this task

**Load TPM Risk Parameters and compute Application Service Risks** scheduled job must be run daily to calculate the product model risk. The scheduled job executes the script generating the application service risk values. You can configure the time in the script as per your preference. Run the back-end job to get the real-time status of the applications risk and store the risk data in the business application risk table.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Select the **Load TPM Risk Parameters and compute Application Service Risks** scheduled job.

    **Note:**

    The job is inactive by default. Select the **Active** check box to run the scheduled job at the scheduled time.

3.  Click **Execute Now**.

    1.  To configure the time in the script, navigate to **System Scheduler** &gt; **Scheduled Jobs** &gt; **Scheduled Jobs**.

        If a job is active, then you can schedule a time to run the job.

    2.  Select **Load TPM Risk Parameters and compute Bus**.

    3.  Click **Configure Job Definition** related link.

    4.  Click the link at the top panel to edit the record.

    5.  Click **Execute Now**.

        After executing the scheduled job, the engine automatically stores the risk values in the Business Application Risk \[sn\_apm\_tpm\_business\_application\_risk\] table. It updates the values in the table each time after you run the job.

    6.  Navigate to **Enterprise Architecture** &gt; **Technology Portfolio Management \(TPM\)** &gt; **Business Application Risk Values**.

    7.  View the risk record of each business application in the table.

        The risk values are:

        -   **High**

            One or more than one associated application service is at high risk.

        -   **Medium**

            One or more than one associated application service is at medium risk.

        -   **Low**

            One or all the associated application services are at low risk.

        -   **Not Assessed**

            Either the business application does not have any application service associated to it or the associated application service is not of production type.


## Result

The TPM risk engine loads the risk parameters, runs, and generates the risk parameter scores, software model risk values, hardware model risk values, and application service risk values.

## What to do next

Navigate to the following tables to view the risk values and scores:

-   Navigate to **Enterprise Architecture** &gt; **Technology Portfolio Management \(TPM\)** &gt; **Risk Parameter Scores** to view the scores of the risk parameters.
-   Navigate to **Enterprise Architecture** &gt; **Technology Portfolio Management \(TPM\)** &gt; **Hardware Model Risk Values** to view the risks of the hardware models.
-   Navigate to **Enterprise Architecture** &gt; **Technology Portfolio Management \(TPM\)** &gt; **Software Model Risk Values** to view the risks of the software models.
-   Navigate to **Enterprise Architecture** &gt; **Technology Portfolio Management \(TPM\)** &gt; **Application Service Risk Values** to view the risks of the application services.

The risk values of the business applications, application services, hardware, and software models are rendered on the [Technology Portfolio Management timeline](view-technology-risks-in-timeline.md).

**Parent Topic:**[Configuring Enterprise Architecture \(formerly Application Portfolio Management\)](../concept/configure-apm.md)

