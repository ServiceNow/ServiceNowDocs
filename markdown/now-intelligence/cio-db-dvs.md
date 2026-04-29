---
title: Chief Information Officer Dashboard data visualizations
description: Use these data visualizations to get high-level and detailed views of how information is used in your organization.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Chief Information Officer \(CIO\) Dashboard, Executive dashboard overview, Platform Analytics]
---

# Chief Information Officer Dashboard data visualizations

Use these data visualizations to get high-level and detailed views of how information is used in your organization.

## Overview tab

For more information about indicator data sources, see [Chief Information Officer Dashboard indicators](cio-db-indicators.md).

|Column|Visualization|Visualization Type|Data Source|
|------|-------------|------------------|-----------|
|Value|Total combined value YTD|Single score|Formula indicator: Total Value YTD|
|Value|Value components YTD|Vertical bar|Formula indicator: Total Value YTD|
|Operations|% breached SLA|Single score|Formula indicator: % open and overdue incident assignments|
|Operations|Cloud health score|Single score|Automated indicator: CMDB Health Scorecard|
|Operations|CMDB health score by health metric|Line|Automated indicator: CMDB Health Scorecard|
|Operations|% SLA by priority|Donut|Formula indicator: % incidents resolved in time|
|Security|New security issues|Single score|Automated indicator: Number of new security incidents|
|Security|Active P1s|Single score|Automated indicator: SI - Incident Priority 1|
|Security|Total issues by priority|Vertical bar|Automated indicator: Number of open security incidents|
|Security|P1 issues trend|Line|Automated indicator: SI - Incident Priority 1|
|Execution|Active projects|Single score|Automated indicator: PPM - Number of Active Projects|
|Execution|Active projects in red|Single score|Automated indicator: PPM - Number of Active Red Projects|
|Execution|Projects in red by portfolio|Vertical bar|Automated indicator: PPM - Number of Active Red Projects|
|Execution|Projects by state|Donut|Automated indicator: PPM - Number of Active Projects|
|Experience|eSAT|Single score|Automated indicator: eSAT monthly|
|Experience|Self-Service: Success Rate|Single score|Formula indicator: Self-Service: Success Rate|
|Experience|Self-Service: Success Rate trend|Line|Formula indicator: Self-Service: Success Rate|
|Experience|eSAT trend|Line|Automated indicator: eSAT monthly|

## Value tab

|Column|Visualization|Visualization Type|Data Source|
|------|-------------|------------------|-----------|
|Revenue|Pipeline closed|Single score|Manual indicator: Revenue impact|
|Revenue|Pipeline by portfolio|Vertical bar|Manual indicator: Revenue impact|
|Cost Impact|Total cost|Single score|Manual indicator: Cost impact|
|Cost Impact|Cost by portfolio|Vertical bar|Manual indicator: Cost impact|

## Operations tab

|Column|Visualization|Visualization Type|Data Source|
|------|-------------|------------------|-----------|
|Incident Management|Mean time to resolve|Single score|Formula indicator: Average close time of incidents|
|Incident Management|% breached SLA|Single score|Formula indicator: % open and overdue incident assignments|
|Incident Management|Open incidents by age|Vertical bar|Automated indicator: Number of open incidents|
|Incident Management|% SLA trend by priority|Line|Formula indicator: % incidents resolved in time|
|Request Management|Requests backlog growth|Single score|Formula indicator: Requests backlog growth|
|Request Management|Open requests|Single score|Automated indicator: Number of open requests|
|Request Management|Requests by priority|Horizontal bar|Automated indicator: Number of open requests|
|Request Management|Avg time to close requests|Line|Formula indicator: Average close time of requests|
|Change Management|% Urgent changes|Single score|Formula indicator: % of urgent changes|
|Change Management|% of Unsuccessful changes|Single score|Formula indicator: % unsuccessful changes|
|Change Management|Average age of open changes by priority|Vertical bar|Formula indicator: Average age of open changes|
|Change Management|Change backlog growth|Line|Formula indicator: Change backlog growth|
|CMDB|Count of CIs monitored|Single score|Automated indicator: Number of Monitored Configuration Items|
|CMDB|Avg CIs fault count|Single score|Automated indicator: Avg CIs Fault count|
|CMDB|CMDB health results|Vertical bar|Automated indicator: CMDB health results|
|CMDB|CMDB health scorecard|Vertical bar|Automated indicator: CMDB Health Scorecard|
|Asset Management|Potential savings|Single score|Automated indicator: Potential Savings|
|Asset Management|Percent spend not in use|Single score|Formula indicator: Percent Spend Not in Use|
|Asset Management|Percent spend not in use - by product|Vertical bar|Formula indicator: Percent Spend Not in Use|
|Asset Management|Potential savings - by product|Vertical bar|Automated indicator: Potential savings|

## Security tab

|Column|Visualization|Visualization Type|Data Source|
|------|-------------|------------------|-----------|
|Security Incident Response|Active P1s|Single score|Automated indicator: SI - Incident Priority 1|
|Security Incident Response|Open Issues By Age|Vertical bar|Automated indicator: Number of open security incidents|
|Security Incident Response|P1 trend|Line|Automated indicator: SI - Incident Priority 1|
|Vulnerability Management|Avg vulnerability age|Single score|Formula indicator: Average Age of Vulnerable Items|
|Vulnerability Management|P1 vulnerabilities|Single score|Automated indicator: Critical Vulnerable Items|
|Vulnerability Management|Vulnerabilities by age|Vertical bar|Automated indicator: Unassigned Vulnerable Items|
|Vulnerability Management|P1 vulnerabilities trend|Line|Automated indicator: Critical Vulnerable Items|
|Security Patching|Vuln deferred|Single score|Automated indicator: Deferred Vulnerable Items|
|Security Patching|Vuln patching SLA attainment|Single score|Formula indicator: Vulnerable Items Mean Time to Remediate|
|Security Patching|Closed vuln which met target|Vertical bar|Automated indicator: Closed Vulnerable Items \(Target Met\)|
|Security Patching|Deferred Vulnerable Items by Reason|Donut|Automated indicator: Deferred Vulnerable Items|
|Compliance|Compliance score|Single score|Automated indicator: Policy Compliance Score Percentage|
|Compliance|\# of failed controls|Single score|Automated indicator: \# of Failed Control Indicators|
|Compliance|Citation compliance score percentage|Donut|Automated indicator: Citation compliance score percentage|
|Compliance|Policy compliance score percentage|Vertical bar|Automated indicator: Policy Compliance Score Percentage|

## Execution tab

|Column|Visualization|Visualization Type|Data Source|
|------|-------------|------------------|-----------|
|Innovation Management|Average age of open ideas|Single score|Formula indicator: PPM:Average Age of Open Ideas|
|Innovation Management|% of ideas converted|Single score|Formula indicator: PPM:% of Ideas Converted|
|Innovation Management|Converted ideas by categories|Line|Automated indicator: PPM:Ideas Converted|
|Innovation Management|Open ideas by state|Vertical bar|Automated indicator: PPM:Open Ideas|
|Demand Management|Average age open demand|Single score|Formula indicator: PPM:Average Age of Open Ideas|
|Demand Management|% of Demands to Projects last 12 months|Single score|PPM - Percentage of Demand to Project Last 12 months|
|Demand Management|Open Demands by state|Donut|Automated indicator: PPM - Open Demands Submitted, Screening, Qualified or Approved|
|Demand Management|Converted Demands trend|Line|Automated indicator: PPM - Number of Demands With Projects This Month|
|Project Portfolio Management|Total Projects|Single score|Automated indicator: PPM - Number of Active Projects|
|Project Portfolio Management|Projects with critical issues|Single score|Automated indicator: PPM - Number of Projects With Critical Issues|
|Project Portfolio Management|Projects by portfolio|Vertical bar|Automated indicator: PPM - Number of Active Projects|
|Project Portfolio Management|Projects by investment class|Donut|Automated indicator: PPM - Number of Active Projects|
|Resource Management|Total Allocated|Single score|Automated indicator: Total Allocated hrs|
|Resource Management|Total Availability|Single score|Automated indicator: Total available hrs|
|Resource Management|Allocated quarterly trend|Line|Formula indicator: Total allocated hours quarterly|
|Resource Management|Availability quarterly trend|Line|Formula indicator: Total available hours quarterly|
|Cost Management|Planned cost|Single score|Automated indicator: PPM - Planned Cost|
|Cost Management|Actual cost|Single score|Automated indicator: PPM - Actual Cost|
|Cost Management|Variance by portfolio|Vertical bar|Formula indicator: Variance by portfolio|

## Experience tab

|Column|Visualization|Visualization Type|Data Source|
|------|-------------|------------------|-----------|
|Self-Service|Self-Service: Success Rate|Single score|Formula indicator: Self-Service: Success Rate|
|Self-Service|Self-Service: Engagements|Single score|Formula indicator: Self-Service: Engagements|
|Self-Service|Self-Service: Success Rate trend|Area|Formula indicator: Self-Service: Success Rate|
|Self-Service|Self-Service: Engagement trend|Area|Formula indicator: Self-Service: Engagements|
|Survey Management|eSAT score|Single score|Automated indicator: eSAT monthly|
|Survey Management|cSAT monthly|Single score|Automated indicator: cSAT monthly|
|Survey Management|eSAT monthly trend|Area|Automated indicator: eSAT monthly|
|Survey Management|cSAT monthly trend|Area|Automated indicator: cSAT monthly|

