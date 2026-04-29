---
title: Chief Customer Operations Officer Dashboard indicators
description: Indicators provide the data used in most of the dashboard’s visualizations. The indicators are used across the dashboard.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Chief Customer Operations Officer \(CCO\) Dashboard, Executive dashboard overview, Platform Analytics]
---

# Chief Customer Operations Officer Dashboard indicators

Indicators provide the data used in most of the dashboard’s visualizations. The indicators are used across the dashboard.

This dashboard employs all three kinds of indicators, Automated, Formula, and Manual. For more information about configuring indicators, see

-   [Automated indicators](../../performance-analytics/concept/automated-indicators.md)
-   [Manual indicators](../../performance-analytics/task/t_CreateAManualIndicator.md)

## Outcome tab

<table id="table_zcc_dry_mgc"><thead><tr><th>

Column

</th><th>

Indicator

</th><th>

Source plugin

</th><th>

Indicator type

</th><th>

Indicator source / Formula calculation / Additional conditions

</th></tr></thead><tbody><tr><td>

Sentiment

</td><td>

CSAT

</td><td>

com.snc.pAutomatedcustomer\_service\_advanced

</td><td>

Formula

</td><td>

\[\[Number of satisfied customers \(CSAT\)\]\]/\[\[Number of CSAT survey respondents\]\]\*100

</td></tr><tr><td>

Sentiment

</td><td>

Number of satisfied customers \(CSAT\) - CCO

</td><td>

com.snc.pAutomatedcustomer\_service\_advanced

</td><td>

Automated

</td><td>

Metric Result.NewConditions: Metric Category = Customer Service Satisfaction Survey and Metric = Overall Customer Satification and Instance Related record 1 != \(empty\) and Actual value &gt;= 3

</td></tr><tr><td>

Sentiment

</td><td>

cSAT Trend

</td><td>

 

</td><td>

Formula

</td><td>

\[\[CSAT / By month AVG +\]\]

</td></tr><tr><td>

Sentiment

</td><td>

CSAT by Business Unit

</td><td>

 

</td><td>

Formula

</td><td>

\[\[Number of satisfied customers \(CSAT\) - CCO / By month SUM +\]\]/\[\[Number of CSAT survey respondents- CCO / By month SUM +\]\]\*100

</td></tr><tr><td>

Proactive

</td><td>

PCSO: Number of Proactive reported cases promoted to major

</td><td>

com.snc.proactive\_cs\_ops

</td><td>

Automated

</td><td>

PCSO.CaseInstallbaseitemSoldproduct.Created-   Condition: Major case state = Accepted
-   Calculation: Count Distinct \(cs\_case\)

</td></tr><tr><td>

Proactive

</td><td>

PCSO: Number of Affected Install Base Items

</td><td>

 

</td><td>

Automated

</td><td>

PCSO.CaseInstallbaseitemSoldproduct.Created.ThisMonthCalculation: Count Distinct \(aib\_install\_base\_item\)

</td></tr><tr><td>

Proactive

</td><td>

Proactive cases

</td><td>

com.snc.proactive\_cs\_ops

</td><td>

Formula

</td><td>

\[\[PCSO: Number of Proactive Cases / By month SUM +\]\]

</td></tr><tr><td>

Proactive

</td><td>

Top Impacted Customers

</td><td>

com.snc.proactive\_cs\_ops

</td><td>

Formula

</td><td>

\[\[PCSO: Number of outages / By month SUM +\]\]

</td></tr><tr><td>

Self Service

</td><td>

Self-Service: Success Rate

</td><td>

com.snc.self\_service\_analytics\_core, com.snc.pAutomatedself\_service\_analytics\_csm, com.sn\_communities, com.glide.cs.chatbot

</td><td>

Formula

</td><td>

\[\[Self-Service: Successful Engagements\]\] / \[\[Self-Service: Engagements\]\] \* 100

</td></tr><tr><td>

Self Service

</td><td>

Self-Service: Successful Engagements

</td><td>

com.snc.self\_service\_analytics\_core, com.snc.pAutomatedself\_service\_analytics\_csm, com.sn\_communities, com.glide.cs.chatbot

</td><td>

Formula

</td><td>

\{\{Knowledge: Helpful Feedback\}\} + \{\{Communities: Helpful Feedback\}\} + \{\{Number of Catalog requests\}\} + \{\{VA: Successful Conversations\}\}

</td></tr><tr><td>

Service Health

</td><td>

% of closed cases with breached SLAs

</td><td>

com.snc.pAutomatedcustomer\_service\_advanced

</td><td>

Formula

</td><td>

\(\[\[Number of closed cases with breached SLAs\]\]/\[\[Number of Closed Cases\]\]\) \* 100

</td></tr><tr><td>

Service Health

</td><td>

Average resolution time of cases

</td><td>

com.snc.pAutomatedcustomer\_service\_advanced

</td><td>

Formula

</td><td>

\[\[Summed duration of resolved cases\]\] / \[\[Number of resolved cases\]\] / 24

</td></tr><tr><td>

Service Health

</td><td>

SLA Attainment Trend

</td><td>

 

</td><td>

Formula

</td><td>

\[\[% of closed cases with breached SLAs / By month AVG +\]\]

</td></tr><tr><td>

Service Health

</td><td>

Average age of open cases

</td><td>

com.snc.pAutomatedcustomer\_service\_advanced

</td><td>

Formula

</td><td>

\[\[Summed age of open cases\]\] / \[\[Number of Open Cases\]\] / 24

</td></tr><tr><td>

Spotlight

</td><td>

Cases in Spotlight

</td><td>

com.sn\_cco\_dashboard

</td><td>

Automated

</td><td>

Cases in Spotlight

</td></tr><tr><td>

Spotlight

</td><td>

Cases in Spotlight - unassigned

</td><td>

com.sn\_cco\_dashboard

</td><td>

Automated

</td><td>

Cases in Spotlight - unassigned

</td></tr><tr><td>

Spotlight

</td><td>

Unassigned Spotlight cases trend

</td><td>

 

</td><td>

Formula

</td><td>

\[\[Cases in Spotlight - unassigned / By month SUM +\]\]

</td></tr></tbody>
</table>## Operations tab

|Column|Indicator|Source plugin|Indicator Type|Indicator Source or Formula calculation|
|------|---------|-------------|--------------|---------------------------------------|
|Throughput|Number of Closed Cases|com.snc.pAutomatedcustomer\_service\_advanced|Automated|Cases.Closed|
|Throughput|\# of Cases Resolved on First Contact|com.snc.pAutomatedcustomer\_service\_advanced|Automated|Cases.Resolved|
|Availability|PCSO: Number of outages|com.snc.proactive\_cs\_ops|Automated|PCSO.OutageCaseInstallBase.Created|
|Availability|PCSO: Number of Impacted Customers|com.snc.proactive\_cs\_ops|Automated|PCSO.OutageCaseInstallBase.Created.ThisMonth|
|Availability|Outages Trend| |Formula|\[\[PCSO: Number of outages / By month SUM +\]\]|
|Risk|Get Accounts in Risk - headline| |Automated|Get Accounts in Risk - headline|
|Risk|Get Products in Risk - headline| |Automated|Get Products in Risk - headline|
|Risk|Accounts at risk - Trend| |Formula|\[\[Get Accounts in Risk - headline / By quarter SUM +\]\]|
|Risk|Products at risk - Trend| |Formula|\[\[Get Products in Risk - headline / By quarter SUM +\]\]|
|Performance|Average age of open cases|com.snc.pAutomatedcustomer\_service\_advanced|Formula|\[\[Summed age of open cases\]\] / \[\[Number of Open Cases\]\] / 24|
|Performance|Average re-assignment of open cases|com.snc.pAutomatedcustomer\_service\_advanced|Formula|\[\[Summed re-assignment count of open cases\]\] / \[\[Number of Open Cases\]\]|
|Performance|Trend of average age of open cases|com.snc.pAutomatedcustomer\_service\_advanced|Formula|\[\[Average age of open cases / By month SUM +\]\]|
|Performance|Trend of Average re-assignment of open cases|com.snc.pAutomatedcustomer\_service\_advanced|Formula|\[\[Average re-assignment of open cases / By month SUM +\]\]|

