---
title: Scan suites
description: Review details on the scan suites available on your instance.
locale: en-US
release: yokohama
product: Security Center
classification: security-center
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Security scanner, Security configuration console, Security Center, Platform Security]
---

# Scan suites

Review details on the scan suites available on your instance.

![Scan suite list and details page](../images/sc-suites.png)

Scan suites are collections of security center checks that execute together. You can use base system suites or create your own by cloning an existing suite and updating the checks made in the clone. For details, see [Create a scan suite](../task/create-new-suite.md).

Select the **+Create task** button to create a Security Task related to a scan suite. For details on Security Tasks, see [Security Tasks](security-task-manager.md).

## Scan suite details

![Scan suite details](../images/sc-suites-2.png)

Select the **Name** field of a suite to view the suite details. This page provides details on the scan suites in a tabbed interface. In the tabbed page, you can find this information:

-   **Details**

    Details on the suite include its name, application, and description.

-   **Checks**

    List of the checks included in this suite. Details on individual checks are the same as are found in [Scan checks](scan-checks.md).

-   **Child Suites**

    List of child suites associated with this suite. When you execute this suite, all child suites also execute.

-   **Parent Suites**

    List of suites in which this suite is a child suite. When you execute a parent suite, this suite is also executed.

-   **Schedule**

    Details of the scheduled execution of this suite.


-   **[Access Controls Auditor checks](../reference/auditor-control-checks.md)**  
Learn about the checks available in the default Access Controls Auditor Suites, what criteria they evaluate, and how they can be used to improve the security of your instance.
-   **[Auditor checks](../reference/auditor.md)**  
Use the Auditor suite to SecureCheck to detect misconfiguration that can impact the security posture of your instance.
-   **[Create a scan suite](../task/create-new-suite.md)**  
Create and schedule a custom suite so that you can analyze the security of your instance for your organization.
-   **[Reschedule a scan suite](../task/reschedule-suite-scan.md)**  
Change the schedule of your scan suites to suit your needs.

**Parent Topic:**[Security scanner](sc-scanning.md)

