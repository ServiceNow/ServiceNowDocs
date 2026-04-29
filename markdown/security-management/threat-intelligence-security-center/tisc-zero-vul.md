---
title: Zero-day vulnerability tracking
description: Learn how to analyze RSS Feeds coming into the system.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with automated flows, Administer Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# Zero-day vulnerability tracking

Learn how to analyze RSS Feeds coming into the system.

## Before you begin

Role required:

-   System Administrator \(view, create or edit\)
-   sn\_sec\_tisc.admin \(view\)

## About this task

Whenever a new RSS Feed is created into the system, and it has a mention of ‘Zero Day’ in either title or description.

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence Security Center** &gt; **Administration**.

2.  Select **Automated Flows**.

3.  Select **Zero-day vulnerability tracking** link to view the respective rule details in the flow designer.

4.  View the flow designer action for the following trigger:

    ```
    RSS Feed Created where (Title contains zero day, or Description contains zero day, or Title contains zero_day, or Description contains zero_day, or Title contains zero-day, or Description contains zero-day)
    ```

5.  **If the observable is an IPv4 or IPv6 address and it falls within an allowed CIDR range, then:**

    1.  Create a case for TISC Team, along with a remediation task for VR Team.

    2.  Notify the concerned TISC Teams and VR Teams.


**Parent Topic:**[Working with automated flows](../concept/tisc-automated-flows.md)

**Related topics**  


[Automated IOC Enrichment](tisc-ioc-enrichment.md)

[Analyze, assess, and disseminate observables](tisc-disseminate-observables.md)

[Analyze and assess threat IoC’s](tisc-analyze-ioc.md)

[Vulnerability Management Support](tisc-vul-mgmt.md)

[Automated flows tables](../concept/tisc-flows-tables.md)

