---
title: Create a scan suite
description: Create and schedule a custom suite so that you can analyze the security of your instance for your organization.
locale: en-US
release: zurich
product: Security Center
classification: security-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Scan suites, Security scanner, Security configuration console, Security Center, Platform Security]
---

# Create a scan suite

Create and schedule a custom suite so that you can analyze the security of your instance for your organization.

## Before you begin

Role required: admin or sn\_vsc.security\_center\_viewer.

A suite is a collection of checks that can be used for a scan. View a list of scan suites organized in a table by navigating to **Scanner** &gt; **Suites**. Create your own suites or to use the default suite, Auditor. Auditor is a default base system suite that contains checks for security best practices. These checks consist of system properties, plugins, and tables that can affect the security posture of your instance. The following steps show how to create a suite along with the several options available for configuring them.

## Procedure

1.  In Security Center, select the **Scanner** tab, then select **Suites** in the panel on the left side of the screen.

2.  In the **Scan Suites** page, select the **New** button.

3.  Enter a suite **name** and **description**, and then select **Save**

    ![Create a new suite form](../images/create-suite-1.png)

    After selecting **Save**, configuration options for the suite display in a tabbed interface.

4.  Select the **Checks** tab.

    Use this tab to add checks to your suite.

    1.  Select **Edit**.

    2.  Select the checks that you want to add, and then select Add \(**&gt;**\) to place it in your suite.

    3.  **Save**.

5.  Select the **Child Suites** tab.

    Use this tab to add child suites. Suites added as child suites are also executed.when this suite is used in a scan.

    1.  Select **Edit**.

    2.  Select the child suites that you want to add, and then select the Add \(**&gt;**\) to place it in your child suite.

    3.  **Save**.

6.  Select the **Parent Suites** tab.

    Use this tab to add parent suites. Parent suites that are executed in a scan will also execute this suite.

    1.  Select **Edit**.

    2.  Select the child suites that you want to add, and then select Add \(**&gt;**\) to place it in your parent suite.

    3.  **Save**.

7.  Select the **Schedule** tab.

    Use this tab to set a time for your suite to execute.

    1.  Select **New**.

    2.  Enter details of the scheduled scan.

        The time fields are in the format: hour:minutes:seconds.

    3.  **Save**.


-   **[Clone the access controls auditor suite](clone-the-auditor-suite.md)**  
Clone and customize the default access controls auditor suite in your instance to create a new suite tailored to your organization's security practices.
-   **[View the Access Controls Auditor Suite](view-access-controls-auditor-suites.md)**  
View the checks available in the default Access Controls Auditor Suites to understand which checks are executed when this suite runs.

**Parent Topic:**[Scan suites](../concept/sec-center-suites.md)

