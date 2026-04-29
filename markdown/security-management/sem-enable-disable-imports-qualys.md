---
title: Enable or disable the import of test results for a Qualys test group
description: In Security Exposure Management Workspace control the import of the test results for the tests in a Qualys test group by using the Enable/Disable import button, which is available in the test group's record view.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Enable or disable the import of test results for a Qualys test group in the Vulnerability Manager Workspace]
breadcrumb: [Use, Unified Security Exposure Management, Security Operations]
---

# Enable or disable the import of test results for a Qualys test group

In Security Exposure Management Workspace control the import of the test results for the tests in a Qualys test group by using the **Enable/Disable import** button, which is available in the test group's record view.

## Before you begin

Role required:

-   sn\_vul.vulnerability\_analyst, sn\_vul.vulnerability\_admin, or sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_sec\_manager, sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.vulnerability\_analyst, sn\_vul\_container.vulnerability\_admin, or sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.admin, sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management** &gt; **Lists**.

2.  In the **Libraries**, under the **Test Groups** list, open a Qualys test group in the record view.

3.  Disable the import of the test results associated with a Qualys test group by selecting the **Disable import** button.

    From the upcoming data ingestion, the test results aren’t imported for the Qualys test group.

    The value in the **Is Import disabled** field changes to true.

4.  Enable the import of the test results by selecting the **Enable import** button.


**Parent Topic:**[Using Unified Security Exposure Management](../concept/using-unified-security-exposure-management.md)

