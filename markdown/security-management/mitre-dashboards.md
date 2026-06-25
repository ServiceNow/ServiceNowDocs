---
title: Using the MITRE-ATT&amp;CK dashboard
description: The MITRE-ATT&amp;CK dashboard provides an executive view of the data source coverage, tactics, and techniques that are used in your organization.Use the MITRE-ATT&amp;CK dashboard to get an overview of the data source coverage, tactics, and techniques that are used in your organization.The MITRE-ATT&amp;CK Overview module consists of widgets that enable you to correlate the MITRE-ATT&amp;CK information with the security incident information in your environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/mitre-dashboards.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using MITRE-ATT&amp;CK to detect and analyze threats, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Using the MITRE-ATT&amp;CK dashboard

The MITRE-ATT&amp;CK dashboard provides an executive view of the data source coverage, tactics, and techniques that are used in your organization.

The MITRE-ATT&amp;CK Overview module displays MITRE-ATT&amp;CK information about security incidents including trends and reports. You can click any part of a widget \(bar, data point, table, and so on\) to view data that is specific to that part.

\[Omitted image "mitre-overview-reports.png"\] Alt text: The MITRE-ATT&amp;CK Overview module shows four widgets.

**Parent Topic:**[Using MITRE-ATT&amp;CK to detect and analyze threats](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/mitre-att-ck-features.md)

**Related topics**  


[Associate MITRE-ATT&amp;CK information with security incidents]()

[Associate MITRE-ATT&amp;CK information with observables]()

[Associate MITRE-ATT&amp;CK information with security case]()

[Rollup MITRE-ATT&amp;CK information using Threat Lookup results]()

[Rollup MITRE-ATT&amp;CK information from detection rules]()

[Rollup MITRE-ATT&amp;CK information from child security incidents]()

[Perform link analysis and threat hunting using MITRE-ATT&amp;CK specific filters]()

[MITRE-ATT&amp;CK heat map and navigator]()

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

\[Omitted image "mitre-reports-techniques.png"\] Alt text: MITRE Overview Techniques.

### Example of Security Incidents by MITRE-ATT&amp;CK Tactic

In this example, the **Security Incidents by MITRE ATT&amp;CK Tactic** widget displays the top tactics by security incident in an organization's environment in the last 90 days.

\[Omitted image "mitre-reports-tactics.png"\] Alt text: MITRE Overview Tactics.

### Example of Critical Assets with MITRE-ATT&amp;CK Techniques

In this example, the **Critical Assets with MITRE ATT&amp;CK Techniques** widget displays the top 10 critical assets that are associated with the MITRE-ATT&amp;CK techniques. The assets have a business criticality of either 1 \(most critical\) or 2 \(somewhat critical\).

This report enables an organization to see the types and number of techniques that are used in carrying attacks against the critical assets.

\[Omitted image "mitre-reports-cis.png"\] Alt text: MITRE Overview Configuration Items.

### Example of Security Incident Close Codes Vs MITRE-ATT&amp;CK Techniques

In this example, the **Security Incident Close Codes Vs MITRE-ATT&amp;CK Techniques** widget displays the security incident close codes that were mapped against the identified top techniques in an organization's environment.

The x-axis displays the top techniques that were used to carry attacks against the enterprise, and the y-axis displays the closed codes.

\[Omitted image "mitre-reports-codes.png"\] Alt text: MITRE overview of closed codes versus techniques.

### Example of detection coverage by MITRE-ATT&amp;CK techniques

In this example, the **MITRE-ATT&amp;CK Techniques by Detection Coverage** widget displays the technique count by the detection coverage in your environment.

The x-axis displays the technique count, and the y-axis displays the detection coverage types.

\[Omitted image "mitre-reports-detection.png"\] Alt text: This illustration shows the MITRE dashboards with the detection coverage information.

### Example of mitigation coverage by MITRE-ATT&amp;CK techniques

In this example, the **MITRE-ATT&amp;CK Techniques by Mitigation Coverage** widget displays the technique count by the mitigation coverage in your environment.

The x-axis displays the technique count, and the y-axis displays the mitigation coverage types.

\[Omitted image "mitre-reports-mitigation.png"\] Alt text: This illustration shows the MITRE dashboards with the mitigation coverage information.

### Example of threat groups by MITRE-ATT&amp;CK techniques

In this example, the **Threat Groups by MITRE-ATT&amp;CK Technique** widget displays the techniques by the threat group count. This widget displays 20 techniques with the highest threat group count.

The x-axis displays the threat group count, and the y-axis displays the MITRE-ATT&amp;CK techniques.

\[Omitted image "mitre-reports-threat.png"\] Alt text: This illustration shows the MITRE dashboards with the threat group information.

### Example of CVEs by MITRE-ATT&amp;CK techniques

In this example, the **CVEs by MITRE-ATT&amp;CK Technique** widget displays the techniques with the relevant CVE count in your environment.

The x-axis displays the relevant CVE count, and the y-axis displays the MITRE-ATT&amp;CK techniques.

\[Omitted image "mitre-report-cve.png"\] Alt text: This illustration shows the MITRE dashboards with the CVE information.

