---
title: Security Operations Efficiency dashboard
description: Security operations center \(SOC\) managers can view overall efficiency metrics and measure the individual performance of the SOC team members in the organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/cj-sir-socpa-dashboard.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Security Incident Response Platform Analytics Solutions, Security Incident Response setup, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Operations Efficiency dashboard

Security operations center \(SOC\) managers can view overall efficiency metrics and measure the individual performance of the SOC team members in the organization.

The SOC manager can use the Performance Analytics dashboard to improve efficiency and develop a picture of how SOC is performing in both general and specific areas over time.

## Analyst Efficiency tab

\[Omitted image "cj-sir-soc-analyst.png"\] Alt text: Performance Analytics SOC Efficiency dashboard: Analyst Efficiency tab

Select any of the indicators to drill down for further details. For example, select the indicator in the Average security incidents worked per analyst section.

|Indicator|Description|
|---------|-----------|
|Average security incidents worked per analyst|Average number of open security incidents per analyst for the specified period. The formula used is `[[Number of open security incidents / By month AVG +]]/[[Number of Security Agents]]`|
|Closed security incidents per analyst|The total number of incidents closed by each analyst in the selected category in the specified period. The formula used is `[Number of closed security incidents > Security Incident Category = <category_name> / By month SUM +]]/[[Number of Security Agents / By month AVG +]]`|
|Average security incident resolution|The average time taken by each analyst to close security incidents in the specified period. The formula used to show the result in days is `([[Summed duration of closed security incidents > Security Incident Category = <category_name> / By month AVG +]] / [[Number of closed security incidents > Security Incident Category = <category_name> / By month AVG +]]) / 24`|
|Average security incident age|The average number of days for which security incidents remain open for each analyst. The formula used to show the result in days is `([[Summed age of open security incidents > Security Incident Category = <category_name> / By month AVG +]]/ [[Number of open security incidents > Security Incident Category = <category_name> / By month AVG +]]) / 24`|
|Security incident backlog analysis|The total number of open security incidents in the specified period. Select an option from the Breakdown list to view the backlog for each analyst, security group, priority, and so on. You can also compare the number of open security incidents between two selected months.|
|Closed security incident analysis|The total number of security incidents that are closed in the specified period. Select an option from the Breakdown list to view the count for each analyst, security group, priority, and so on. You can also compare the number of security incidents that were closed between two selected months.|
|Security incident age|The average number of days for security incidents remain open in the specified period. Select an option from the Breakdown list to view the security incident age for each analyst, security group, priority, and so on. The formula used to show the result in days is `([[Summed age of open security incidents > Security Incident Category = <category_name> > Security Assignment Group = <group_name> / By month AVG +]]/ [[Number of open security incidents > Security Incident Category = <category_name> > Security Assignment Group = <group_name> / By month AVG +]]) / 24`|
|Security incident resolution time|The average number of days taken to resolve security incidents during the specified period. Select an option from the Breakdown list to view the security incident resolution time for each analyst, security group, priority, and so on. The formula used to show the result in days is `([[Summed duration of closed security incidents > Security Incident Category = Malicious code activity > Security Assigned To = John Ashby / By month AVG +]] / [[Number of closed security incidents > Security Incident Category = Malicious code activity > Security Assigned To = John Ashby / By month AVG +]]) / 24`|

## Detection and Response Effectiveness tab

<table id="table_hr2_cbs_vhb"><thead><tr><th>

Indicator

</th><th>

Description

</th></tr></thead><tbody><tr><td>

True positive incidents

</td><td>

Percentage of true positive security incidents in the selected category for the specified period. The formula used is `(1-([[Number of false positive security incidents > Security Incident Category = Malicious code activity / By month SUM +]] / [[Number of closed security incidents > Security Incident Category = Malicious code activity / By month SUM +]])) * 100`

</td></tr><tr><td>

False positive critical incidents

</td><td>

Percentage of false positive critical security incidents in the selected category for the specified period. The formula used is `([[Number of false positive security incidents > Security Incident Risk Score = Critical Risk > Security Incident Category = Malicious code activity / By month SUM +]] / [[Number of closed security incidents > Security Incident Category = Malicious code activity / By month SUM +]]) * 100` **Note:** Any security incident where the `Closed code = Invalid vulnerability or False positive` is treated as a false positive incident

</td></tr><tr><td>

Mean false positive risk score

</td><td>

Average monthly risk score of closed security incidents that were identified as false positive incidents. A lower risk score indicates that the security analysts spent lesser time analyzing false positive incidents. The formula used is `([[Number of false positive security incidents > Security Incident Risk Score = Critical Risk > Security Incident Category = Malicious code activity / By month SUM +]] / [[Number of closed security incidents > Security Incident Category = Malicious code activity / By month SUM +]]) * 100`

</td></tr><tr><td>

False positive security incident duration

</td><td>

Average number of days that the security analysts spent in investigating false positive incidents. The formula used is `([[Summed duration of false positive security incidents]] / [[Number of false positive security incidents]]) / 24`

</td></tr><tr><td>

Security incident source effectiveness

</td><td>

Percentage of true positive security incidents identified by a specific source for the specified period. The source can be email, network activity,customer support, and so on. This data helps measure the effectiveness of the security incident source. The formula used is `(1-([[Number of false positive security incidents > Security Incident Category = Malicious code activity > Security Incident Source = IDS/IPS / By month SUM +]] / [[Number of closed security incidents > Security Incident Category = Malicious code activity > Security Incident Source = IDS/IPS / By month SUM +]])) * 100`

</td></tr><tr><td>

Security incident source volume analysis

</td><td>

Number of closed security incidents for current month for each Security incident source. You can also compare the number of security incidents for each source type between two selected months.

</td></tr><tr><td>

Security incident backlog analysis

</td><td>

The total number of open security incidents in the specified period and the average number of days for which the incidents remain open. You can also compare the number of open security incidents between two selected months. The formula used to calculate the average backlog period is `([[Summed age of open security incidents > Security Incident Category = Malicious code activity]]/ [[Number of open security incidents > Security Incident Category = Malicious code activity]]) / 24`

</td></tr><tr><td>

Closed security incident analysis

</td><td>

The total number of closed security incidents in the specified period and the average resolution time for these incidents. The formula used to calculate the average resolution time is `([[Summed duration of closed security incidents > Security Incident Category = Malicious code activity]] / [[Number of closed security incidents > Security Incident Category = Malicious code activity]]) / 24`

</td></tr></tbody>
</table>## Incident Risk Score Analysis tab

|Indicator|Description|
|---------|-----------|
|Total risk exposure analysis|Total number of open incidents in each risk category \(low, moderate, and critical\) in the specified period. You can also compare the number of incidents in the different risk categories between two months.|
|Normalized security analyst work by risk score|The total risk score for each security analyst for the specified period. This is calculated based on the number of true positive security incidents that the security analyst closed. The formula used is `[[Summed Risk Score of Closed Security Incidents > Security Incident Category = Malicious code activity > Security Assigned To = SI Admin / By month SUM +]] - [[Summed Risk Score of False Positive Security Incidents > Security Incident Category = Malicious code activity > Security Assigned To = SI Admin / By month SUM +]]`|
|Security analyst work by mean risk score|The average risk score for each security analyst for the specified period. The formula used is `[[Summed Risk Score of Closed Security Incidents > Security Incident Category = Malicious code activity > Security Assigned To = SI Admin / By month AVG +]] - [[Summed Risk Score of False Positive Security Incidents > Security Incident Category = Malicious code activity > Security Assigned To = SI Admin / By month AVG +]]`|

## Security Incident Stage Analysis tab

You can see the number of open incidents on a specific day and the status \(analysis, draft, contain, eradicate, recover, or review\) of these incidents. On each stage, you can view average age, affected CIs, response tasks, and so on. Select a link to view additional details or the breakdown of these incidents.

**Parent Topic:**[Security Incident Response Platform Analytics Solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/security-incident-content-pack.md)

**Related topics**  


[CISO dashboard]()

[Security Incident Management Premium dashboard]()

[Security Incident Management dashboard]()

[Security Incident Explorer dashboard]()

