---
title: Run the Service Exchange pre-configuration scan
description: Track errors on recent transactions, see connection status, run health checks, and receive recommendations to improve the health of your Impact instance for connection with Service Exchange.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-11-20"
reading_time_minutes: 2
breadcrumb: [Configure the Impact Store Application, Configuring Impact, Impact]
---

# Run the Service Exchange pre-configuration scan

Track errors on recent transactions, see connection status, run health checks, and receive recommendations to improve the health of your Impact instance for connection with Service Exchange.

## Before you begin

Role required: admin, impact admin

For more information on Service Bridge, see [Secure data transfer using Service Bridge](../concept/service-bridge-overview.md).

## About this task

View and diagnose errors and follow the steps provided to resolve the errors. Each error record provides the following details:

-   A detailed description of the error
-   Reason the error has occurred
-   Steps to resolve the error

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Configuration** &gt; **Guided Setup**.

    The Guided Setup overview page displays.

2.  Select **Continue**.

3.  In the Task section of Service Exchange Pre-configuration Scan, select **Start Service Bridge Health scan**.

4.  Select **Execute Suite Scan** on the Service Bridge Pre-Onboarding page.

    You are redirected to the ServiceBridge Pre-onboarding page.

    ![The ServiceBridge Pre-onboarding screen with the Execute Suite Scan button displayed.](../image/impact-execute-health-scan.png)

5.  Select the **Full Instance** targets scan option.

    ![Scan Suites target selection page.](../image/impact-servicebridge-scan-scope.png)

6.  Select **Execute Scan**.

    A progress bar displays with the scan summary information.

7.  Select **Go to Result** after 100% of the scans have completed.

8.  On the Scan Findings tab, open the link in the Task column to view details of issues that were discovered.

    The **Results Dashboard** related link displays a dashboard view of the scan results.

    ![Scan findings page where you can select a findings link for resolution options.](../image/servicebridge-health-findings.png)

9.  Address task items in the Scan Task description and refer to Known Error Documentation in the Notes section for information to assist you with solutions to the task.

    **Warning:** If there are remaining issues on the Scan Findings tab, contact your Impact CSM before continuing to register your Impact Store Application.

10. Upon completion, select **Mark as complete**.

11. Close the Pre-configuration checks and return to Guided setup to continue registering your instance.


## What to do next

See [Use automated registration to connect to the Impact Delivery Instance](start-automated-registration-IDI.md) to proceed with setup.

**Parent Topic:**[Configure the Impact Store Application](../concept/configuring-impact-platform.md)

**Previous topic:**[Run your first scan with the Scan Engine](run-scan-engine.md)

**Next topic:**[Use automated registration to connect to the Impact Delivery Instance](start-automated-registration-IDI.md)

