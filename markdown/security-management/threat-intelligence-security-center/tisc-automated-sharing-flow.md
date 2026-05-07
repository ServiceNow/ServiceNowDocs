---
title: Automated sharing of high-risk IOC's with trusted partners
description: Learn how to automate sharing of high-risk IOC's with trusted partners.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Working with automated flows, Administer, Threat Intelligence Security Center, Security Operations]
---

# Automated sharing of high-risk IOC's with trusted partners

Learn how to automate sharing of high-risk IOC's with trusted partners.

## Before you begin

Role required:

-   System Administrator \(view, create or edit\)
-   sn\_sec\_tisc.admin \(view\)

## About this task

Automated sharing of high-risk IOC's with trusted partners triggers only when:

-   the type of the observable is a domain name, IPv4 address, or IPv6 address.
-   the observable is in a processed state.

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence Security Center** &gt; **Administration**.

2.  Select **Automated Flows**.

3.  Select **Automated sharing of high-risk IOC's with trusted partners** action link to view the respective rule details in the flow designer.

4.  View the flow designer action for the following triggers:

    ```
    Daily at 12.00.00
    Run every day once
    ```

5.  **Actions**:

    1.  Look Up System Property Record and Browse outbound intelligence threshold limit:

        ```
        Look Up System Property Record where (Name is sn_sec_tisc.shared_intelligence_entity_threshold).
        ```

    2.  IOC type = IP, Domain, Hash; Reputation = Malicious ; confidence &gt;= 80 or Threat Score &gt;=80.

        ```
        Look Up Observable Records where (Type is IP address (V4), or Type is IP address (V6), or Type is Domain Name, or Type is MD5 hash; and Confidence greater than 80, and Reputation is Malicious, and Processing Status is Processed, and Updated on Yesterday) IOC type = IP, Domain, Hash; Reputation = Malicious ; confidence >= 80 or Threat Score >=80.
        ```

6.  **If the Threshold of records that can be added to outbound intelligence record is met, then:**

    1.  The system automatically passes the records to the Automated Outbound Intelligence action for processing.

    2.  End the flow for this sharing of high-risk IOCs with trusted partners.

7.  **If the record count is greater than 0 then the system will process the remaining records.**

    Example:

    If the defined threshold limit is 1000 and a total of 2030 records are to be processed:

    -   Outbound Intelligence Record \#1 is created with the first 1000 records.
    -   Outbound Intelligence Record \#2 is created with the next 1000 records.
    -   Outbound Intelligence Record \#3 is created with the remaining 30 records.
    This batching process ensures the threshold limit is respected while still processing all the intelligence records efficiently.

8.  End the flow for this sharing of high-risk IOCs with trusted partners.

    ![Automated IOC Enrichment in TISC.](../image/tisc-automated-intel-share.png)


**Parent Topic:**[Working with automated flows](../concept/tisc-automated-flows.md)

**Related topics**  


[Automated IOC Enrichment](tisc-ioc-enrichment.md)

[Automatically add threat intelligence to a TAXII collection](tisc-taxii-automated-flow.md)

[Create vulnerability assessment for zero day](tisc-create-vul-assess.md)

[Analyze, assess, and disseminate observables](tisc-disseminate-observables.md)

[Analyze and assess threat IoC’s](tisc-analyze-ioc.md)

[Vulnerability Management Support](tisc-vul-mgmt.md)

[Zero-day vulnerability tracking](tisc-zero-vul.md)

[Automated flows tables](../concept/tisc-flows-tables.md)

[Automated Sharing of Outbound Intelligence Records](../concept/tisc-automated-outbound-intel-share.md)

[Sharing of Outbound Intelligence Records from GUI](../concept/tisc-create-intel-records-lib.md)

