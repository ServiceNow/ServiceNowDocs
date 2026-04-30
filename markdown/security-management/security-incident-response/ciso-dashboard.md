---
title: CISO dashboard
description: This dashboard reveals the overall security posture of your organization, including security vulnerability and incidents.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Security Incident Response Platform Analytics Solutions, Security Incident Response setup, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# CISO dashboard

This dashboard reveals the overall security posture of your organization, including security vulnerability and incidents.

![Partial view of the Security Operations Center tab of the CISO dashboard](../../../product/security-incident-response/image/ciso-dashboard.png "Security Operations Center tab")

![The Vulnerability Profile tab of the CISO dashboard](../../../product/security-incident-response/image/ciso-dashboard-vulnerability.png "Vulnerability Profile tab")

![The Security Controls Profile tab of the CISO dshboard with compliance metrics](../../../product/security-incident-response/image/ciso-dashboard-sec-controls.png "Security Controls Profile tab")

![The Business Risk Profile tab showing risks by category](../../../product/security-incident-response/image/ciso-dashboard-business-risk.png "Business Risk Profile tab")

## End users and roles

|End user and goal|Required role|
|-----------------|-------------|
|CISO: Needs clear visibility regarding the current security posture of the overall organization|sn\_si.ciso|

## CISO dashboard indicators

The CISO dashboard presents the following key performance indicators:

-   **SI - Average Time to Identify**

    A 7-day average of the time in minutes it takes to identify a security incident, calculated daily.

-   **Average Time to Contain**

    A 7-day average of the time in minutes it takes to contain a security incident, calculated daily.

-   **Average Time to Eradicate**

    A 7-day average of the time in minutes it takes to eradicate a security incident, calculated daily. Both Average Time to Contain and Average Time to Eradicate are based on the indicator SI - Average Duration Time broken down by Security Incident State.

-   **New Security Incidents This Week**

    The weekly sum of the score of the daily Number of new security incidents indicator.

-   **Security Incidents Closed \(weekly\)**

    The 7-day running sum of the daily Number of closed security incidents indicator.

-   **New Security Incidents by Priority**

    Daily breakdown of the Number of new security incidents indicator by Priority.

-   **New vs Closed Security Incidents \(weekly\) volume**

    The 7-day running sum time series of the Number of new incidents indicator charted against the 7-day running sum time series of the Number of closed incidents indicator.

-   **Security Incident Heatmap**

    A global map showing the number of open security incidents in each country.

-   **Security Incident Treemap**

    An interactive treemap where you can select to see:

    -   Security incidents per business service, broken down by business criticality
    -   Security incidents broken down by category or subcategory of incident
    -   Security incidents per assignment group or per assignee
    -   'Victim stats' of security incident per affected resource or affected user

## Breakdowns

The following breakdowns apply to the indicators on the dashboard:

-   Business criticality
-   Security Group
-   Security Incident Age
-   Security Incident Category
-   Security Incident Close Code
-   Security Incident Priority
-   Security Incident State
-   SI - Business Service
-   Vulnerability

## Data visualizations

The dashboard includes the following visualizations:

|Title|Type|Description|
|-----|----|-----------|
|Security Incidents Open for More Than 30 Days by Assignment Group and State|Heatmap ![Heatmap icon](../../performance-analytics/image/heatmap.png)|Displays models with the most vulnerable items.|
|Risks by Category|Donut ![Donut icon](../../performance-analytics/image/donut-icon.png)|Lists the age of reopened vulnerable items.|
|Citations by Authority Document|Donut ![Donut icon](../../performance-analytics/image/donut-icon.png)|Number of active vulnerabilities|
|Security Incidents With Assignee That is not Active|Heatmap ![Heatmap icon](../../performance-analytics/image/heatmap.png)|Displays the number of open vulnerable items associated with vulnerabilities, \(Common Vulnerability Enumeration \(CVE\) records\), from most to least.|
|Security Incidents Not Updated for More Than 30 Days by Assignment Group and State|Heatmap ![Heatmap icon](../../performance-analytics/image/heatmap.png)|Displays publishers with the most vulnerable items.|
|Vulnerability Map|Map ![Map icon](../../performance-analytics/image/map-icon.png)|A world map showing vulnerabilities by location|
|Most Vulnerable Models|Donut ![Donut icon](../../performance-analytics/image/donut-icon.png)|The applications that contain the most vulnerabilities|
|Most Vulnerable CIs by Class|Donut ![Donut icon](../../performance-analytics/image/donut-icon.png)|CIs by server type|
|Services with Critically Significant Vulnerabilities|List ![List icon3](../../performance-analytics/image/scorecard-icon.png)| |
|Non-compliant profiles|Bar ![Bar icon](../../performance-analytics/image/column-icon.png)|Non-compliant controls by profile|
|Control Overview|Bar ![Bar icon](../../performance-analytics/image/column-icon.png)|Number of compliant and non-compliant controls|
|Policy Exceptions|List ![List icon3](../../performance-analytics/image/scorecard-icon.png)|Policy exceptions with priority, owner, and short description|
|Risks by Category|Donut ![Donut icon](../../performance-analytics/image/donut-icon.png)|The number of risks in each category of risk|
|Inherent Risk|Bubble ![Bubble icon](../../performance-analytics/image/bubble-icon.png)|Inherent SLE vs Inherent ARO|
|Residual Risk|Bubble ![Bubble icon](../../performance-analytics/image/bubble-icon.png)|Residual SLE vs Residual ARO|
|Moderate, High, and Very High Risks|Scores![Latest score icon](../../performance-analytics/image/latest-score-icon.png)|The numbers of moderate, high, and very high risks, respectively|
|Risk by Profile|Stacked Bar![Stacked bar icon](../../performance-analytics/image/stacked-column-bkdown-icon.png)|Risk count where you can select what to group by and what to stack by|

**Parent Topic:**[Security Incident Response Platform Analytics Solutions](security-incident-content-pack.md)

**Related topics**  


[Security Incident Management Premium dashboard](si-mgmt-premium-dashboard.md)

[Security Incident Management dashboard](security-incident-mgmt-dashboard.md)

[Security Incident Explorer dashboard](si-explorer-dashboard.md)

[Security Operations Efficiency dashboard](../../../product/security-incident-response/concept/cj-sir-socpa-dashboard.md)

