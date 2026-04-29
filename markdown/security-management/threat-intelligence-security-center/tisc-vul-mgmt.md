---
title: Vulnerability Management Support
description: Learn how a new vulnerability is created in TISC with a related vulnerability in VR.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with automated flows, Administer Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# Vulnerability Management Support

Learn how a new vulnerability is created in TISC with a related vulnerability in VR.

## Before you begin

Role required:

-   System Administrator \(view, create or edit\)
-   sn\_sec\_tisc.admin \(view\)

## About this task

When new vulnerability is created in TISC and there is a related vulnerability in VR.

-   If VR vulnerability\(v2\) score is &gt; 8 OR VR vulnerability\(v3\) score is &gt; 8.
-   Total VI’s associate to it are greater than 0.

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence Security Center** &gt; **Administration**.

2.  Select **Automated Flows**.

3.  Select **Vulnerability Management Support** action link to view the respective rule details in the flow designer.

4.  View the flow designer action for the following trigger:

    ```
    When new vulnerability is created in TISC and there is a related vulnerability in VR.
    ```

5.  **If the percentage of total VI’s remediated that are associated to that vulnerability is 100%, then:**

    1.  Add a tag called Remediated to the observable.

6.  **Else, enrich the observable data with available capabilities:**

    1.  Create a remediation task for VR.

    2.  Notify the concerned VR team’s regarding it.

        ![Vulnerability management support](../image/tisc-vul-mgmt-support.png)


**Parent Topic:**[Working with automated flows](../concept/tisc-automated-flows.md)

**Related topics**  


[Automated IOC Enrichment](tisc-ioc-enrichment.md)

[Analyze, assess, and disseminate observables](tisc-disseminate-observables.md)

[Analyze and assess threat IoC’s](tisc-analyze-ioc.md)

[Zero-day vulnerability tracking](tisc-zero-vul.md)

[Automated flows tables](../concept/tisc-flows-tables.md)

