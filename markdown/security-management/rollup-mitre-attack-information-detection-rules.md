---
title: Rollup MITRE-ATT&amp;CK information from detection rules
description: Enable rollup of MITRE-ATT&amp;CK information from the detection rules to the security incidents for better security incident and threat analysis.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using MITRE-ATT&amp;CK to detect and analyze threats, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Rollup MITRE-ATT&amp;CK information from detection rules

Enable rollup of MITRE-ATT&amp;CK information from the detection rules to the security incidents for better security incident and threat analysis.

## Before you begin

Role required: none.

Ensure that you have performed the following:

-   Enable the Rollup MITRE ATT&amp;ACK information automatically from alert rules to security incidents property in the Properties module. By default, this option is disabled. For more information, see [Review the MITRE-ATT&amp;CK system properties](configure-mitre-att-ck-properties.md).
-   Perform mapping of detection rules to MITRE-ATT&amp;CK TTPs in Detection Rules - MITRE ATT&amp;CK TTP Mapping module. The detection rule name must match the alert rule name that triggers the security incident. For more information, see [Create and map detection rules](create-detection-rules.md).

## About this task

If you do not intend to use the base system SIEM auto-extraction rules, then enable the automatic rollup of MITRE-ATT&amp;CK TTPs based on the detection rule mapping. You can populate the alert or event rule that triggers the security incident in the Alert Rule name field. You can also populate the Alert Rule name field by using SIEM integration, email parsing, manual creation, and so on.

## Procedure

1.  Navigate to **MITRE ATT&amp;CK Administration** &gt; **Properties**.

2.  Enable the Rollup MITRE ATT&amp;ACK information automatically from alert rules to security incidents property, and click **Save**.

    By default, this option is disabled.

3.  You need to populate the **Alert Rule** name field of the security incident with the required alert rules.

    **Note:** Ensure that you add the exact Alert Rule name. To add multiple rules, you need to add the rules using a comma separator.

4.  Right-click the form, and click **Save**.

    If the alert rule name value in the security incident matches a record in the Detection rule - MITRE ATT&amp;CK TTP Mapping module, the corresponding techniques and tactics associated to the alert rule are linked to the security incident automatically.

    ![This illustration shows how to roll up MITRE information from the detection rules to a security incident.](../image/mitre-rollup-detection-rule.gif)

5.  Open the security incident, select the **MITRE ATT&amp;CK Card** and validate whether the techniques are rolled up.

6.  Enable **Show origin of techniques** option to view the origin of the techniques.

    The origin of techniques should be Detection Rule.


**Parent Topic:**[Using MITRE-ATT&amp;CK to detect and analyze threats](../concept/mitre-att-ck-features.md)

**Related topics**  


[Associate MITRE-ATT&amp;CK information with security incidents](associate-mitre-with-sir.md#)

[Associate MITRE-ATT&amp;CK information with observables](associate-mitre-observables.md)

[Associate MITRE-ATT&amp;CK information with security case](../../threat-intelligence-case-management/task/associate-mitre-att-ck-information-with-security-case-management.md)

[Rollup MITRE-ATT&amp;CK information using Threat Lookup results](rollup-threat-lookup-results.md)

[Rollup MITRE-ATT&amp;CK information from child security incidents](rollup-mitre-att-ck-information-from-child-security-incidents.md)

[Perform link analysis and threat hunting using MITRE-ATT&amp;CK specific filters](link-analysis-threat-hunt-mitre.md)

[MITRE-ATT&amp;CK heat map and navigator](../concept/mitre-att-ck-heatmap-and-navigator.md#)

[Using the MITRE-ATT&amp;CK dashboard](../concept/mitre-dashboards.md#)

