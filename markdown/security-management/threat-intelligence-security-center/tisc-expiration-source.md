---
title: Expiration rules for source records
description: Expiration rules are basically helpful to set the expiration time for the source records. The aggregate record inherits the highest expiration time from its corresponding sources records.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Defining Expiration Rules, About Rules Engine in TISC, Administer Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# Expiration rules for source records

Expiration rules are basically helpful to set the expiration time for the source records. The aggregate record inherits the highest expiration time from its corresponding sources records.

## How the rules are applied

## Incoming source record type is Malware from the data source type as CrowdStrike

**Rule evaluation process based on the rules provided for applying expiration times to source records:**

1.  **Fetch all the enabled rules:** The application starts by verifying all the rules that are currently enabled.
2.  Check for specific rule combination:

    Look for a rule that specifically matches the combination of:

    -   **Data Source type**: CrowdStrike
    -   **Type of Records**: Malware
3.  **Priority based on the matching rule combinations:**

    If there exists a rule where the data source type is **CrowdStrike** and the record type is **Malware**, this rule takes the precedence. The expiration time specified in this rule will be applied.

4.  **Fallback rules:**
    1.  If no rule matches the **CrowdStrike and Malware** combination, then the system checks for a rule where the data source type is **CrowdStrike** and the record type is **All**.
    2.  If still no rule is found, it then looks for a rule where the data source type is **All** and the record type is **Malware**.
    3.  Finally, if none of the above rules exist, it defaults to a rule where both data source type and record type are **All**.
5.  If none of these rules exist in the system, then no expiration rule will be applied to the source records. In that case, navigate to the below table \(shown in the screenshot\) to check the combination of rules that were applied to the objects.

    ![Expiration Rules for Source Records.](../image/tisc-config-expiration-rule.png)

6.  **Deletion of data sources:**

    Suppose, if a data source that has the expiration rules associated with it is deleted, then the deletion may be restricted or not allowed until these rules are addressed. This ensures that there are no inconsistencies in the application of expiration policies.


**Parent Topic:**[Defining Expiration Rules](../task/tisc-expiration-rules.md)

