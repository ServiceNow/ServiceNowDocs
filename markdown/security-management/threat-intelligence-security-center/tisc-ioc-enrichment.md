---
title: Automated IOC Enrichment
description: Learn how to automate enrichment of IOC’s using flows when they match a certain criterion.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Working with automated flows, Administration, Threat Intelligence Security Center, Security Operations]
---

# Automated IOC Enrichment

Learn how to automate enrichment of IOC’s using flows when they match a certain criterion.

## Before you begin

Role required:

-   System Administrator \(view, create or edit\)
-   sn\_sec\_tisc.admin \(view\)

## About this task

Automate enrichment of IOC’s triggers only when:

-   the type of the observable is a domain name, IPv4 address, or IPv6 address.
-   the observable is in a processed state.
-   the observable does not have the tags enriched or Skip Enrichment.

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence Security Center** &gt; **Administration**.

2.  Select **Automated Flows**.

3.  Select **Automated IOC Enrichment** action link to view the respective rule details in the flow designer.

4.  View the flow designer action for the following trigger:

    ```
    Observable Updated where (Type is Domain Name, or Type is IP address (V4), or Type is IP address (V6); and Processing Status is Processed; and TISC Tags does not contain Enriched, or TISC Tags does not contain Skip Enrichment, or TISC Tags does not contain Potential New Threat)
    ```

5.  **If the observable is an IPv4 or IPv6 address and it falls within an allowed CIDR range, then:**

    1.  Add the observable to Allow List.

    2.  Update the observables tags to Skip Enrichment.

    3.  End the flow for this observable.

6.  **Else, enrich the observable data with available capabilities:**

    1.  Perform threat lookup and sighting search to gather additional information about the observable.

    2.  Update the observable with enriched data.

    3.  Add a tag **Enriched** to indicate that the IOC has been processed.

7.  **Also, if the observables reputation is clean, then:**

    1.  Mark observable as false positive and inactivate.

8.  **Else, if observable reputation is unknown**

    1.  Add tag **Not Potential Threat &amp; Enriched** to indicate that it is not a threat.

    ![Automated IOC Enrichment in TISC.](../image/tisc-automated-ioc-enrichment.png)


**Parent Topic:**[Working with automated flows](../concept/tisc-automated-flows.md)

**Related topics**  


[Analyze, assess, and disseminate observables](tisc-disseminate-observables.md)

[Analyze and assess threat IoC’s](tisc-analyze-ioc.md)

[Vulnerability Management Support](tisc-vul-mgmt.md)

[Zero-day vulnerability tracking](tisc-zero-vul.md)

[Automated flows tables](../concept/tisc-flows-tables.md)

