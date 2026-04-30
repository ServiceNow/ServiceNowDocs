---
title: Perform link analysis and threat hunting using MITRE-ATT&amp;CK specific filters
description: Correlate and perform link analysis of observables, security incidents, and MITRE-ATT&amp;CK related information so that your organization can start hunting for threats.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using MITRE-ATT&amp;CK to detect and analyze threats, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Perform link analysis and threat hunting using MITRE-ATT&amp;CK specific filters

Correlate and perform link analysis of observables, security incidents, and MITRE-ATT&amp;CK related information so that your organization can start hunting for threats.

## Before you begin

Role required: sn\_ti.mitre\_analyst, sn\_si.read

## About this task

After you associate the security incidents with MITRE-ATT&amp;CK information, you can use the MITRE-ATT&amp;CK specific filters for threat hunting. Use the MITRE-ATT&amp;CK filters with the existing Security Incident Response filters to correlate and perform link analysis.

## Procedure

1.  Navigate to **All** &gt; **Security Incidents** &gt; **Show All Incidents**.

2.  Click **Update Personalized List** to add the MITRE columns.

3.  Select a filter condition so that you can view MITRE related information and associations with security incidents or observables:

    -   MITRE-ATT&amp;CK Adversary Group
    -   MITRE-ATT&amp;CK Data Source
    -   MITRE-ATT&amp;CK Procedure \(Malware\)
    -   MITRE-ATT&amp;CK Procedure \(Tools\)
    -   MITRE-ATT&amp;CK Tactic
    -   MITRE-ATT&amp;CK Technique
4.  Create a filter condition that is based on the above criteria and click **Run** to perform a link analysis or correlation between security incidents, observables, and MITRE-ATT&amp;CK related information.

    **Note:** The MITRE-ATT&amp;CK data is stored as a string and you can only use **contains** as the operator for filter conditions.

    For example, if you want to review that a configuration item \(CI\) is compromised, you select a CI. You then correlate the CI with techniques that are present by adding a MITRE-ATT&amp;CK Technique ID. You can then continue to build your filter criteria to correlate the information and for threat hunting.

    ![MITRE filter conditions for threat analysis.](../image/mitre-filter-conditions.png)


**Parent Topic:**[Using MITRE-ATT&amp;CK to detect and analyze threats](../concept/mitre-att-ck-features.md)

**Related topics**  


[Associate MITRE-ATT&amp;CK information with security incidents](associate-mitre-with-sir.md#)

[Associate MITRE-ATT&amp;CK information with observables](associate-mitre-observables.md)

[Associate MITRE-ATT&amp;CK information with security case](../../threat-intelligence-case-management/task/associate-mitre-att-ck-information-with-security-case-management.md)

[Rollup MITRE-ATT&amp;CK information using Threat Lookup results](rollup-threat-lookup-results.md)

[Rollup MITRE-ATT&amp;CK information from detection rules](rollup-mitre-attack-information-detection-rules.md)

[Rollup MITRE-ATT&amp;CK information from child security incidents](rollup-mitre-att-ck-information-from-child-security-incidents.md)

[MITRE-ATT&amp;CK heat map and navigator](../concept/mitre-att-ck-heatmap-and-navigator.md#)

[Using the MITRE-ATT&amp;CK dashboard](../concept/mitre-dashboards.md#)

