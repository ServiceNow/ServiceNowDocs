---
title: Cybersecurity Executive Dashboard
description: The Cybersecurity Executive Dashboard is a comprehensive solution that empowers Chief Information Security Officers \(CISOs\) and cybersecurity executives with visibility into the organization's security posture and initiatives. The dashboard consolidates data from various products within the ServiceNow Security Operations suite and Governance, Risk and Compliance \(GRC\).
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-12-02"
reading_time_minutes: 23
keywords: [Cybersecurity Executive Dashboard, servicenow, Chief Information Security Officers, cybersecurity, cybersecurity dashboard, cybersecurity executive, benchmarking, benchmark plugin, benchmarks dashboard, target, targets, performance analytics, dashboard, dashboards, ceo dashboard, share dashboard, cybersecurity executive dashboard, executive dashboard, reports and dashboards, ciso dashboard, responsive dashboard, breakdown dashboard, performance analytics dashboard, security operations dashboard, cxo dashboards, platform analytics dashboard, compliance dashboard]
breadcrumb: [Security Operations]
---

# Cybersecurity Executive Dashboard

The Cybersecurity Executive Dashboard is a comprehensive solution that empowers Chief Information Security Officers \(CISOs\) and cybersecurity executives with visibility into the organization's security posture and initiatives. The dashboard consolidates data from various products within the ServiceNow Security Operations suite and Governance, Risk and Compliance \(GRC\).

The dashboard provides the following features:

-   Organization-wide security posture scoring
-   Security, Risk, and Compliance scores by business unit
-   Customizable monitoring
-   Unified view of an organization's security landscape
-   Benchmarking
-   User-friendly interface
-   Visibility into phishing simulation metrics from KnowBe4 and Microsoft Defender for Office 365

![Top half of CISO dashboard with targets and Overview tab selected](../image/vr-ciso-db-top.png)

These features enable proactive decision making by providing quick access to critical security metrics. Thus, making it an indispensable tool for enhancing overall security resilience and readiness.

![Bottom half of CISO dashboard with Overview tab and Business units selected](../image/vr-ciso-db-bottom.png)

## Required ServiceNow AI Platform roles

-   CISO \(sn\_bod.ciso\) to view and share the dashboard.
-   sn\_bod.ciso\_admin to view, share the dashboard, configure weights for security posture rating.
-   GRC CISO User \(sn\_grc\_dashboards.grc\_ciso\_user\) to view risk and compliance reports.

## Access the Cybersecurity Executive Dashboard

To open the dashboard, navigate to **All** &gt; **Cybersecurity Executive Dashboard** &gt; **Cybersecurity Executive Dashboard**.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

<table id="table_jfc_mk1_kzb"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Chief Information Security Officers \(CISOs\)

</td><td>

CISOs gain insights on vulnerability management, incident management, organization security posture, phishing simulation metrics, and so on, for their organizations.

</td></tr></tbody>
</table>## Data visualization

**Note:** To learn more about a widget, select the information icon ![Information icon](../../../product/vulnerability-response/image/info-icon.png).

<table id="table_ofc_mk1_kzb"><thead><tr><th>

Metrics

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Targets

</td><td>

Percentage

</td><td>

Shows the set target to cover for a metric.

 The status of the targets is indicated through color coding. It shows all the targets whose review date is either within the past 30 days or upcoming. You can set the number of days for displaying targets using the **sn\_bod.show\_targets\_from** system property. Additionally, these targets can be edited.

 See [Set targets](../../../product/vulnerability-response/task/set-targets-cybersecurity-dashboard.md) for more information.

</td></tr></tbody>
</table><table id="table_n43_yv4_mbc"><thead><tr><th>

Metrics

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Security score

</td><td>

Single Score![Single-score icon](../../performance-analytics/image/single-score.png)

</td><td>

Overall score of the organization's security posture by considering vulnerable items, security incidents, major security incidents, and misconfigurations.

</td></tr><tr><td>

Insights

</td><td>

Highlights

</td><td>

Highlights of the entire dashboard.

</td></tr><tr><td>

Compliance score

</td><td>

Single Score![Single-score icon](../../performance-analytics/image/single-score.png)

</td><td>

Provides compliance posture of the organization with the help of compliance score calculated based on the percentage of compliant controls out of the total number of controls.

</td></tr><tr><td>

Risk score

</td><td>

Single Score![Single-score icon](../../performance-analytics/image/single-score.png)

</td><td>

Provides the count of risk statements based on the risk ratings. It helps organizations understand the potential impact and likelihood of various risks, enabling them to prioritize and manage these risks.

</td></tr><tr><td colspan="3">

Business critical entities

</td></tr><tr><td>

Business units

</td><td>

Single Score![Single-score icon](../../performance-analytics/image/single-score.png)

</td><td>

Overall security score of the business units by considering the risk associated with vulnerabilities, misconfigurations, Operational Technology \(OT\) vulnerabilities, security incidents, and major security incidents. The health label of the business units is based on the security score only.

 To see how these labels are assigned, navigate to Risk Score Weights \[sn\_sec\_cmn\_risk\_score\_weight\_list.do\] table and search for business entity. Labels such as 'Healthy' are assigned based on predefined value ranges. For instance, a security score ranging from 0 to 39 is labeled as Healthy. The color coding for these labels is specified in the`UnifiedCISOutils` script include. You can configure both the value range as well as the colors for the labels.

 To see how the business unit and business unit head names are assigned, go to **All** &gt; **Organization** &gt; **Business Units**.

 **Note:** Depending on the plugins you have enabled, you can access the Compliance score, Risk score, and Security score. To view the Compliance and Risk score, you must activate the GRC plugins. To view the Security score, you must activate the Security Operations related plugins. See Applications to active section for more information.

</td></tr><tr><td>

Business services

</td><td>

Single Score![Single-score icon](../../performance-analytics/image/single-score.png)

</td><td>

Overall security score of the business services by considering the risk associated with vulnerabilities, misconfigurations, Operational Technology \(OT\) vulnerabilities, security incidents, and major security incidents.

 To see how these labels are assigned, navigate to Risk Score Weights \[sn\_sec\_cmn\_risk\_score\_weight\_list.do\] table and search for business entity. Labels such as 'Healthy', 'Moderate' and 'Critical' are assigned based on predefined value ranges. For instance, a security score ranging from 0 to 39 is labeled as Healthy. The color coding for these labels is specified in the`UnifiedCISOutils` script include. You can configure both the value range as well as the colors for the labels.

 To see how the business unit and business unit head name are assigned, go to **All** &gt; **Organization** &gt; **Business Units**.

 **Note:** Depending on the plugins you have enabled, you can access the Compliance score, Risk score, and Security score. To view the Compliance and Risk score, you must activate the GRC plugins. To view the Security score, you must activate the Security Operations related plugins. See Applications to active section for more information.

</td></tr></tbody>
</table><table id="table_bd1_cw4_mbc"><thead><tr><th>

Metrics

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mean time to remediate \(monthly\)

</td><td>

Line

</td><td>

Average time taken to close vulnerabilities and failed test results across all assets \(hosts, containers, and applications\) in a month.

 It also provides the following metrics:

-   Target: Target set in days to remediate the vulnerabilities.
-   Gap: Difference in days between the target and actual time taken to remediate the vulnerabilities.
-   Industry benchmark: Average of metrics from the peers in the same industry.
-   Global benchmark: Average of metrics from the peers in the global market

 See [Opt-in for benchmark scores](../../../product/vulnerability-response/task/vr-retrieve-benchmark-results.md) on how to view the benchmark scores.

</td></tr><tr><td>

Average age of active vulnerabilities \(monthly\)

</td><td>

Single Score![Single-score icon](../../performance-analytics/image/single-score.png)

</td><td>

Monthly average age of all three types of vulnerable items. It also provides a comparison of the current month age with the previous month.

 It also provides the following metrics:

-   Industry benchmark: Average of metrics from the peers in the same industry.
-   Global benchmark: Average of metrics from the peers in the global market
-   Target: Target set in days to remediate the vulnerabilities.

</td></tr><tr><td>

Remediation efficiency \(monthly\)

</td><td>

Single Score![Single-score icon](../../performance-analytics/image/single-score.png)

</td><td>

Percentage of monthly closed vulnerable items to monthly active vulnerable items.

 It also provides the following metrics:

-   Percentage change from the previous month.
-   Target: Target set in percentage to remediate the vulnerabilities.
-   Gap: The gap between target and current score.
-   Industry benchmark: Average of metrics from the peers in the same industry.
-   Global benchmark: Average of metrics from the peers in the global market

</td></tr><tr><td>

Average age of active vulnerabilities by assignment group

</td><td>

Multiple line

</td><td>

Average age of active vulnerabilities for each assignment group.

</td></tr><tr><td>

Vulnerabilities by risk rating and age

</td><td>

Heatmap![Heatmap icon](../../performance-analytics/image/heatmap.png)

</td><td>

Breakdown of active vulnerabilities across hosts, containers, and applications by risk rating and age.

</td></tr><tr><td>

Remediation target adherence by assignment group

</td><td>

Vertical Bar![Bar](../../../reuse/reporting/image/trend.svg)

</td><td>

The ratio of the number of vulnerabilities and misconfigurations closed within remediation target to the total number of vulnerabilities and misconfigurations closed.

</td></tr><tr><td>

Scan coverage

</td><td>

Percentage

</td><td>

Percentage of the assets scanned in the last 90 days out of all assets in the CMDB.

</td></tr><tr><td>

Assets scanned vs unscanned

</td><td>

Horizontal bar

</td><td>

Breakdown of assets scanned in the last 90 days and total assets in CMDB by CI Class

</td></tr><tr><td>

Assets scanned

</td><td>

Horizontal bar

</td><td>

Assets scanned in the last 90 days for vulnerabilities versus configuration compliance.

</td></tr><tr><td>

Active critical and high findings trend

</td><td>

Multiple line![Heatmap icon](../../performance-analytics/image/heatmap.png)

</td><td>

Daily trend of vulnerabilities and misconfigurations that have critical and high risk rating.

</td></tr><tr><td>

Vulnerabilities by asset category and risk rating

</td><td>

Vertical Bar![Bar](../../../reuse/reporting/image/trend.svg)

</td><td>

Breakdown of active vulnerabilities and misconfigurations by asset category and risk rating \(critical, high, and medium\).

</td></tr><tr><td>

Deferred findings by reason and assignment group

</td><td>

Vertical Bar![Bar](../../../reuse/reporting/image/trend.svg)

</td><td>

Breakdown of active vulnerabilities and misconfigurations deferred by deferral reason and assignment group.

</td></tr><tr><td colspan="3">

Operational technology \(OT\)

</td></tr><tr><td>

Active critical and high vulnerability trend

</td><td>

Line![Heatmap icon](../../performance-analytics/image/heatmap.png)

</td><td>

Daily trend of OT vulnerabilities that are active with critical and high risk rating.

</td></tr><tr><td>

Mean time to remediate \(monthly\)

</td><td>

Single Score![Single-score icon](../../performance-analytics/image/single-score.png)

</td><td>

Average time taken to close OT vulnerabilities. The ratio of total age of OT vulnerabilities closed to the total number of OT vulnerabilities.

 It also provides the following metrics:

-   Percentage change from the previous month.
-   Target: Target set in days to remediate the vulnerabilities.
-   Industry benchmark: Average of metrics from the peers in the same industry.
-   Global benchmark: Average of metrics from the peers in the global market

 See [Opt-in for benchmark scores](../../../product/vulnerability-response/task/vr-retrieve-benchmark-results.md) on how to view the benchmark scores.

</td></tr><tr><td>

Vulnerabilities by risk rating and age

</td><td>

Heatmap![Heatmap icon](../../performance-analytics/image/heatmap.png)

</td><td>

Breakdown of active OT vulnerabilities by risk rating and age.

</td></tr><tr><td>

Average age of active vulnerabilities \(monthly\)

</td><td>

Line chart

</td><td>

Monthly average age of OT vulnerable items. It also provides a comparison of the current month age with the previous month.

</td></tr><tr><td>

Vulnerabilities by state and age

</td><td>

Heatmap![Heatmap icon](../../performance-analytics/image/heatmap.png)

</td><td>

Breakdown of active OT vulnerabilities by state and age.

</td></tr></tbody>
</table><table id="table_ccs_r1p_mbc"><thead><tr><th>

Metrics

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Major security incidents

</td><td>

Single Score![Single-score icon](../../performance-analytics/image/single-score.png)

</td><td>

Number of major security incidents that are currently active.

</td></tr><tr><td>

Average security incidents resolution time \(monthly\)

</td><td>

Single Score![Single-score icon](../../performance-analytics/image/single-score.png)

</td><td>

Monthly average resolution time in days of closed security incidents.

 It also provides the following metrics:

-   Percentage change from the previous month.
-   Target: Target set in days to remediate the security incidents.
-   Gap: The gap between the actual days taken to resolve and the target set to remediate.
-   Industry benchmark: Average of metrics from the peers in the same industry.
-   Global benchmark: Average of metrics from the peers in the global market

</td></tr><tr><td>

Average time to eradicate \(monthly\)

</td><td>

Line chart

</td><td>

Monthly average resolution in days to eradicate security incidents.

</td></tr><tr><td>

Average time to identify \(monthly\)

</td><td>

Single Score![Single-score icon](../../performance-analytics/image/single-score.png)

</td><td>

Monthly average resolution in days to identify the security incidents.

</td></tr><tr><td>

Average time to contain \(monthly\)

</td><td>

Single Score![Single-score icon](../../performance-analytics/image/single-score.png)

</td><td>

Monthly average resolution in days to contain security incidents.

</td></tr><tr><td>

Active incidents by priority and category

</td><td>

Heatmap![Heatmap icon](../../performance-analytics/image/heatmap.png)

</td><td>

Count of active security incidents, which are categorized by priority and category.

</td></tr><tr><td>

Closed and open incidents trend

</td><td>

Vertical Bar![Bar](../../../reuse/reporting/image/trend.svg)

</td><td>

Breakdown of closed and open incidents.

</td></tr><tr><td>

Active incidents by states

</td><td>

Vertical Bar![Bar](../../../reuse/reporting/image/trend.svg)

</td><td>

Breakdown of active incidents based on their states.

</td></tr></tbody>
</table>|Metrics|Type|Description|
|-------|----|-----------|
|Monthly phishing simulation overview|Vertical Bar![Bar](../../../reuse/reporting/image/trend.svg)|Sum of users who performed the actions such as opened, clicked, and reported in the phishing simulation along with the sum of total users of each simulation for the past six months.|

<table id="table_obb_vcp_mbc"><tbody><tr><td colspan="3">

To view Risk and Compliance widgets, you must activate the GRC plugins. For information on GRC plugins, see the Applications to activate section. For information on GRC widgets, see [Risk and compliance dashboard for GRC: Metrics](grc-cybersecurity-risk-compl-dashboard.md).

</td></tr></tbody>
</table>## Indicators

-   **Host SLA – Closed**

    This indicator is calculated daily. It considers the total age of all host vulnerabilities that were closed on the previous day at the time of calculation.

-   **Container SLA – Closed**

    This indicator is calculated daily. It considers all the container vulnerabilities that were closed on the previous day at the time of calculation.

-   **Application SLA – Closed**

    This indicator is calculated daily. It considers the total age of all the application vulnerabilities that were closed on the previous day at the time of calculation.

-   **Test Result SLA – Passed**

    This indicator is calculated daily. It considers all the test result vulnerabilities that were passed on the previous day at the time of calculation.

-   **Host SLA - Closed Count**

    This indicator is calculated daily. It considers the count of all host vulnerabilities that were closed on the previous day at the time of calculation.

-   **Container SLA - Closed Count**

    This indicator is calculated daily. It considers the count of all container vulnerabilities that were closed on the previous day at the time of calculation.

-   **Application SLA - Closed Count**

    This indicator is calculated daily. It considers the count of all application vulnerabilities that were closed on the previous day at the time of calculation.

-   **Test Result SLA – Passed Count**

    This indicator is measured daily. It considers the count of all test result vulnerabilities that were last passed on the previous day at the time of calculation.

-   **Scanned Assets**

    This indicator is calculated daily. It considers the sum of scanned CIs from the sn\_vul\_analytics\_scan\_coverage\_config table, which includes those last scanned within the past 90 days, across all CMDB CI Classes.

-   **Scannable Assets**

    This indicator is calculated daily. It considers the sum of total CIs from sn\_vul\_analytics\_scan\_coverage\_config table for all the CMDB CI Classes present.

-   **Vulnerable Items**

    This indicator is calculated daily. It considers the count of active vulnerable items at the time of calculation.

-   **Application Vulnerable Item**

    This indicator is calculated daily. It considers the count of active application vulnerable items at the time of calculation.

-   **Container Vulnerable Item**

    This indicator is calculated daily. It considers the count of active container vulnerable items at the time of calculation.

-   **Summed Age of Vulnerable Items**

    This indicator is calculated daily. It considers the summed age of active vulnerable items at the time of calculation.

-   **Summed Age of Application Vulnerable Items**

    This indicator is calculated daily. It considers the summed age of active application vulnerable items at the time of calculation.

-   **Open Vulnerable Items**

    This indicator is calculated daily. It considers the open vulnerable items at the time of calculation.

-   **Open Container Vulnerable Items**

    This indicator is calculated daily. It considers the open container vulnerable items at the time of calculation.

-   **Open Application Vulnerable Items**

    This indicator is calculated daily. It considers the open application vulnerable items at the time of calculation.

-   **Active Test Results**

    This indicator is calculated daily. It considers the open test results at the time of calculation.

-   **Deferred VITs**

    This indicator is calculated daily. It has an indicator source as host vulnerable item.

-   **Deferred AVITs**

    This indicator is calculated daily. It has an indicator source as an application vulnerable item.

-   **Deferred CVITs**

    This indicator is calculated daily. It has an indicator source as a container vulnerable item.

-   **Deferred Test Results**

    This indicator is calculated daily. It considers the test results that were in a deferred state.

-   **Open Config Issues - Test results**

    This indicator is calculated daily. It has an indicator source as test result for the Unified Vulnerability Response Dashboard.

-   **SI-Average Time To Identify**

    This indicator is calculated daily. It considers the security incident where definition is time to identify at the time of calculation.

-   **SI - Average Duration Time**

    This indicator is calculated daily. It considers the security incident where the definition is an incident state duration at the time of calculation.

-   **Number of Open Major Security Incidents**

    This indicator is calculated daily. It considers open major security incidents at the time of calculation.

-   **Number of closed security incidents**

    This indicator is calculated daily. It considers closed security incidents at the time of calculation.

-   **Closed Application Vulnerable Items**

    This indicator is calculated daily. It considers closed application vulnerable items at the time of calculation.

-   **Closed Container Vulnerable Items**

    This indicator is calculated daily. It considers closed container vulnerable items at the time of calculation.

-   **Closed Vulnerable Items**

    This indicator is calculated daily. It considers closed vulnerable items at the time of calculation.

-   **Get Max Risk Score for Vulnerable Items**

    This indicator is calculated daily. It considers the maximum risk score for vulnerable items at the time of calculation.

-   **Get Max Risk Score for Container Vulnerable Item**

    This indicator is calculated daily. It considers the maximum risk score for container vulnerable items at the time of calculation.

-   **Get Max Risk Score for Application Vulnerable Items**

    This indicator is calculated daily. It considers the max risk score for application vulnerable items at the time of calculation.

-   **Summed Risk Score of VITs**

    This indicator is calculated daily. It considers the sum of risk scores of vulnerable items at the time of calculation.

-   **Summed Risk Score of AVIs**

    This indicator is calculated daily. It considers the sum of risk scores of application vulnerable items at the time of calculation.

-   **Summed Risk Score of CVIs**

    This indicator is calculated daily. It considers the sum of risk scores of container vulnerable items at the time of calculation.

-   **Summed Risk Score of Misconfigurations**

    This indicator is calculated daily. It considers the sum of risk scores of test results at the time of calculation.

-   **Get Max Risk Score for SI Incidents**

    This indicator is calculated daily. It considers the max risk scores of security incidents at the time of calculation.

-   **Get Max Risk Score for Misconfigurations Test Results**

    This indicator is calculated daily. It considers the maximum risk scores for misconfiguration of test results at the time of calculation.

-   **Get Avg Risk Score for Misconfiguration Test Results**

    This indicator is calculated daily. It considers the average risk scores for misconfiguration of test results at the time of calculation.

-   **Number of open security incidents**

    This indicator is calculated daily. It considers open security incidents at the time of calculation.

-   **Phishing Overview**

    This indicator is calculated daily. It considers the count of Security Simulation Metrics at the time of calculation.

-   **Aggregate MTTR**

    Calculates the average time taken to close vulnerabilities \(hosts, containers, and applications\) and the time taken to close the test results in days. \[\[Host SLA - Closed\]\] + \[\[Application SLA - Closed\]\] + \[\[Container SLA - Closed\]\] + \[\[Test Result SLA - Passed\]\]\) / \(\[\[Host SLA - Closed Count\]\] + \[\[Application SLA - Closed Count\]\] + \[\[Test Result SLA - Passed Count\]\] + \[\[Container SLA - Closed Count\]\]\)

-   **Current Scan Coverage**

    Calculates the percentage by utilizing the ratio between the number of items scanned and the total number of items eligible for scanning during the same period. var scannedItems =\[\[Scanned Assets\]\];var scannableItems = \[\[Scannable Assets\]\];var res;if \(scannedItems == 0\)res = 0;elseres = scannedItems / scannableItems \* 100;if \(res &gt; 100\)res = 100;res;

-   **Average Age of Active Vulnerable Items**

    Calculates the average age of all active vulnerable items \(hosts, containers, and applications\) in days. \(\[\[Summed Age of Vulnerable Items\]\] + \[\[Summed Age of Application Vulnerable Items\]\] + \[\[Summed Age of Container Vulnerable Items\]\]\) / \(\[\[Vulnerable Items\]\] + \[\[Application Vulnerable Items\]\] + \[\[Container Vulnerable Items\]\]\)

-   **Active VITs by age and risk rating**

    Calculates the total count of all active vulnerable items \(hosts, containers, and applications\) categorized by their age and level of risk assessment. \[\[Open Vulnerable Items\]\] + \[\[Open Container Vulnerable Items\]\] + \[\[Open Application Vulnerable Items\]\]

-   **Deferred Issues**

    Calculates the total count of all vulnerable items \(hosts, containers, applications, and test results\) with the state as 'Deferred'. \[\[Deferred VITs\]\] + \[\[Deferred AVITs\]\] + \[\[Deferred Test Results\]\] + \[\[Deferred CVITs\]\]

-   **Average resolution time of closed security incidents**

    Calculates the average time taken to close the security incidents in days. \(\[\[Summed duration of closed security incidents\]\] / \[\[Number of closed security incidents\]\]\) /24

-   **Security Score**

    Calculates the overall security ratings daily. It’s calculated based on the rolled up risk score. var secPostureRating = 100 - \[\[Security score\]\]; secPostureRating;

-   **Security Score \(Business Units\)**

    Calculates the final rolled up risk score where the roll-up risk score of vulnerable items, misconfigurations, security incidents, and major security incidents are multiplied with the respective weights that are fetched from the security posture roll-up table. var numMajorIncidents = \[\[Number of Open Major Security Incidents\]\], majorSIRiskScore, rollUpRiskScore; if\(numMajorIncidents &gt; 0\) majorSIRiskScore = 100; else majorSIRiskScore = 0; rollUpRiskScore = \(\[\[Vulnerability and Misconfiguration Rolled up Risk Score\]\] \* 20 + \[\[OT Vulnerability Rolled up Risk Score\]\] \* 20 + \[\[Get Max Risk Score for SI Incidents\]\] \* 20 + majorSIRiskScore \* 40\)/100; rollUpRiskScore;

-   **Security Score \(Business Services\)**

    Calculates the final rolled up risk score where the roll-up risk score of vulnerable items, misconfigurations, security incidents, and major security incidents are multiplied with the respective weights that are fetched from the security posture roll-up table. var numMajorIncidents = \[\[Number of Open Major Security Incidents - Services\]\], majorSIRiskScore, rollUpRiskScore; if\(numMajorIncidents &gt; 0\) majorSIRiskScore = 100; else majorSIRiskScore = 0; rollUpRiskScore = \(\[\[Vulnerability and Misconfiguration Rolled up Risk Score - Services\]\] \* 20 + \[\[OT Vulnerability Rolled up Risk Score - Services\]\] \* 20 + \[\[Get Max Risk Score for SI Incidents - Services\]\] \* 20 + majorSIRiskScore \* 40\)/100; rollUpRiskScore;

-   **Vulnerability Rolled up Risk Score**

    Calculates the vulnerability rolled up risk score where the max risk score, average risk score of vulnerable items and count of vulnerable items are multiplied with their respective weights. var maxRiskScore = 100; var count = \[\[Active VITs by age and risk rating\]\]; var countRiskScore; if \(0 == count\) countRiskScore = 0; else if \(count &gt; 10000\) countRiskScore = maxRiskScore; else if \(count &gt; 1000\) countRiskScore = \(maxRiskScore \* 0.80\); else if \(count &gt; 100\) countRiskScore = \(maxRiskScore \* 0.60\); else if \(count &gt; 10\) countRiskScore = \(maxRiskScore \* 0.40\); else countRiskScore = \(maxRiskScore \* 0.20\); var vulRiskScore = \(\[\[Get Max Score form all Vulnerable Items\]\] \* 0 + \[\[Average Risk Score of all Vulnerable Items\]\] \* 100 + countRiskScore \* 0\)/100; vulRiskScore;

-   **Get Max Score from all Vulnerable Items**

    Calculates the vulnerability rolled up risk score where the max risk score, average risk score of vulnerable items and count of vulnerable items are multiplied with their respective weights. var maxScoreForVI = \[\[Get Max Risk Score for Vulnerable Items\]\], maxScoreForCVI = \[\[Get Max Risk Score for Container Vulnerable Item\]\], maxScoreForAVI = \[\[Get Max Risk Score for Application Vulnerable Items\]\], maxScore; if \(maxScoreForVI &gt;= maxScoreForCVI &amp;&amp; maxScoreForVI &gt;= maxScoreForAVI\) maxScore = maxScoreForVI; else if \(maxScoreForCVI &gt;= maxScoreForVI &amp;&amp; maxScoreForCVI &gt;= maxScoreForAVI \) maxScore = maxScoreForCVI; else maxScore = maxScoreForAVI; maxScore;

-   **Average Risk Score of all Vulnerable Items**

    Calculates the average risk score from all vulnerable items \(hosts, containers, and applications\). var summedRiskScore = \[\[Summed Risk Score of VITs\]\] + \[\[Summed Risk Score of AVIs\]\] + \[\[Summed Risk Score of CVIs\]\], avgRiskScore; var totalVulCount = \[\[Open Vulnerable Items\]\] + \[\[Open Application Vulnerable Items\]\] + \[\[Open Container Vulnerable Items\]\]; if\(summedRiskScore == 0\) avgRiskScore = 0; else if\(totalVulCount .=0 \) avgRiskScore = summedRiskScore / totalVulCount; avgRiskScore;

-   **Misconfiguration Rolled up Risk Score**

    Calculates the misconfiguration rolled up risk score using the test outcomes categorized as Failed, Error, or Unknown. var maxRiskScore = 100; var count = \[\[Open Config Issues - Test results\]\]; var countRiskScore; if \(0 == count\) countRiskScore = 0; else if \(count &gt; 10000\) countRiskScore = maxRiskScore; else if \(count &gt; 1000\) countRiskScore = \(maxRiskScore \* 0.80\); else if \(count &gt; 100\) countRiskScore = \(maxRiskScore \* 0.60\); else if \(count &gt; 10\) countRiskScore = \(maxRiskScore \* 0.40\); else countRiskScore = \(maxRiskScore \* 0.20\); var misRiskScore = \(\[\[Get Max Risk Score for Misconfigurations Test Results\]\] \* 0 + \[\[Get Avg Risk Score for Misconfiguration test results\]\] \* 100 + countRiskScore \* 0\)/100; misRiskScore;

-   **Average Time to Eradicate**

    Calculates the average time taken to eradicate security incidents in days \[\[SI - Average Duration Time &gt; Security Incident State = Eradicate\]\] / 1440

-   **Average Time to Identify**

    Calculates the average time taken to identify security incidents in days. \[\[SI - Average Time To Identify\]\] / 1440

-   **Average Time to Contain**

    Calculates the average time taken to contain security incidents in days. \[\[SI - Average Duration Time &gt; Security Incident State = Contain\]\] / 1440

-   **Remediation Target Adherence**

    Calculates the monthly percentage of remediation target adherence from test results, vulnerable items, container vulnerable items, and application vulnerable items. The target adherence is determined by the number of items that have fulfilled the set target. \(\[\[Test Result SLA - Passed Count &gt; Remediation status \(unified\) = Target Met\]\] + \[\[Container SLA - Closed Count &gt; Remediation status \(unified\) = Target Met\]\] + \[\[Application SLA - Closed Count &gt; Remediation status \(unified\) = Target Met\]\] + \[\[Host SLA - Closed Count &gt; Remediation status \(unified\) = Target Met\]\]\) / \(\[\[Test Result SLA - Passed Count\]\] + \[\[Container SLA - Closed Count\]\] + \[\[Application SLA - Closed Count\]\] + \[\[Host SLA - Closed Count\]\]\) \* 100

-   **Monthly Remediation Efficiency \(All Vulnerable Items\)**

    Calculates the monthly percentage of closed vulnerable items, containers vulnerable items, and application vulnerable items in contrast to newly identified ones. var closedItems = \[\[Host SLA - Closed Count\]\] + \[\[Container SLA - Closed Count\]\] + \[\[Application SLA - Closed Count\]\] + \[\[Test Result SLA - Passed Count\]\];

    var newItems = \[\[Host VITs opened/reopened yesterday\]\] + \[\[Container VITs opened/reopened yesterday\]\] + \[\[Application VITs opened/reopened yesterday\]\] + \[\[Test results opened/reopened yesterday\]\];

    var res = 0;if \(closedItems == 0\) res = 0;else if \(newItems .=0\)res = closedItems / newItems \* 100;if \(res &gt; 1000\) res = 1000; res;

-   **Host VITs opened/reopened yesterday**

    This indicator is calculated daily. It considers the host vulnerable items that were last opened on the previous day at the time of calculation.

-   **Application VITs opened/reopened yesterday**

    This indicator is calculated daily. It considers the application vulnerable items that were last opened on the previous day at the time of calculation.

-   **Container VITs opened/reopened yesterday**

    This indicator is calculated daily. It considers the container vulnerable items that were last opened on the previous day at the time of calculation.

-   **Test results opened/reopened yesterday**

    This indicator is calculated daily. It considers the test results that were last seen on the previous day at the time of calculation.

-   **OT Vulnerable Items**

    This indicator is calculated daily. It considers active OT vulnerable items present at the time of calculation.

-   **OT Summed Duration of Closed Vulnerable**

    This indicator is calculated daily. It considers the total age of all OT vulnerabilities that are closed on the day of calculation.

-   **OT Closed Vulnerable Items**

    This indicator is calculated daily. It considers the OT vulnerable items that are closed on the day of calculation.

-   **Average age of OT active vulnerable items**

    Calculates the average age of OT vulnerable items \(\[\[Summed age of OT vulnerable Items\]\] / \[\[OT Vulnerable Items\]\]\)


## Breakdowns

-   Business Unit
-   Business Services
-   Risk Rating
-   Age Range
-   Assignment Group \(unified\)
-   Remediation Target Status \(Closed\)
-   Asset Class
-   Asset Category
-   Risk Rating \(unified\)
-   Deferred Reason \(unified\)
-   Security Incident State
-   Security Incident Priority
-   Security Incident Category
-   Phishing Event
-   Deferred Reason Non Closed \(unified\)

## Applications to activate

You must activate the following applications to populate the score in the widgets. Based on the application you’re using, you must activate the dependent applications.

<table id="table_yds_cg5_21c"><thead><tr><th>

If you’re using

</th><th>

Activate

</th></tr></thead><tbody><tr><td>

Vulnerability Response

</td><td>

-   Performance Analytics for Vulnerability Response
-   Vulnerability Response Common
-   Vulnerability Response
-   Vulnerability Response and Configuration Compliance for Containers
-   Configuration Compliance

</td></tr><tr><td>

Operational Technology

</td><td>

Vulnerability Response for Operational Technology

</td></tr><tr><td>

Phishing Integrations

</td><td>

-   Security Simulation and Training Integration for SecOps
-   KnowBe4 Integration for SecOps
-   Microsoft Defender for Office365 Integration for SecOps

</td></tr><tr><td>

Security Incident Response

</td><td>

-   Performance Analytics for Security Incident Response
-   Security Incident Response
-   Major Security Incident Management

</td></tr><tr><td>

Governance, Risk, and Compliance

</td><td>

-   GRC: Common Dashboard Elements
-   GRC: Risk Management Workspace
-   GRC: Advanced Risk
-   GRC: Compliance Management Workspace

</td></tr></tbody>
</table>## Scheduled jobs for data collection

The following scheduled jobs are run to collect scores on new data automatically.

|Scheduled job|Frequency|Description|
|-------------|---------|-----------|
|Upload the benchmark scores|On Demand|Collects scores from the instance and posts to the central instance. The benchmark algorithms calculate the industry's best scores.|
|Download the benchmark scores|On Demand|Downloads the benchmark scores. It’s available in the Benchmark Scores \[sn\_bm\_client\_score\_list\] table.|

