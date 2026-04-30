---
title: Application Risk and Compliance Overview dashboard
description: The Application Risk and Compliance Overview dashboard provides the current view of risk and compliance posture for the business applications that are used in an enterprise. You can now view the dashboard in Next Experience UI Framework.
locale: en-US
release: xanadu
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Analytics and Reporting solutions for GRC: Policy and Compliance Management, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Application Risk and Compliance Overview dashboard

The Application Risk and Compliance Overview dashboard provides the current view of risk and compliance posture for the business applications that are used in an enterprise. You can now view the dashboard in Next Experience UI Framework.

**Important:** Starting with version 18.1.0 of the Policy and Compliance Management application, the Application Risk and Compliance Overview dashboard is available in the Next Experience UI Framework.

If you are on Vancouver or Washington DC, you can view the dashboard in the Next Experience UI Framework.

![Application Risk and Compliance Overview dashboard in the Next Experience UI Framework.](../image/app-risk-compl-overvvw-pa-db-pc.png "Application Risk and Compliance Overview dashboard in the Next Experience UI Framework")

## Required ServiceNow AI Platform roles

-   Admin \(sn\_grc.admin\), to provide admin rights and edit the reports in the dashboard.
-   Reader \(sn\_grc.reader\), to view the reports in the dashboard.

## Access the Application Risk and Compliance Overview dashboard

To open the dashboard, navigate to **All** &gt; **Advanced GRC Dashboards** &gt; **Analytics Application Risk Dashboard**.

## Reports

-   The Compliance Overview tab appears when you activate the Policy and Compliance plugin. The tab provides an overview of the compliance posture of the business applications.
-   The Risk Overview tab appears when you activate the Advanced Risk plugin. The tab provides an overview of the risks associated with business applications.
-   The Risk Posture tab appears when you activate the Risk plugin. The tab provides information about the risk exposure of business applications. The reports in this tab can also be filtered using the Business Application filter.
-   The Audit Overview tab appears when you activate the Audit plugin. The tab provides an overview of audit and audit activities related to business applications.
-   The Policy Exceptions Overview tab appears when you activate the Policy and Compliance plugin. The tab provides information about policy exceptions requested for business applications. The data displayed in the Policy Exceptions Overview tab can be filtered using the Business Application filter.
-   The Issues Overview tab appears when you activate either the Risk Management plugin or the Policy and Compliance Management plugin. The tab provides information about the various compliance and risk issues associated with business applications. The data displayed in the Issues Overview tab can be filtered using the Business Application filter.

|Title|Description|
|-----|-----------|
|Compliance Overview tab|
|Total Controls|Provides the total number of active controls.|
|Compliant Controls|Provides the total number of compliant controls which are not in draft or retired state.|
|Non-Compliant Controls|Provides the total number of non-compliant controls which are not in draft or retired state.|
|Compliance Status By Month|Provides the number of active controls by month. This bar chart shows the compliance status for the current month and can be grouped by either Control Status or Business Application.|
|Compliance %|Provides the percentage of different statuses of active controls such as Compliant, Non Compliant, and Not Applicable.|
|Application Compliance Summary|Provides the summary of policies, authority documents, and the controls associated with business applications.|
|Risk Overview tab|
|Risk Heatmap by Application Criticality|Displays the heatmap of the application risks based on the criticality of applications versus the risk rating of the application.|
|Risk Response Tasks Overview|Displays the response tasks created for a risk and different states of those tasks. This bar chart can be grouped and stacked by risk response, risk response state, risk calculated score, risk response assigned to, or business application.|
|Application Risk Summary|Displays the summary of risks directly associated with the applications that contribute to the overall risk rating of the application. Other downstream risks that contribute to the application risk rating are not represented in this report. The risks considered for this report are very high, high, and moderate.|
|Application Risk Mitigating Controls Status|Provides the information for an application's risks and the associated controls. The risks considered for this report are very high, high, and moderate. The state of controls must not be in draft or retired. The risks for only one year are displayed.|
|Risk Posture tab|
|Very High Risks|Displays the very high risks of an application.|
|High Risks|Displays the high risks of an application.|
|Moderate Risks|Displays the moderate risks of an application.|
|Acceptance Task Expirations|Displays the risk response acceptance tasks that have an expiration on the current day, the current week, the current month, the current quarter, and the current year.|
|Contributing Risks Trend|Displays the trend of risks directly associated with business applications and how they are performing over a period. Other downstream risks that contribute to the application risk rating are not represented in this report.|
|Audit Overview tab|
|Open Audit Engagements|Displays the number of audit engagements in open state.|
|Ineffective Controls|Displays the number of ineffective controls for an audit engagement.|
|Open Issues|Displays the number of open issues for an audit engagement.|
|Past Due Issues|Displays the number of past due audit issues for an application.|
|Upcoming Audit Engagements|Displays the monthly count for the upcoming audit engagements.|
|Open Issues by Audit Engagements|Displays the monthly count for the open audit issues.|
|Past Due Issues by Audit Engagements|Displays the past due audit issues over a period.|
|Ineffective Controls by Audit Engagements|Displays the information regarding audit engagements and the associated ineffective controls.|
|Policy Exceptions Overview tab|
|New Exceptions|Provides information about the new exceptions requested.|
|Approved Exceptions|Provides information about the number of approved exceptions.|
|Rejected Exceptions|Provides information about the number of rejected exceptions.|
|Expired Exceptions|Provides information about the number of expired exceptions.|
|Exceptions Awaiting Approval|Provides information about the exceptions that are awaiting approval and are due on the current date, the current week, the current month, and the current quarter.|
|Extensions Awaiting Approval|Provides information about the extensions that are awaiting approval and are due on the current date, the current week, the current month, and the current quarter.|
|Upcoming Exceptions Expirations|Provides information about the exceptions that are about to expire and which are due on the current date, the day after the current date, the current week, the week after the current week, and the current month.|
|Exceptions Requested vs. Approved|Provides information about the exceptions requested versus the number of exceptions approved per month.|
|Issues Overview tab|
|Open Issues|Displays the number of issues in open state.|
|Critical Priority Issues|Displays the number of critical priority issues.|
|High Priority Issues|Displays the number of high priority issues.|
|Accepted Issues|Displays the number of issues that are accepted.|
|Past Due Issues|Displays the number of past due issues.|
|Issues to be Resolved|Displays the number of issues that must be resolved on the current date, current week, current month, current quarter, and current year.|
|Remediation Tasks to be Completed|Displays the number of remediation tasks that must be completed on the current date, current week, current month, current quarter, and current year.|
|Past Due Issues|Displays the number of past due issues over a time period.|
|Past Due Remediation Tasks|Displays the number of past due remediation tasks over a time period.|
|Issue Creation Trend|Displays the trend of how issues are created over a time period.|
|Issue Closure Trend|Displays the trend of how issues are closed over a time period.|
|Remediation Task Creation Trend|Displays the trend of how remediation tasks are created over a period.|
|Remediation Task Closure Trend|Displays the trend of how remediation tasks are closed over a period.|

## Filters

<table id="table_e15_vms_gbc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Compliance Overview tab

</td><td>

Filters used to filter data on the reports available from the Compliance Overview tab are:-   Business Application
-   Business Criticality
-   Entity Owner
-   Enforcement such as mandatory or voluntary controls
-   Key Control
-   Control State
-   Control Owning Group

</td></tr><tr><td>

Risk Overview tab

</td><td>

Filters used to filter data on the reports available from the Risk Overview tab are:-   Business Application
-   Criticality
-   Risk Rating
-   Application Owner
-   Business Owner

</td></tr><tr><td>

Audit Overview tab

</td><td>

Filters used to filter data on the reports available from the Audit Overview tab are:-   Business Application
-   Audit Engagement
-   Criticality

</td></tr></tbody>
</table>**Parent Topic:**[Analytics and Reporting solutions for GRC: Policy and Compliance Management](grc-policy-compliance-content-pack.md)

