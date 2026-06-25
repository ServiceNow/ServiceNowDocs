---
title: Analyze, assess, and disseminate observables
description: Learn how to analyze and disseminate observables which are related to threat.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-disseminate-observables.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with automated flows, Administer, Threat Intelligence Security Center, Security Operations]
---

# Analyze, assess, and disseminate observables

Learn how to analyze and disseminate observables which are related to threat.

## Before you begin

Role required:

-   System Administrator \(view, create or edit\)
-   sn\_sec\_tisc.admin \(view\)

## About this task

Whenever a sighting search enrichment is requested, it returns with no sightings.

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence Security Center** &gt; **Administration**.

2.  Select **Automated Flows**.

3.  Select **Analyze, assess and disseminate on the IoCs related to threat** action link to view the respective rule details in the flow designer.

4.  View the flow designer action for the following trigger:

    ```
    Sighting Created where (Sighting count is 0)
    ```

5.  **The observable has a threat score greater than 80, confidence greater than 80 and reputation is malicious:**

    1.  Add the observable to deny list.

    2.  End the flow for this observable.

6.  **Else, the observable reputation is suspicious, and the threat score is in the range of 60-80:**

    1.  Add a tag called Potential New Threat.

    2.  Add the observable to watch list.

    3.  Create a case task with CTI team to track this observable and analyze further.

    4.  Link observable to the case for investigation.

        \[Omitted image "tisc-analyse-disseminate.png"\] Alt text: Analyze, assess, and disseminate on the IoC’s related to threat.


**Parent Topic:**[Working with automated flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-automated-flows.md)

**Related topics**  


[Automated IOC Enrichment]()

[Automated sharing of high-risk IOC's with trusted partners]()

[Automatically add threat intelligence to a TAXII collection]()

[Create vulnerability assessment for zero day]()

[Analyze and assess threat IoC’s]()

[Vulnerability Management Support]()

[Zero-day vulnerability tracking]()

[Automatic Threat Actor priority tagging]()

[Automated flows tables]()

