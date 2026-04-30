---
title: Risk and Compliance Dashboard reports and solutions
description: The Risk and Compliance dashboard is a unified dashboard that provides a comprehensive analytical data of reports available from the major GRC applications for the chief information security officer to understand the compliance and risk posture of the organization. The dashboard consolidates data from various products within the ServiceNow GRC suite of applications.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Risk and compliance dashboard for GRC: Metrics, Cybersecurity Executive Dashboard, Security Operations]
---

# Risk and Compliance Dashboard reports and solutions

The Risk and Compliance dashboard is a unified dashboard that provides a comprehensive analytical data of reports available from the major GRC applications for the chief information security officer to understand the compliance and risk posture of the organization. The dashboard consolidates data from various products within the ServiceNow GRC suite of applications.

**Note:** All reports are available only when the corresponding workspaces are installed.

![Video showing the reports available in the different tabs of the Risk and compliance dashboard.](../image/ced-risk-compliance-grc-db-washingtondc.gif "Risk and compliance dashboard")

## Required ServiceNow AI Platform roles

-   **For Compliance related reports**

    User must have sn\_grc\_dashboards.grc\_ciso\_user role and sn\_bod.ciso role.

-   **For Risk related reports**

    User must have sn\_grc\_dashboards.grc\_ciso\_user role and sn\_bod.ciso role.

-   **For Business Continuity Management related reports**

    User must have sn\_bcm.viewer role and sn\_bod.ciso role.

-   **For Third-party risk related reports**

    User must have sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer role and sn\_bod.ciso role.

-   **For Privacy related reports**

    User must have sn\_privacy.analyst role and sn\_bod.ciso role.

-   **For Audit related reports**

    User must have sn\_audit\_ws.auditor role and sn\_bod.ciso role.


## Access the Risk and Compliance Dashboard

To open the dashboard, navigate to **All** &gt; **Cybersecurity Executive Dashboard** &gt; **Cybersecurity Executive Dashboard**.

## Indicators

-   **Compliance posture**
    -   Compliance percentage: Formula indicator that depicts compliance posture.
    -   All Controls: Automated indicator that supports the formula indicator.
    -   Compliant Controls: Automated indicator that supports the formula indicator.
-   **Privacy compliance posture**

    PA indicator: Processing activity compliance score percentage.


## Breakdowns

Functional Domain.

## Reports

**Note:** All reports are available only when the corresponding workspaces are installed.

<table id="table_omn_21q_mbc"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Compliance posture

</td><td>

Line chart![Line icon.](../../performance-analytics/image/line-icon.png)

</td><td>

Control \[sn\_compliance\_control\]

</td><td>

Provides cybersecurity and risk, and IT risk and compliance posture based on data analysis to the compliance managers.

</td></tr><tr><td>

Risk posture

</td><td>

Donut chart![Donut icon.](../../performance-analytics/image/donut-icon.png)

</td><td>

The source tables are as follows:

-   Risk \[sn\_risk\_risk\]
-   Detailed aggregated risk \[sn\_risk\_advanced\_risk\_assessment\_result\] \(When the Advanced Risk application is installed and Advanced Risk Assessment is enabled

</td><td>

Provides the risk count based on the risk ratings.

</td></tr><tr><td>

Ongoing crisis events

</td><td>

Single Score ![Single-score icon.](../../performance-analytics/image/single-score.png)

</td><td>

Recovery event \[sn\_recovery\_event\] where event type is actual

</td><td>

Displays the total number of ongoing crisis events that are neither approved nor closed.

</td></tr><tr><td>

Assets by recovery status

</td><td>

Donut chart![Donut icon.](../../performance-analytics/image/donut-icon.png)

</td><td>

Assets \[sn\_recovery\_event\_asset\]

</td><td>

Provides the total number of assets for ongoing crisis events grouped by their recovery status, including assets that have been recovered and those that have not.

</td></tr><tr><td>

Recovery tasks by status

</td><td>

Donut chart![Donut icon.](../../performance-analytics/image/donut-icon.png)

</td><td>

Recovery tasks \[sn\_recovery\_event\_task\]

</td><td>

Provides the status of recovery tasks in various states for ongoing crisis events.

</td></tr></tbody>
</table>|Title|Type|Source table|Description|
|-----|----|------------|-----------|
|Authority documents|Donut chart ![Donut icon.](../../performance-analytics/image/donut-icon.png)|Authority Document \[sn\_compliance\_authority\_document\]|Provides data of compliant and non-compliant authority documents in the chart. The list provides details of the authority documents, their individual compliance score in percentage, count of high priority issues and high risk exceptions on the authority documents, and the count of compliant cases.|
|Policies|Donut chart ![Donut icon.](../../performance-analytics/image/donut-icon.png)|Policy \[sn\_compliance\_policy\]|Provides the count of compliant and non-compliant policies in the chart. The list provides details of the policies, their individual compliance score in percentage, count of high priority issues and risk exceptions raised on each policy, and the count of compliant cases.|

<table id="table_vgc_gbq_mbc"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Risk posture

</td><td>

Donut chart ![Donut icon.](../../performance-analytics/image/donut-icon.png)

</td><td>

The source tables are as follows:

-   Risk \[sn\_risk\_risk\]
-   Detailed aggregated risk \[sn\_risk\_advanced\_risk\_assessment\_result\] \(When the Advanced Risk application is installed and Advanced Risk Assessment is enabled\)

</td><td>

Provides the risk count based on the risk ratings.

</td></tr><tr><td>

Risk posture

</td><td>

List ![List icon.](../../performance-analytics/image/scorecard-icon.png)

</td><td>

GRC Content Status \[sn\_grc\_content\_reports\]

</td><td>

Provides the risk rating for each organizational risk to understand the overall risk assessment results. These ratings help organizations understand the potential impact and likelihood of various risks, enabling them to prioritize and manage these risks. The Risk posture card also highlights the following information for each risk:-   **Risk appetite**: Risk appetite value defined.
-   **High priority issues**: The number of issues with priority is defined as High.
-   **Overdue risk response tasks**: Number of overdue risk response tasks.
-   **KRI Breach %**: Percentage of Key Risk Indicators \(KRIs\) that have exceeded their predefined thresholds or limits.

</td></tr><tr><td>

Third-party risk posture

</td><td>

Donut chart ![Donut icon.](../../performance-analytics/image/donut-icon.png)

</td><td>

Third-party risks \[sn\_grc\_dashboards\_third\_party\_risk\]

</td><td>

Provides the risk rating for each third party. The risk rating is the overall assessment rating that considers the scores and ratings from all assessments conducted for a third party or vendor. The Third-party risk posture card also highlights the following information for each third party or vendor:-   **Risk criteria**: Group of risk domains \(sometimes called risk areas in other platform features\) that applies to a particular type of third party.
-   **Risk tier**: Value determined based on the responses collected after an inherent risk assessment \(IRQ\) is completed.
-   **Risk intelligence rating**: Aggregate of all the scores collected from Risk intelligence providers.
-   **Overdue risk response tasks**: Number of overdue risk response tasks.

</td></tr></tbody>
</table>|Title|Type|Source table|Description|
|-----|----|------------|-----------|
|Privacy compliance posture|Line ![Line icon](../../performance-analytics/image/line-icon.png)|PA indicator: Processing activity compliance score percentage \[pa\_indicators\]|Provides the compliance posture by month and is plotted by referring to the overall compliance score across all the processing activities.|
|Overdue high priority issues|Single score ![Single score](../../performance-analytics/image/single-score.png)|Issues \[sn\_grc\_issue\]|Provides a focused overview of all overdue high-priority privacy-related issues, enabling quick identification and resolution of critical tasks to ensure compliance and data protection.|
|Privacy risk heatmap|Heatmap ![Heatmap icon](../../performance-analytics/image/heatmap.png)|Risk assessment methodology \[sn\_risk\_advanced\_risk\_assessment\_methodology\]|Provides the privacy risk assessment data in the form of a heatmap. Privacy risk assessments are detailed assessments that are conducted if the criticality score is high. Assess each risk that is associated with the processing activity and know the aggregated risk score on the processing activity. After you assess the privacy risks, you can view the privacy risk posture on the risk heatmap.|

|Title|Type|Source table|Description|
|-----|----|------------|-----------|
|Entities|List ![List icon.](../../performance-analytics/image/scorecard-icon.png)|Entity compliance status \[sn\_compliance\_entities\_reports\]|Provides the summary of risks directly associated with the entity that contribute to the overall risk rating of the entity. The list also displays the compliance score of entities, and high priority issues and risk exceptions that are raised as a result of the non-compliant controls associated with the entity.|

|Title|Type|Source table|Description|
|-----|----|------------|-----------|
|Open and upcoming audit engagements|List ![List icon.](../../performance-analytics/image/scorecard-icon.png)|Engagement \[sn\_audit\_engagement\]|Provides a list of open and upcoming audit engagements. The list also provides details of the engagement lead for each authority document, each engagement's planned start and end dates, high-priority issues, percentage of fieldwork that is completed, and the milestones in progress.|

## Filters

|Name|Type|Description|
|----|----|-----------|
|Risk criteria|Report|Depending on which risk criterias you select, the donut chart and list shows the third parties or vendors that are in those risk areas.|

