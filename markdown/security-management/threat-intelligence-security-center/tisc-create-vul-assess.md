---
title: Create vulnerability assessment for zero day
description: Create a vulnerability assessment to evaluate and document security risks from zero day vulnerabilities in your environment. Use this when you want to assess the potential impact of newly discovered vulnerabilities that lack available patches.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Working with automated flows, Administer, Threat Intelligence Security Center, Security Operations]
---

# Create vulnerability assessment for zero day

Create a vulnerability assessment to evaluate and document security risks from zero day vulnerabilities in your environment. Use this when you want to assess the potential impact of newly discovered vulnerabilities that lack available patches.

## Before you begin

Role required:

-   System administrator \(view, create or edit\)
-   sn\_sec\_tisc.admin \(view\)

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence Security Center** &gt; **Administration**.

2.  Select **Automated Flows**.

3.  Select **Create vulnerability assessment for zero day vulnerabilities** link to view the respective rule details in the flow designer.

    Creates vulnerability assessment based on the provided vulnerability record.

4.  View the flow designer action for the following trigger:

    `Vulnerability Created or Updated where (Is Zero Day is true, and Processing Status is Processed, and TISC Tags does not contain Vulnerability Assessment Created)`

5.  **Create vulnerability assessment for vulnerability:**

    1.  Add tag to entity

    2.  Notify the concerned TISC Teams and VR Teams.


**Parent Topic:**[Working with automated flows](../concept/tisc-automated-flows.md)

**Related topics**  


[Automated IOC Enrichment](tisc-ioc-enrichment.md)

[Automated sharing of high-risk IOC's with trusted partners](tisc-automated-sharing-flow.md)

[Automatically add threat intelligence to a TAXII collection](tisc-taxii-automated-flow.md)

[Analyze, assess, and disseminate observables](tisc-disseminate-observables.md)

[Analyze and assess threat IoC’s](tisc-analyze-ioc.md)

[Vulnerability Management Support](tisc-vul-mgmt.md)

[Zero-day vulnerability tracking](tisc-zero-vul.md)

[Automated flows tables](../concept/tisc-flows-tables.md)

