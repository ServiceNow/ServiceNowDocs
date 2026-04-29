---
title: Chief Information Officer Dashboard indicators
description: Indicators provide the data used in most of the dashboard’s visualizations. The indicators are used across the dashboard.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Chief Information Officer \(CIO\) Dashboard, Executive dashboard overview, Platform Analytics]
---

# Chief Information Officer Dashboard indicators

Indicators provide the data used in most of the dashboard’s visualizations. The indicators are used across the dashboard.

This dashboard employs all three kinds of indicators, Automated, Formula, and Manual. For more information about configuring indicators, see

-   [Automated indicators](../../performance-analytics/concept/automated-indicators.md)
-   [Formula indicators](../../performance-analytics/concept/formula-indicators.md)
-   [Manual indicators](../../performance-analytics/task/t_CreateAManualIndicator.md)

## Overview tab

|Column|Indicator|Source plugin|Indicator type|Formula calculation|
|------|---------|-------------|--------------|-------------------|
|Value|Total value YTD|sn\_compliance|Formula|\(\[\[Cost impact / By year SUM +\]\]+\[\[Revenue impact / By year SUM +\]\]\)|
|Operations|% open and overdue incident assignments|Global|Formula|\( \[\[Number of open and overdue incident assignments\]\] / \[\[Number of open incident assignments that should be responded to in time\]\] \) \* 100|
|Operations|CMDB Health Scorecard|Global|Automated| |
|Operations|% incidents resolved in time|Global|Formula|\( \[\[Number of incidents resolved in time\]\] / \[\[Number of incidents resolved that should have been resolved in time\]\] \) \* 100|
|Security|Number of new security incidents|sn\_sir\_analytics|Automated| |
|Security|SI - Incident Priority 1|sn\_sir\_analytics|Automated| |
|Security|Number of open security incidents|sn\_sir\_analytics|Automated| |
|Execution|PPM - Number of Active Projects|sn\_ciodashboard|Automated| |
|Execution|PPM - Number of Active Red Projects|sn\_ciodashboard|Automated| |
|Experience|eSAT monthly|sn\_ciodashboard|Automated| |
|Experience|Self-Service: Success Rate|sn\_ciodashboard|Formula|\[\[Self-Service: Successful Engagements\]\] / \[\[Self-Service: Engagements\]\] \* 100|

## Value tab

|Column|Indicator|Source plugin|Indicator type|Formula calculation|
|------|---------|-------------|--------------|-------------------|
|Revenue|Revenue impact| |Manual| |
|Revenue|Cost impact| |Manual| |

## Operations tab

|Column|Indicator|Source plugin|Indicator type|Formula calculation|
|------|---------|-------------|--------------|-------------------|
|Incident Management|Average close time of incidents|Global|Formula|\[\[Summed duration of closed incidents\]\] / \[\[Number of closed incidents\]\] / 24|
|Incident Management|% open and overdue incident assignments|Global|Formula|\( \[\[Number of open and overdue incident assignments\]\] / \[\[Number of open incident assignments that should be responded to in time\]\] \) \* 100|
|Incident Management|Number of open incidents|Global|Automated| |
|Incident Management|% incidents resolved in time|Global|Formula|\( \[\[Number of incidents resolved in time\]\] / \[\[Number of incidents resolved that should have been resolved in time\]\] \) \* 100|
|Request Management|Requests backlog growth|Global|Formula|\[\[Number of new requests\]\] - \[\[Number of closed requests\]\]|
|Request Management|Number of open requests|Global|Automated| |
|Request Management|Average close time of requests|Global|Formula|\[\[Summed duration of closed requests\]\] / \[\[Number of closed requests\]\] / 24|
|Change Management|% of urgent changes|Global|Formula|\( \[\[Number of new emergency changes\]\] / \[\[Number of new changes\]\] \) \* 100|
|Change Management|% unsuccessful changes|Global|Formula|\[\[Number of unsuccessful changes\]\] / \[\[Number of closed changes\]\] \* 100|
|Change Management|Average age of open changes|Global|Formula|\[\[Summed age of open changes\]\] / \[\[Number of open changes\]\] / 24|
|Change Management|Change backlog growth|Global|Formula|\[\[Number of new changes\]\] - \[\[Number of closed changes\]\]|
|CMDB|Number of Monitored Configuration Items|Global|Automated| |
|CMDB|Avg CIs Fault count|Global|Automated| |
|CMDB|CMDB health results|Global|Automated| |
|CMDB|CMDB Health Scorecard|Global|Automated| |
|Asset Management|Potential Savings|sn\_ciodashboard|Automated| |
|Asset Management|Percent Spend Not in Use|sn\_ciodashboard|Formula|\(\[\[Potential Savings\]\]+\[\[Over-licensed Amount\]\]\)/\[\[Software Spend\]\]\*100|

## Security tab

|Column|Indicator|Source plugin|Indicator Type|Formula calculation|
|------|---------|-------------|--------------|-------------------|
|Security Incident Response|SI - Incident Priority 1|sn\_sir\_analytics|Automated| |
|Security Incident Response|Number of open security incidents|sn\_sir\_analytics|Automated| |
|Vulnerability Management|Average Age of Vulnerable Items|sn\_vul\_analytics|Formula|\[\[Summed Age of Vulnerable Items\]\] / \[\[Vulnerable Items\]\]|
|Vulnerability Management|Critical Vulnerable Items|sn\_vul\_analytics|Automated| |
|Vulnerability Management|Unassigned Vulnerable Items|sn\_vul\_analytics|Automated| |
|Security Patching|Deferred Vulnerable Items|sn\_vul\_analytics|Automated| |
|Security Patching|Vulnerable Items Mean Time to Remediate|sn\_vul\_analytics|Formula|\[\[Total Duration of Closed Vulnerable Items\]\] / \[\[Closed Vulnerable Items\]\]|
|Security Patching|Closed Vulnerable Items \(Target Met\)|sn\_vul\_analytics|Automated| |
|Compliance|Policy Compliance Score Percentage|sn\_compliance|Automated| |
|Compliance|\# of Failed Control Indicators|sn\_compliance|Automated| |
|Compliance|Citation compliance score percentage|sn\_compliance|Automated| |

## Execution tab

|Column|Indicator|Source plugin|Indicator Type|Formula calculation|
|------|---------|-------------|--------------|-------------------|
|Innovation Management|PPM:Average age of open ideas|sn\_ciodashboard|Formula|\[\[PPM:Total Age of Open Ideas\]\]/\[\[PPM:Open Ideas\]\]/24|
|Innovation Management|PPM:% of ideas converted|sn\_ciodashboard|Formula|\(\[\[PPM:Ideas Converted\]\]/\[\[PPM:Active Ideas\]\]\)\*100|
|Innovation Management|PPM:Ideas Converted|sn\_ciodashboard|Automated| |
|Innovation Management|PPM:Open Ideas|sn\_ciodashboard|Automated| |
|Demand Management|Average age open demand|sn\_ciodashboard|Formula|\[\[PPM - Total Age of Open Demand in Submitted, Screening, Qualified, Approved state\]\]/\[\[PPM - Open Demands Submitted, Screening, Qualified or Approved\]\]/24|
|Demand Management|PPM - Percentage of Demand to Project Last 12 months|sn\_ciodashboard|Formula|\(\[\[PPM - Number of Demands With Projects This Month / 12m running SUM\]\]/\[\[PPM - Number of Total Demands This Month / 12m running SUM\]\]\*100\)|
|Demand Management|PPM - Open Demands Submitted, Screening, Qualified or Approved|sn\_ciodashboard|Automated| |
|Demand Management|PPM - Number of Demands With Projects This Month|sn\_ciodashboard|Automated| |
|Project Portfolio Management|PPM - Number of Active Projects|sn\_ciodashboard|Automated| |
|Project Portfolio Management|PPM - Number of Projects With Critical Issues|sn\_ciodashboard|Automated| |
|Resource Management|Total Allocated hrs|sn\_ciodashboard|Automated| |
|Resource Management|Total available hrs|sn\_ciodashboard|Automated| |
|Resource Management|Total allocated hours quarterly|sn\_ciodashboard|Formula|\[\[Total Allocated hrs / By quarter SUM +\]\]|
|Resource Management|Total available hours quarterly|sn\_ciodashboard|Formula|\[\[Total available hrs / By quarter SUM +\]\]|
|Cost Management|PPM - Planned Cost|sn\_ciodashboard|Automated| |
|Cost Management|PPM - Actual Cost|sn\_ciodashboard|Automated| |
|Cost Management|Variance by portfolio|sn\_ciodashboard|Formula|\(\[\[PPM - Planned Cost\]\]-\[\[PPM - Actual Cost\]\]\);|

## Experience tab

|Column|Indicator|Source plugin|Indicator type|Formula calculation|
|------|---------|-------------|--------------|-------------------|
|Self-Service|Self-Service: Success Rate|sn\_ssa\_pa|Formula|\[\[Self-Service: Successful Engagements\]\] / \[\[Self-Service: Engagements\]\] \* 100|
|Self-Service|Self-Service: Engagements|sn\_ssa\_pa|Formula|\{\{Knowledge: Articles viewed this month\}\} + \{\{Communities: Views this month\}\} + \{\{Catalog: Views this month\}\} + \{\{VA: Conversations this month\}\}|
|Survey Management|eSAT score|sn\_ciodashboard|Automated| |
|Survey Management|cSAT monthly|sn\_ciodashboard|Automated| |

