---
title: Analyze and assess threat IoC’s
description: Learn how to analyze an IOC’s which are a threat and notifying the security incident team.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-analyze-ioc.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with automated flows, Administer, Threat Intelligence Security Center, Security Operations]
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

        \[Omitted image "tisc-analyze-assess-IoCs.png"\] Alt text: Analyze, assess the IoC’s related to the threat and create incident.


**Parent Topic:**[Working with automated flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-automated-flows.md)

**Related topics**  


[Automated IOC Enrichment]()

[Automated sharing of high-risk IOC's with trusted partners]()

[Automatically add threat intelligence to a TAXII collection]()

[Create vulnerability assessment for zero day]()

[Analyze, assess, and disseminate observables]()

[Vulnerability Management Support]()

[Zero-day vulnerability tracking]()

[Automatic Threat Actor priority tagging]()

[Automated flows tables]()

