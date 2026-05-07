---
title: Automatically add threat intelligence to a TAXII collection
description: Learn how to automatically add threat intelligence to a TAXII server collection.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with automated flows, Administer, Threat Intelligence Security Center, Security Operations]
---

# Automatically add threat intelligence to a TAXII collection

Learn how to automatically add threat intelligence to a TAXII server collection.

## Before you begin

Role required:

-   System Administrator \(view, create or edit\)
-   sn\_sec\_tisc.admin \(view\)

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence Security Center** &gt; **Administration**.

2.  Select **Automated Flows**.

3.  Select **Automatically add threat intelligence to a TAXII collection** action link to view the respective rule details in the flow designer.

4.  View the flow designer action for the following triggers:

    ```
    Observable Created or Updated where (Type is IP address (V4), or Type is IP address (V6), or Type is Domain Name; and TISC Tags contains Add to: Sample Collection, and Reputation is Malicious, and Threat Score greater than or is 60
    ```

5.  **Actions**

    Adds the record provided in the inputs to TAXII server collections configured in the selected template

    1.  **Add Record to TAXII Server Collection**

    2.  **Add Records to TAXII Server Collection**

6.  End the flow for adding threat intelligence to a TAXII collection.

    ![Automated TAXII server collection.](../image/tisc-taxii-collections-flow.png)


**Parent Topic:**[Working with automated flows](../concept/tisc-automated-flows.md)

**Related topics**  


[Automated IOC Enrichment](tisc-ioc-enrichment.md)

[Automated sharing of high-risk IOC's with trusted partners](tisc-automated-sharing-flow.md)

[Create vulnerability assessment for zero day](tisc-create-vul-assess.md)

[Analyze, assess, and disseminate observables](tisc-disseminate-observables.md)

[Analyze and assess threat IoC’s](tisc-analyze-ioc.md)

[Vulnerability Management Support](tisc-vul-mgmt.md)

[Zero-day vulnerability tracking](tisc-zero-vul.md)

[Automated flows tables](../concept/tisc-flows-tables.md)

