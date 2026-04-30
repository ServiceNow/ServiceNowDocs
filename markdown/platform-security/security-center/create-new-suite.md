---
title: Create new suite
description: Create and schedule a custom suite so that you can analyze the security of your instance for your organization.
locale: en-US
release: xanadu
product: Security Center
classification: security-center
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Scan suites, Security scanner, Security configuration console, Security Center, Platform Security]
---

# Create new suite

Create and schedule a custom suite so that you can analyze the security of your instance for your organization.

## Before you begin

Role required: admin or sn\_vsc.security\_center\_viewer.

A suite is a collection of checks that can be used for a scan. View a list of scan suites available in your instance organized in a table by navigating to **Scanner** &gt; **Suites**. You have the ability to create your own suites or to use the default suite, Auditor: this is a default out-of-the-box suite that contains checks for security best practices. These checks consist of system properties, plugins, and tables that can affect the security posture of your instance. The following steps shows how to create a suite along with the several options available for configuring them.

## Procedure

1.  Navigate to **Suites** &gt; **New**.

2.  Enter a suite **name** and **description**, and then select **Save**.

3.  **Checks**

    This is where you add checks to your suite.

    1.  Select **Edit**.

    2.  Select the checks you want to add, and then select Add \(**&gt;**\) to place it in your suite.

    3.  **Save**.

4.  **Child Suites**

    This is where you add child suites, or the suites that are placed under the parent suites.

    1.  Select **Edit**.

    2.  Select the child suites you want to add, and then select the Add \(**&gt;**\) to place it in your child suite.

    3.  **Save**.

5.  **Parent Suites**

    This is where you add parent suites. All child suites are executed when a parent suite is used in a scan.

    1.  Select **Edit**.

    2.  Select the child suites you want to add, and then select Add \(**&gt;**\) to place it in your parent suite.

    3.  **Save**.

6.  **Schedule**

    Set a time for your suite to execute.

    1.  Select **New**.

    2.  Enter details of the scheduled scan.

        The time fields are in the format: hour:minutes:seconds.

    3.  **Save**.


-   **[Clone the access controls auditor suite](clone-the-auditor-suite.md)**  
Clone and customize the default access controls auditor suite in your instance to create a new suite tailored to your organization's security practices.
-   **[View the Access Controls Auditor Suite](view-access-controls-auditor-suites.md)**  
View the checks available in the default Access Controls Auditor Suites to understand which checks are executed when this suite runs.

**Parent Topic:**[Scan suites](../concept/sec-center-suites.md)

