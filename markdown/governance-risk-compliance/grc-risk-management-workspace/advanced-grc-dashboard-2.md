---
title: Advanced Governance, Risk, and Compliance Application Risk dashboard
description: The GRC Application Risk and Compliance Overview Dashboard provides the latest view of risk and compliance aspects for the business applications that are used in an enterprise.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Analytics and reporting solutions for Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# Advanced Governance, Risk, and Compliance Application Risk dashboard

The GRC **Application Risk and Compliance Overview Dashboard** provides the latest view of risk and compliance aspects for the business applications that are used in an enterprise.

The Application Risk Dashboard is useful for the Chief Information Officer \(CIO\) and application owners. Both these users must have the sn\_compliance.reader, sn\_risk.reader, and sn\_audit.user roles to view the dashboard. Navigate to **Advanced GRC Dashboard** &gt; **Application Risk Dashboard**. The **Application Risk and Compliance Overview Dashboard** is displayed.

**Note:** To be able to view this dashboard, you must activate the GRC: Advanced Dashboards \(com.sn\_grc\_pa\_advanced\) plugin and the GRC: Policy and Compliance Management \(sn\_compliance\) plugin.

The Application Risk and Compliance Overview dashboard provides you a detailed report of the risk and compliance posture of all the business applications in an organization.

![Advanced GRC application risk dashboard](../image/advanced-grc-dashboard.png "Application Risk and Compliance Dashboard")

This dashboard highlights the following:

-   The compliance impact of applications in use.
-   The risk posture of applications.
-   The state of remediation and exceptions activity of the issues.
-   The audit activity around applications and status.

This dashboard provides answers to the following questions that are of interest to the CIO and the application owner:

1.  What are the key applications, and are they all operational and delivering the required services optimally?
2.  What are the policies and authority documents that the applications must be compliant to? Are the applications compliant to them?
3.  What are the risks faced by the applications? Are any of them high to raise a concern? Are there enough mitigations in place? Are there adequate controls in place and are they working effectively?
4.  For applications that need remediation, are the remediations being done on time according to the Service Level Agreements \(SLAs\)? Which are the applications that generate the maximum number of issues?
5.  Are exceptions being sought often on the applications and why? Are they within manageable limits?
6.  Are the applications due for audit any time? How have the applications performed on these audits?

The dashboard offers various representations such as bar graphs, donut charts, and trend charts. Application owners can use various filters on the dashboard to view reports related to the business applications they own such as, critical business applications, mandated controls related to specific business application, or high priority issues and so on.

## Compliance Overview

The Compliance Overview tab appears when you activate the Policy and Compliance plugin. The Compliance Overview tab provides an overview of the compliance posture of the business applications and displays the following reports:

-   Total Controls: This report provides the total number of active controls.
-   Compliant Controls: This report provides the total number of compliant controls which are not in draft or retired state.
-   Non-Compliant Controls: This report provides the total number of non-compliant controls which are not in draft or retired state.
-   Compliance Status By Month: This report provides the number of active controls by month.

    **Note:** This bar chart shows the compliance status for the current month and can be grouped by either Control Status or Business Application.

-   Compliance %: This report provides the percentage of different statuses of active controls such as Compliant, Non Compliant, and Not Applicable.
-   Application Compliance Summary: This report provides the summary of policies, authority documents, and the controls associated with business applications.

The following filters can be used to filter data on the reports:

-   Business Application
-   Business Criticality
-   Entity Owner
-   Enforcement such as mandatory or voluntary controls
-   Key Control
-   Control State
-   Control Owning Group

## Risk Overview

The Risk Overview tab appears when you activate the Advanced Risk plugin. The Risk Overview tab provides an overview of the risks associated with business applications and displays the following reports:

-   Risk Heatmap by Application Criticality: This report displays the heatmap of the application risks based on criticality of applications versus the risk rating of the application.
-   Risk Response Tasks Overview: This report displays the response tasks created for a risk and different states of those tasks.

    **Note:** This bar chart can be grouped by and stacked by risk response, risk response state, risk calculated score, risk response assigned to, or business application.

-   Application Risk Summary: This report displays the summary of risks directly associated with the applications that contribute to the overall risk rating of the application. Other downstream risks that contribute to the application risk rating are not represented in this report. The risks considered for this report are very high, high, and moderate.
-   Application Risk Mitigating Controls Status: This report provides the information for an application's risks and the associated controls. The risks considered for this report are very high, high, and moderate. The state of controls must not be in draft or retired. The risks for only one year are displayed.

The following filters can be used to filter data on the reports:

-   Business Application
-   Criticality
-   Risk Rating
-   Application Owner
-   Business Owner

## Risk Posture

The Risk Posture tab appears when you activate the Risk plugin. The Risk Posture tab provides information about the risk exposure of business applications. The reports in this tab can also be filtered using the Business Application filter. The Risk Posture tab displays the following:

-   Very High Risks: This report displays the very high risks of an application.
-   High Risks: This report displays the high risks of an application.
-   Moderate Risks: This report displays the moderate risks of an application.
-   Acceptance Task Expirations: This report displays the risk response acceptance tasks that have an expiration on the current day, the current week, the current month, the current quarter, and the current year.
-   Contributing Risks Trend: This report displays the trend of risks directly associated with business applications and how they are performing over a period. Other downstream risks that contribute to the application risk rating are not represented in this report.

## Audit Overview

The Audit Overview tab appears when you activate the Audit plugin. The Audit Overview tab provides an overview of audit and audit activities related to business applications and displays the following reports:

-   Open Audit Engagements: This report displays the number of audit engagements in open state.
-   Ineffective Controls: This report displays the number of ineffective controls for an audit engagement.
-   Open Issues: This report displays the number of open issues for an audit engagement.
-   Past Due Issues: This report displays the number of past due audit issues for an application.
-   Upcoming Audit Engagements: This report displays the monthly count for the upcoming audit engagements.
-   Open Issues by Audit Engagements: This report displays the monthly count for the open audit issues.
-   Past Due Issues by Audit Engagements: This report displays the past due audit issues over a period.
-   Ineffective Controls by Audit Engagements: This report displays the information regarding audit engagements and the associated ineffective controls.

The following filters can be used to filter data on the reports:

-   Business Application
-   Audit Engagement
-   Criticality

## Policy Exceptions Overview

The Policy Exceptions Overview tab appears when you activate the Policy and Compliance plugin. The Policy Exception Overview tab provides information about policy exceptions requested for business applications. The data displayed in the Policy Exceptions Overview tab can be filtered using the Business Application filter. This tab displays the following reports:

-   New Exceptions: This report provides information about the new exceptions requested.
-   Approved Exceptions: This report provides information about the number of approved exceptions.
-   Rejected Exceptions: This report provides information about the number of rejected exceptions.
-   Expired Exceptions: This report provides information about the number of expired exceptions.
-   Exceptions Awaiting Approval: This report provides information about the exceptions that are awaiting approval and are due on the current date, the current week, the current month, and the current quarter.
-   Extensions Awaiting Approval: This report provides information about the extensions that are awaiting approval and are due on the current date, the current week, the current month, and the current quarter
-   Upcoming Exceptions Expirations: This report provides information about the exceptions that are about to expire and which are due on the current date, the day after the current date, the current week, the week after the current week, and the current month.
-   Exceptions Requested vs. Approved: This report provides information about the exceptions requested versus the number of exceptions approved per month.

## Issues Overview

The Issues Overview tab appears when you activate either the Risk Management plugin or the Policy and Compliance Management plugin. The Issues Overview tab provides information about the various compliance and risk issues associated with business applications. The data displayed in the Issues Overview tab can be filtered using the Business Application filter. This tab displays the following reports:

-   Open Issues: This report displays the number of issues in open state.
-   Critical Priority Issues: This report displays the number of critical priority issues.
-   High Priority Issues: This report displays the number of high priority issues.
-   Accepted Issues: This report displays the number of issues that are accepted.
-   Past Due Issues: This report displays the number of past due issues.
-   Issues to be Resolved: This report displays the number of issues that must be resolved on the current date, the current week, current month, current quarter, and current year.
-   Remediation Tasks to be Completed: This report displays the number of remediation tasks that must be completed on the current date, the current week, current month, current quarter, and current year.
-   Past Due Issues: This report displays the number of past due issues over a time period.
-   Past Due Remediation Tasks: This report displays the number of past due remediation tasks over a time period.
-   Issue Creation Trend: This report displays the trend of how issues are created over a time period.
-   Issue Closure Trend: This report displays the trend of how issues are closed over a time period.
-   Remediation Task Creation Trend: This report displays the trend of how remediation tasks are created over a period.
-   Remediation Task Closure Trend: This report displays the trend of how remediation tasks are closed over a period.

**Parent Topic:**[Analytics and reporting solutions for Risk Management](../../../use/dashboards/application-content-packs/grc-risk-mgmt-content-pack.md)

**Parent Topic:**[Common Governance, Risk, and Compliance features](common-grc-features.md)

