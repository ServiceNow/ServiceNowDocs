---
title: Using the MITRE-ATT&amp;CK dashboard
description: The MITRE-ATT&amp;CK dashboard provides an executive view of the data source coverage, tactics, and techniques that are used in your organization.Use the MITRE-ATT&amp;CK dashboard to get an overview of the data source coverage, tactics, and techniques that are used in your organization.The MITRE-ATT&amp;CK Overview module consists of widgets that enable you to correlate the MITRE-ATT&amp;CK information with the security incident information in your environment.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using MITRE-ATT&amp;CK to detect and analyze threats, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Using the MITRE-ATT&amp;CK dashboard

The MITRE-ATT&amp;CK dashboard provides an executive view of the data source coverage, tactics, and techniques that are used in your organization.

The MITRE-ATT&amp;CK Overview module displays MITRE-ATT&amp;CK information about security incidents including trends and reports. You can click any part of a widget \(bar, data point, table, and so on\) to view data that is specific to that part.

![The MITRE-ATT&CK Overview module shows four widgets.](../image/mitre-overview-reports.png)

**Parent Topic:**[Using MITRE-ATT&amp;CK to detect and analyze threats](mitre-att-ck-features.md)

**Related topics**  


[Associate MITRE-ATT&amp;CK information with security incidents](../task/associate-mitre-with-sir.md#)

[Associate MITRE-ATT&amp;CK information with observables](../task/associate-mitre-observables.md)

[Associate MITRE-ATT&amp;CK information with security case](../../threat-intelligence-case-management/task/associate-mitre-att-ck-information-with-security-case-management.md)

[Rollup MITRE-ATT&amp;CK information using Threat Lookup results](../task/rollup-threat-lookup-results.md)

[Rollup MITRE-ATT&amp;CK information from detection rules](../task/rollup-mitre-attack-information-detection-rules.md)

[Rollup MITRE-ATT&amp;CK information from child security incidents](../task/rollup-mitre-att-ck-information-from-child-security-incidents.md)

[Perform link analysis and threat hunting using MITRE-ATT&amp;CK specific filters](../task/link-analysis-threat-hunt-mitre.md)

[MITRE-ATT&amp;CK heat map and navigator](mitre-att-ck-heatmap-and-navigator.md#)

## Use the MITRE-ATT&amp;CK dashboard to see your security-related data

Use the MITRE-ATT&amp;CK dashboard to get an overview of the data source coverage, tactics, and techniques that are used in your organization.

### Before you begin

Role required: sn\_si.ciso, sn\_si.analyst, sn\_si.manager, sn\_ti.read

### Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **MITRE ATT&amp;CK Repository** &gt; **Overview**.

2.  Click any of the following widgets to see additional details:

    -   Security Incidents by MITRE-ATT&amp;CK Technique
    -   Security Incidents by MITRE-ATT&amp;CK Tactic
    -   Critical Assets with MITRE-ATT&amp;CK Techniques
    -   Security Incident Close Codes Vs MITRE-ATT&amp;CK Techniques
    -   MITRE-ATT&amp;CK Techniques by Detection Coverage
    -   MITRE-ATT&amp;CK Techniques by Mitigation Coverage
    -   Threat Groups by MITRE-ATT&amp;CK Technique
    -   CVEs by MITRE-ATT&amp;CK Technique

## MITRE-ATT&amp;CK widgets

The MITRE-ATT&amp;CK Overview module consists of widgets that enable you to correlate the MITRE-ATT&amp;CK information with the security incident information in your environment.

### Example of Security Incidents by MITRE-ATT&amp;CK Technique

In this example, the **Security Incidents by MITRE ATT&amp;CK Technique** widget displays the techniques by security incident in an organization's environment in the last 90 days.

![MITRE Overview Techniques.](../image/mitre-reports-techniques.png)

### Example of Security Incidents by MITRE-ATT&amp;CK Tactic

In this example, the **Security Incidents by MITRE ATT&amp;CK Tactic** widget displays the top tactics by security incident in an organization's environment in the last 90 days.

![MITRE Overview Tactics.](../image/mitre-reports-tactics.png)

### Example of Critical Assets with MITRE-ATT&amp;CK Techniques

In this example, the **Critical Assets with MITRE ATT&amp;CK Techniques** widget displays the top 10 critical assets that are associated with the MITRE-ATT&amp;CK techniques. The assets have a business criticality of either 1 \(most critical\) or 2 \(somewhat critical\).

This report enables an organization to see the types and number of techniques that are used in carrying attacks against the critical assets.

![MITRE Overview Configuration Items.](../image/mitre-reports-cis.png)

### Example of Security Incident Close Codes Vs MITRE-ATT&amp;CK Techniques

In this example, the **Security Incident Close Codes Vs MITRE-ATT&amp;CK Techniques** widget displays the security incident close codes that were mapped against the identified top techniques in an organization's environment.

The x-axis displays the top techniques that were used to carry attacks against the enterprise, and the y-axis displays the closed codes.

![MITRE overview of closed codes versus techniques.](../image/mitre-reports-codes.png)

### Example of detection coverage by MITRE-ATT&amp;CK techniques

In this example, the **MITRE-ATT&amp;CK Techniques by Detection Coverage** widget displays the technique count by the detection coverage in your environment.

The x-axis displays the technique count, and the y-axis displays the detection coverage types.

![This illustration shows the MITRE dashboards with the detection coverage information.](../image/mitre-reports-detection.png)

### Example of mitigation coverage by MITRE-ATT&amp;CK techniques

In this example, the **MITRE-ATT&amp;CK Techniques by Mitigation Coverage** widget displays the technique count by the mitigation coverage in your environment.

The x-axis displays the technique count, and the y-axis displays the mitigation coverage types.

![This illustration shows the MITRE dashboards with the mitigation coverage information.](../image/mitre-reports-mitigation.png)

### Example of threat groups by MITRE-ATT&amp;CK techniques

In this example, the **Threat Groups by MITRE-ATT&amp;CK Technique** widget displays the techniques by the threat group count. This widget displays 20 techniques with the highest threat group count.

The x-axis displays the threat group count, and the y-axis displays the MITRE-ATT&amp;CK techniques.

![This illustration shows the MITRE dashboards with the threat group information.](../image/mitre-reports-threat.png)

### Example of CVEs by MITRE-ATT&amp;CK techniques

In this example, the **CVEs by MITRE-ATT&amp;CK Technique** widget displays the techniques with the relevant CVE count in your environment.

The x-axis displays the relevant CVE count, and the y-axis displays the MITRE-ATT&amp;CK techniques.

![This illustration shows the MITRE dashboards with the CVE information.](../image/mitre-report-cve.png)

