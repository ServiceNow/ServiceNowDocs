---
title: Scan suites
description: Review details on the scan suites available on your instance. Scan suites group security checks that run together, so you can scan your instance with base system suites or with custom suites that you create.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/security-center/sec-center-suites.html
release: brazil
product: Security Center
classification: security-center
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Security scanner, Security configuration console, Security Center, Platform Security]
---

# Scan suites

Review details on the scan suites available on your instance. Scan suites group security checks that run together, so you can scan your instance with base system suites or with custom suites that you create.

\[Omitted image "sc-suites.png"\] Alt text: Scan suite list and details page

Scan suites are collections of Security Center checks that execute together. You can use base system suites or create your own by cloning an existing suite and updating the checks made in the clone. For details, see [Create a scan suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/security-center/create-new-suite.md).

Select the **+Create task** button to create a Security Task related to a scan suite. For details on Security Tasks, see [Security Tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/security-center/security-task-manager.md).

## Scan suite details

\[Omitted image "sc-suites-2.png"\] Alt text: Scan suite details

Select the **Name** field of a suite to view the suite details. This page provides details on the scan suites in a tabbed interface. In the tabbed page, you can find this information:

-   **Details**

    Name, application, and description of the suite.

-   **Checks**

    List of the checks included in this suite. Details on individual checks are the same as are found in [Scan checks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/security-center/scan-checks.md).

-   **Child Suites**

    List of child suites associated with this suite. When you execute this suite, all child suites also execute.

-   **Parent Suites**

    List of suites in which this suite is a child suite. When you execute a parent suite, this suite also executes.

-   **Schedule**

    Details of the scheduled execution of this suite.


-   **[Access Controls Auditor checks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/security-center/auditor-control-checks.md)**  
Checks in the default Access Controls Auditor suites evaluate specific criteria to help you improve the security of your instance.
-   **[Auditor checks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/security-center/auditor.md)**  
Auditor suite checks in SecureCheck detect misconfigurations that can impact the security posture of your instance.
-   **[Create a scan suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/security-center/create-new-suite.md)**  
Create and schedule a custom suite so that you can analyze the security of your instance for your organization.
-   **[Reschedule a scan suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/security-center/reschedule-suite-scan.md)**  
Change the schedule of your scan suites to suit your needs.

**Parent Topic:**[Security scanner](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/security-center/sc-scanning.md)

