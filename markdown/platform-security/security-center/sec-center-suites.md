---
title: Scan suites
description: Review details on the scan suites available on your instance.
locale: en-US
release: xanadu
product: Security Center
classification: security-center
topic_type: concept
last_updated: "2024-10-28"
reading_time_minutes: 1
breadcrumb: [Security scanner, Security configuration console, Security Center, Platform Security]
---

# Scan suites

Review details on the scan suites available on your instance.

![Scan suite list and details page](../images/sc-suites.png)

Scan suites are collections of security center checks that execute together. You can use bcase system suites or create your own by cloning an existing suite and updating the checks made in the clone. For details, see [Create new suite](../task/create-new-suite.md).

The scan suites page details on the scan suites available on your instance. Select a suite to view details of the suite in a tabbed interface. In the tabbed page, you can find this information:

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
-   **[Create new suite](../task/create-new-suite.md)**  
Create and schedule a custom suite so that you can analyze the security of your instance for your organization.
-   **[Reschedule a scan suite](../task/reschedule-suite-scan.md)**  
Change the schedule of your scan suites to suit your needs.

**Parent Topic:**[Security scanner](sc-scanning.md)

