---
title: Proactive Code Check analytics
description: Platform Owners use Proactive Code Check to track compliance against coding best practices and organizational standards. Owners can review detailed findings and audit the status of issues that were uncovered during the scan. Historical data is available up to six months.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-02-12"
reading_time_minutes: 1
breadcrumb: [Impact Proactive Code Check, Impact Platform Health, Using Impact Store Application, Impact Store Application, Impact]
---

# Proactive Code Check analytics

Platform Owners use Proactive Code Check to track compliance against coding best practices and organizational standards. Owners can review detailed findings and audit the status of issues that were uncovered during the scan. Historical data is available up to six months.

## About this task

-   Identify recurring issues and trends in unresolved findings.
-   View progress on resolving technical debt over time.
-   Prioritize remediation efforts using a severity-based categorization of findings.

## Before you begin

Role required: Impact\_platform\_owner, sn.mif\_mif\_read

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Platform health** &gt; **Diagnostics**.

    The Proactive Code Check overview displays with data from the last 30 days.

    ![The PCC analytics page with findings summaries displayed.](../image/pcc-analytics.png)

2.  Select **View Dashboard** to view additional information about the scans.

    -   Filter by instances or by time period.
    -   The Prevented findings charts display metrics related to findings that were resolved prior to moving an update set to a production completed status.![Chart of the findings that were prevented in non-production update sets.](../image/pcc-dashboard-prevented-findings.png)
    -   The Unresolved findings section displays metrics related to findings that remained open after an update set was moved to a production completed status.![Chart of the findings that were unresolved in non-production update sets.](../image/pcc-dashboard-unresolved-findings.png)
    -   Compare Trends in Resolved vs. Unresolved Findings.
3.  Select **View all findings** to view all findings related to Proactive Code Check.

    ![List of all findings detected.](../image/pcc-all-findings-table.png)

    -   View All Findings Across Instances.
    -   Filter and Group Findings by Severity, Type, or Check.
    -   Identify Checks Producing the Most Findings for Targeted Improvements.
    -   Analyze Findings Across Time Periods to Track Trends and Recurring Issues.

        |Findings category|State|
        |-----------------|-----|
        |Count of Findings \(Findings Resolved\)|Muted and Created on Today|
        |Count of Findings Unresolved|Recurring or New and Updated on Today|
        |Count of Findings Resolved|Resolved and Updated on Today|
        |Count of Findings New|New and Updated on Today|
        |Count of Findings Muted|Muted and Updated on Today|


**Parent Topic:**[Impact Proactive Code Check](proactive-code-check.md)

