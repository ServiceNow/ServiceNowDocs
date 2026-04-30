---
title: General Counsel Dashboard indicators
description: Indicators provide the data used in most of the dashboard’s visualizations. The indicators are used across the dashboard.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-09-23"
reading_time_minutes: 2
breadcrumb: [General Counsel \(GC\) Dashboard, Executive dashboard overview, Dashboards, Platform Analytics experience, Platform Analytics]
---

# General Counsel Dashboard indicators

Indicators provide the data used in most of the dashboard’s visualizations. The indicators are used across the dashboard.

This dashboard employs all three kinds of indicators, Automated, Formula, and Manual. For more information about configuring indicators, see

-   [Automated indicators](../../performance-analytics/concept/automated-indicators.md)
-   [Formula indicators](../../performance-analytics/concept/formula-indicators.md)
-   [Manual indicators](../../performance-analytics/task/t_CreateAManualIndicator.md)

<table id="table_zcc_dry_mgc"><thead><tr><th>

Column

</th><th>

Indicator

</th><th>

Source plugin

</th><th>

Indicator type

</th><th>

Indicator Source / Formula calculation / Additional conditions

</th></tr></thead><tbody><tr><td>

Contracts

</td><td>

Open Backlog Contract Requests

</td><td>

-   sn\_lg\_pa
-   sn\_lg\_contracts
-   sn\_lg\_ops

</td><td>

Automated

</td><td>

Legal Contracts : Active

</td></tr><tr><td>

Contracts

</td><td>

Open Contract Amount

</td><td>

-   sn\_lg\_pa
-   sn\_lg\_contracts
-   sn\_lg\_ops

</td><td>

Automated

</td><td>

Legal Contracts : ActiveCalculation: Sum \(deal\_size\)

</td></tr><tr><td>

Contracts

</td><td>

Average request completion time for contracts

</td><td>

-   sn\_lg\_pa
-   sn\_lg\_contracts
-   sn\_lg\_ops

</td><td>

Automated

</td><td>

Legal.Closed.Requests-   Additional conditions: Practice area = Contracts and Task type = General Contract Support
-   Calculation: Average \(Legal Request Completion time\(days\)\)

</td></tr><tr><td>

Service Delivery

</td><td>

Open Legal Requests

</td><td>

-   sn\_lg\_pa
-   sn\_lg\_ops

</td><td>

Automated

</td><td>

Legal.Requests.Open

</td></tr><tr><td>

Service Delivery

</td><td>

Open Legal Matters

</td><td>

-   sn\_lg\_pa
-   sn\_lg\_ops
-   sn\_lg\_matter

</td><td>

Automated

</td><td>

Legal.Matters.Open

</td></tr><tr><td>

Service Delivery

</td><td>

Average request completion time per practice area

</td><td>

-   sn\_lg\_pa
-   sn\_lg\_ops

</td><td>

Automated

</td><td>

Legal.Closed.RequestsCalculation: Average \(Legal Request Completion time\(days\)\)

</td></tr><tr><td>

Service Delivery

</td><td>

Average matter completion time per practice area

</td><td>

-   sn\_lg\_pa
-   sn\_lg\_ops
-   sn\_lg\_matter

</td><td>

Automated

</td><td>

Legal.Closed.MattersCalculation: Average \(Legal Matter Completion time\(days\)\)

</td></tr><tr><td>

Privacy and Compliance

</td><td>

Open Privacy and Compliance Requests

</td><td>

-   sn\_lg\_pa
-   sn\_lg\_ops

</td><td>

Formula

</td><td>

\[\[Open Legal Requests &gt; Practice area = Privacy\]\] + \[\[Open Legal Requests &gt; Practice area = Compliance\]\]

</td></tr><tr><td>

Privacy and Compliance

</td><td>

% of privacy and compliance requests that met SLA

</td><td>

-   sn\_lg\_pa
-   sn\_lg\_ops

</td><td>

Formula

</td><td>

\[\[Requests Completed within SLA\]\]/\[\[Total Completed Legal Requests with SLA\]\] \* 100

</td></tr><tr><td>

Privacy and Compliance

</td><td>

Average request completion time for privacy and compliance

</td><td>

-   sn\_lg\_pa
-   sn\_lg\_ops

</td><td>

Automated

</td><td>

Legal.Closed.Matters-   Additional conditions: Practice area = Privacy or Practice area = Compliance
-   Calculation: Average \(Legal Matter Completion time\(days\)\)

</td></tr><tr><td>

Digital Forensics

</td><td>

Open Digital Forensic Requests

</td><td>

-   sn\_lg\_pa
-   sn\_lg\_ops
-   sn\_lg\_forensics

</td><td>

Automated

</td><td>

Legal.Matter.Task.Open

</td></tr><tr><td>

Digital Forensics

</td><td>

Average activity completion time for digital forensics

</td><td>

-   sn\_lg\_pa
-   sn\_lg\_ops
-   sn\_lg\_forensics

</td><td>

Automated

</td><td>

Legal.DigitalForensics.Closed.Matter.TasksCalculation: Average \(Legal Matter Task Completion time\(days\)\)

</td></tr><tr><td>

Self Service

</td><td>

Number of legal kb article views

</td><td>

com.snc.knowledge3

</td><td>

Automated

</td><td>

article.kb\_knowledge\_base=1ec18f62b31713007a6de81816a8dc9e^EQCalculation: Sum \(times\_viewed\)

</td></tr><tr><td>

Self Service

</td><td>

Total VA conversations for legal

</td><td>

-   sn\_lg\_va
-   sn\_lg\_ops

</td><td>

Automated

</td><td>

Conversations.NewAdditional conditions: Topic Application = Legal Virtual Agent Conversations

</td></tr></tbody>
</table>