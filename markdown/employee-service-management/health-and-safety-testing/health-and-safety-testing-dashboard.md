---
title: Health and Safety Testing dashboard
description: Use the Health and Safety Testing dashboard to gain insight on the health of your users with reports detailing testing trends, the types of tests performed, and approvals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/health-and-safety-testing/health-and-safety-testing-dashboard.html
release: australia
product: Health and Safety Testing
classification: health-and-safety-testing
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Health and Safety Testing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Health and Safety Testing dashboard

Use the Health and Safety Testing dashboard to gain insight on the health of your users with reports detailing testing trends, the types of tests performed, and approvals.

To access the Health and Safety Testing dashboard, navigate to **Self-Service** &gt; **Dashboards**.

\[Omitted image "health-testing-dashboard.png"\] Alt text: Testing Status dashboard

## End user and goals

<table id="table_snk_rcb_3sb"><thead><tr><th>

End user and goal

</th><th>

Required role

</th><th>

Benefits

</th></tr></thead><tbody><tr><td>

Health and Safety Testing manager or administrator: Needs an overview of the organization's testing status. They might want to see the frequency of tests, the number of results being reported each month approved, the authenticity of the tests, and what types of tests are being reported.

</td><td>

-   Administrator: sn\_imt\_health\_test.admin
-   Manager: sn\_imt\_health\_test.testing\_admin
-   \(Optional\) sn\_imt\_core.admin

**Note:** The sn\_imt\_core.admin role is not required but users with that role can review some of the reports. Users with only the sn\_imt\_health\_test.testing\_admin role are unable to view the Test Results by Result Type and Test Approvals with Approved or Reject Status reports


</td><td>

-   Review the number of health test results by type
-   Monitor and compare the number of test results that have been approved or rejected
-   Monitor your organization's monthly testing rate
-   Monitor the monthly number of test results reported

</td></tr><tr><td>

Employee Readiness Core admin: Needs an at-a-glance view of the organization's testing rate and the number of results reported to help determine employee readiness.

</td><td>

sn\_imt\_core.admin

</td><td>

-   Monitor your organization's monthly testing rate
-   Monitor the monthly number of test results reported

</td></tr></tbody>
</table>## Data visualizations

|Title|Type|Description|
|-----|----|-----------|
|Test Results by Result Type|Pie breakdown \[Omitted image "pie-breakdown-wthoutlabel.png"\] Alt text: Pie breakdown icon|A breakdown of the test results in your organization by the result \(positive, negative, and inconclusive\).|
|Test Approvals with Approved or Rejected Status|Pie breakdown \[Omitted image "pie-breakdown-wthoutlabel.png"\] Alt text: Pie breakdown icon|The number of test results in your organization that have been either approved or rejected.|
|Employee Testing Rate \(Monthly\)|Line\[Omitted image "line-icon.png"\] Alt text: Line icon|Testing rate of users in your organization for the month.|
|Test Results \(Monthly\)|Stacked bar chart\[Omitted image "stacked-bar-chart.png"\] Alt text: Stacked bar chart icon|The monthly number of test results reported \(positive, negative, and inconclusive\).|

**Parent Topic:**[Health and Safety Testing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/health-and-safety-testing/health-safety-testing.md)

