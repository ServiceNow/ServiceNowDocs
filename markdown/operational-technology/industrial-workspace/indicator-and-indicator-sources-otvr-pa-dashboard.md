---
title: Indicator sources and indicators for the Operational Technology Vulnerability Response \(PA\) dashboard
description: The Operational Technology Vulnerability Response application uses indicator sources and indicators to gather data and track the progress of your vulnerability remediation.
locale: en-US
release: xanadu
product: Industrial Workspace
classification: industrial-workspace
topic_type: reference
last_updated: "2025-01-22"
reading_time_minutes: 4
breadcrumb: [Use, Industrial Workspace, Operational Technology]
---

# Indicator sources and indicators for the Operational Technology Vulnerability Response \(PA\) dashboard

The Operational Technology Vulnerability Response application uses indicator sources and indicators to gather data and track the progress of your vulnerability remediation.

## Indicator sources

The Operational Technology Vulnerability Response indicators gather data from the following indicator sources. If you expect more than 1 million records to be collected from the indicator sources, you must override the expected count in the Records collection section of the indicator source. For more information, see [Review the indicator sources for a larger number of records](../task/update-indicator-source-to-collect-more-records.md).

-   **OTVI.New**

    Uses the sn\_vul\_vulnerable\_item table and collects the new OT vulnerable items.

-   **OTVI.Active**

    Uses the sn\_vul\_vulnerable\_item table and includes all the active vulnerable items in your OT system.

-   **OTVI.Closed**

    Uses the sn\_vul\_vulnerable\_item table and includes all the closed vulnerable items in your OT system.

-   **OTRT.Active**

    Uses the sn\_vul\_vulnerablity table and includes all the active remediation tasks in your OT system.


## Indicators

Several indicators are used to measure and track the progress of your vulnerability remediation in the Operational Technology Vulnerability Response application.

The **collect records** option for the indicators is inactive by default for the Operational Technology Vulnerability Response application. This option is turned off to avoid the performance issues that may occur when you collect a large amount of data for each indicator.

-   **OT Vulnerable Items**

    Number of the OT vulnerable items on the data source OTVI.Active, which uses the sn\_vul\_vulnerable\_item table. The goal is to minimize the number of vulnerable items in your system.

-   **OT Critical Vulnerable Items**

    Number of the OT critical vulnerable items on the data source OTVI.Active, which uses the sn\_vul\_vulnerable\_item table. The goal is to minimize the number of critical vulnerable items in your system.

-   **OT Unassigned Vulnerable Items**

    All active OT Vulnerable Items where both the Assignment Group and Assigned To fields are empty. The goal is to minimize the number of unassigned vulnerable items.

-   **OT Closed Vulnerable Items**

    The OT Closed Vulnerable Items indicator is measured daily as a unit number. The goal is to maximize the number of closed vulnerable items in your system.

-   **OT Deferred Vulnerable Items**

    Number of OT deferred vulnerable items on the data source OTVI.Active, which uses the sn\_vul\_vulnerable\_item table. The goal is to minimize the number of deferred vulnerable items in your system.

-   **OT Critical Deferred Vulnerable Items**

    Number of OT critical deferred vulnerable items on data source OTVI.Active, which uses the sn\_vul\_vulnerable\_item table. The goal is to minimize the number of critical deferred vulnerable items.

-   **OT Non-Deferred Overdue Critical Vulnerable Items**

    Number of OT non-deferred overdue critical vulnerable items on the data source OTVI.Active, which uses the sn\_vul\_vulnerable\_item table. The goal is to minimize the number of non-deferred overdue critical vulnerable items in your system.

-   **OT Remediation Tasks**

    Number of OT remediation tasks on the data source OTRT.Active, which uses the sn\_vul\_vulnerability table. The goal is to minimize the number of remediation tasks in your system.

-   **OT Non-Deferred Overdue Critical Remediation Tasks**

    Number of OT non-deferred overdue critical remediation tasks on the data source OTRT.Active, which uses the sn\_vul\_vulnerability table. The goal is to minimize the number of non-deferred overdue critical remediation tasks in your system.

-   **OT Non-Deferred Remediation Tasks**

    Number of OT non-deferred remediation tasks on the data source OTRT.Active, which uses the sn\_vul\_vulnerability table. The goal is to minimize the number of non-deferred remediation tasks in your system.

-   **OT Non-Deferred Critical Remediation Tasks**

    Number of OT non-deferred critical remediation tasks on the data source OTRT.Active, which uses the sn\_vul\_vulnerability table. The goal is to minimize the number of non-deferred critical remediation tasks in your system.

-   **OT Unassigned Remediation Tasks**

    All active remediation tasks where both the Assignment Group and Assigned To fields are empty. The goal is to minimize the number of unassigned remediation tasks in your system.

-   **% Vulnerable Items Met Remediation Target**

    `([[Closed Vulnerable Items > Remediation Target = Target Met]] / [[Closed Vulnerable Items]]) * 100`

    The goal is to maximize the percentage of vulnerable items that meet the remediation target in your system.

-   **OT Vulnerable Item Mean Time to Remediate**

    `[[Summed Duration of Closed Vulnerable Items]] / [[Closed Vulnerable Items]]`

-   **OT Summed Duration of Closed Vulnerable Items**

    Number of OT summed duration of closed vulnerable items on the data source OTVI.Closed, which uses the sn\_vul\_vulnerable\_item table. The goal is to minimize the summed duration of the closed vulnerable items in your system.


**Parent Topic:**[Using the Industrial Workspace](../../operational-technology-management/concept/using-industrial-workspace.md)

