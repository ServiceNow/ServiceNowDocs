---
title: Analyze and assess threat IoC’s
description: Learn how to analyze an IOC’s which are a threat and notifying the security incident team.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with automated flows, Administer Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# Analyze and assess threat IoC’s

Learn how to analyze an IOC’s which are a threat and notifying the security incident team.

## Before you begin

Role required:

-   System Administrator \(view, create or edit\)
-   sn\_sec\_tisc.admin \(view\)

## About this task

Whenever a sighting search enrichment is requested:

-   if the observable is sighted \(count &gt; 0\) and
-   Observable Reputation is Malicious and
-   Observable Threat score is &gt; 80 and
-   Observable Confidence &gt; 80

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence Security Center** &gt; **Administration**.

2.  Select **Automated Flows**.

3.  Select **Analyze, assess the IoCs related to the threat and create incident** action link to view the respective rule details in the flow designer.

4.  View the flow designer action for the following trigger:

    ```
    Sighting Created where (Sighting count greater than 0, and Observable. Reputation is Malicious, and Observable. Threat Score greater than 80, and Observable. Confidence greater than 80)
    ```

5.  **If Sighting Created where \(Sighting count greater than 0, and Observable. Reputation is Malicious, and Observable. Threat Score greater than 80, and Observable. Confidence greater than 80\), then:**

    1.  Create an security incident and add the observable to the incident.

    2.  Add Observables to Security Incident V1.

    3.  Send an email communication.

        ![Analyze, assess the IoC’s related to the threat and create incident.](../image/tisc-analyze-assess-IoCs.png)


**Parent Topic:**[Working with automated flows](../concept/tisc-automated-flows.md)

**Related topics**  


[Automated IOC Enrichment](tisc-ioc-enrichment.md)

[Analyze, assess, and disseminate observables](tisc-disseminate-observables.md)

[Vulnerability Management Support](tisc-vul-mgmt.md)

[Zero-day vulnerability tracking](tisc-zero-vul.md)

[Automated flows tables](../concept/tisc-flows-tables.md)

