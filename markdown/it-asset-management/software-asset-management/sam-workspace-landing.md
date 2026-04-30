---
title: Software asset overview
description: Enhance your software asset management experience by using the modernized and user-friendly software asset overview view. The software asset overview is a simplified and intuitive environment that helps you use the application more effectively by reducing complexity.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Software asset overview

Enhance your software asset management experience by using the modernized and user-friendly software asset overview view. The software asset overview is a simplified and intuitive environment that helps you use the application more effectively by reducing complexity.

Use the software asset overview view to:

-   Gain insights into key metrics such as compliance trends, true-up costs, potential savings, normalization rates.
-   Execute routine tasks such as running reconciliation or creating entitlements.
-   Configure Microsoft SQL Server and Microsoft Windows Server on your ServiceNow instance through the Guided Setup. For more information, see [Software Asset Management Guided Experiences](playbook-entitlementsetup-workspace.md).
-   Get actionable insights into your software assets via alerts and notifications.
-   Sort by product or publisher to narrow down your results.
-   Filter by Published status to view reports and dashboards only related to the software products that you manage in a phase-wise implementation of Software Asset Management.

    **Note:** The Published status filter is shown only when the system property com.snc.samp.manage.published.products is enabled on your ServiceNow instance. By default, this filter is set to **Published** and the following reports show details of published products:

    -   Publishers out of compliance
    -   Products out of compliance
    -   Over-licensed amount
    -   Total true-up cost
    -   Top 5 publishers true-up cost
    -   Software spend
    However, you can also view reports related to the products that aren't published by setting this filter to **Unpublished**. To view reports related to all the products, clear the Published status filter.


![Software asset overview landing page](../image/asset-overview-workspace.png "Software asset overview view")

Select any widget to view detailed information. All the widgets are updated whenever a new reconciliation result is available.

To narrow down your results, you can filter the workspace by publisher or product.

**Note:** If you select more than one publisher in the filter and then select the **Publishers out of compliance** widget, all non-compliant publishers are listed. The same is true for products.

<table id="table_vgl_c3y_tz"><thead><tr><th>

Report

</th><th>

Source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Publishers out of compliance

</td><td>

Product Results \[samp\_product\_result\]

</td><td>

The number of publishers that have at least one software model out of compliance.Select the report to view the results in the License usage view.

</td></tr><tr><td>

Products out of compliance

</td><td>

Product Results \[samp\_product\_result\]

</td><td>

The number of products that have at least one software model out of compliance.Select the report to view the results in the License usage view.

</td></tr><tr><td>

Over-licensed amount

</td><td>

Product Results \[samp\_product\_result\]

</td><td>

Cost of licenses owned but not being used.

</td></tr><tr><td>

Expiring maintenance and subscription

</td><td>

Software Entitlement \[alm\_license\]

</td><td>

End date of the total sum of all entitlements that are going to expire within 6 months.

 The total sum of entitlements includes:

-   Perpetual
-   Maintenance
-   Perpetual + Maintenance
-   Upgrade
-   SA
-   Perpetual +SA
-   Step-up

 Select the report to view details about the specific entitlements that are going to expire.

**Note:** Maintenance and SA entitlements aren’t displayed as the Perpetual entitlements associated with them are displayed.

</td></tr><tr><td>

Total true-up Cost

</td><td>

Product Results\[samp\_product\_result\]

</td><td>

Cost to be compliant based on the average prices in entitlements for the rights by publisher.

</td></tr><tr><td>

Top 5 publishers true-up cost

</td><td>

Product Results\[samp\_product\_result\]

</td><td>

The top 5 publishers illustrated in a pie chart in order of true-up cost.

</td></tr><tr><td>

Potential Savings

</td><td>

Product Results\[samp\_product\_result\]

</td><td>

Cost saved if removal candidates are reclaimed.Hover on the donut chart to view the number of removal candidates for a specific justification along with the cost. Removal candidates are grouped by justification. Select on a justification on the donut chart to take you to the list of removal candidates with that specific justification.

</td></tr><tr><td>

Actual savings

</td><td>

Reclamation Candidate\[samp\_sw\_reclamation\_candidate\]

</td><td>

Sum of potential savings in a given month of closed complete removal candidates.

</td></tr><tr><td>

Software Spend

</td><td>

License Metric Results\[samp\_license\_metric\_result\]

</td><td>

Total software cost of all entitlements that aren’t retired.

</td></tr><tr><td>

Software installs normalization status

</td><td>

Software Discovery Models \[cmdb\_sam\_sw\_discovery\_model\]

</td><td>

Count of software installs based on the normalization status.

 Select a normalization status on the donut chart to view the list of discovery models along with the installation count for each discovery model. You can further select a discovery model to view the list of software installations.

 The report for this widget is populated only once the following daily scheduled jobs have run:

-   SAM - Normalize discovery models using content library rules
-   SAM - Daily Job

 **Note:** Only the Product filter can be applied to this widget.

</td></tr><tr><td>

End of life products

</td><td>

Product Lifecycle \[sam\_sw\_product\_lifecycle\]

</td><td>

Graph of software product lifecycles that are reaching their end of life cycle. Select to drill down to the software installations.

</td></tr></tbody>
</table>## Activity center

Get alerts and notifications regarding your software assets. These alerts and notifications are asynchronous in nature. The Activity center displays a pre-defined set of alerts to notify you of actions that require your immediate attention. Notifications about events or activities that you should be aware of also appear in the Activity center. Select an alert or notification for more information.

Any user with the role of sam\_user can access all alerts and notifications except for the following alerts that require the sam\_admin role.

-   Scheduled jobs failed.
-   Last content download failed.

<table id="table_eqz_lxj_bpb"><thead><tr><th>

Alerts

</th><th>

Source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Removal candidates identified

</td><td>

Removal Candidate \[samp\_sw\_reclamation\_candidate\]

</td><td>

New removal candidates whose active status is true and the state is ready.

 Select to view the entire list of removal candidates in the License usage view.

</td></tr><tr><td>

New normalization suggestions

</td><td>

Normalization Suggestions \[samp\_normalization\_suggestions\]

</td><td>

Normalization suggestion records created where the state is new.

 Select to view the new normalization suggestion records in detail.

</td></tr><tr><td>

Unrecognized subscription identifiers

</td><td>

Unrecognized Subscription Identifier \[samp\_sw\_unrecognized\_subscription\_identifier\]

</td><td>

The number of unrecognized subscriptions are identified where the software model column is empty.

</td></tr><tr><td>

New software request

</td><td>

Request \[sc\_request\]

</td><td>

Software requests where the request state is pending approval.Select to view the software request list in the classic Software Asset Management interface.

</td></tr><tr><td>

Last reconciliation failure

</td><td>

Reconciliation Result \[samp\_reconciliation\_result\]

</td><td>

The latest scheduled job for the reconciliation process failed.

 Select to view the results in the License usage view.

 **Note:** Last reconciliation failed \(an alert\) or Last reconciliation completed \(a notification\) is shown depending on the status of the reconciliation process. If the reconciliation process failed, an alert is shown. If the reconciliation process was successful, a notification is shown.

</td></tr><tr><td>

Scheduled jobs failed

</td><td>

Software Asset Job Result \[samp\_job\_log\]

</td><td>

Scheduled jobs that failed in their latest run within the last one week. Select to open the Software Asset job Logs in a new tab.

 **Note:** Only a user with the sam\_admin role can access the Software Asset Job result table.

</td></tr><tr><td>

Entitlement import errors

</td><td>

Entitlement Import Error \[samp\_entitlement\_import\]

</td><td>

Entitlement import errors where the error status column has the value open.

</td></tr><tr><td>

New entitlement import error created via purchase receipts

</td><td>

Entitlement Import Errors \[samp\_entitlement\_import\]

</td><td>

The number of entitlement import errors where the purchase orders have an associated procurement integration profile.**Note:** This alert appears only when the Asset Management - Procurement Integration \(app-itam-procurement-integration\) store application is installed. For more information, see [Install Asset Management - Procurement Integration](../../procurement/task/install-proc-int.md).

</td></tr><tr><td>

Last content download failed

</td><td>

Asset Job Log \[asset\_job\_log\]

</td><td>

The latest scheduled job for content download failed. **Note:** Only a user with the sam\_admin role can access the Asset Job Log table.

</td></tr><tr><td>

Failed - entitlement import of &lt;&lt;.xlsx&gt;&gt;

</td><td>

Entitlement Import \[samp\_bulk\_import\]

</td><td>

Entitlement import status based on its success or failure. The failed status is displayed as an alert or one of the completed statuses is displayed as a notification:

-   Completed - entitlement import
-   Completed with errors - entitlement import

</td></tr><tr><td>

New CPE normalization suggestion

</td><td>

CPE Normalization Suggestions\[sn\_samp\_vr\_cpe\_mapping\_suggestion\]

</td><td>

CPE normalization suggestion records created where the state is new.

 Select to view the new CPE normalization suggestion records in detail.

</td></tr><tr><td>

Number of renewals coming up in 90 days

</td><td>

-   Contract

\[ast\_contract\]

-   Software License

\[alm\_license\]


</td><td>

The number of software contract and entitlement renewals coming up in 90 days.

 Select the alert to view the upcoming renewals within 90 days from the current date.

</td></tr></tbody>
</table><table id="table_dzn_1yn_fpb"><thead><tr><th>

Notifications

</th><th>

Source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New SSO applications identified last week

</td><td>

SSO Application \[samp\_sso\_application\]

</td><td>

New single sign-on \(SSO\) applications that have the SSO status as disconnected and were created within the last one week from the current date.

</td></tr><tr><td>

Last reconciliation completed

</td><td>

Reconciliation Result \[samp\_reconciliation\_result\]

</td><td>

The latest scheduled job for the reconciliation process was successfully completed. Select to view the results in the License usage view.

</td></tr><tr><td>

Products nearing end of life

</td><td>

Software Lifecycle Report \[sam\_sw\_product\_lifecycle\_report\]

</td><td>

Products that are nearing the end of their lifecycle and the install count is greater than 0.

</td></tr><tr><td>

New PPNs added to the library

</td><td>

Software Product Definition \[samp\_sw\_product\_definition\]

</td><td>

New PPNs added to the Content Service library with the latest content version as compared to the present date.

</td></tr><tr><td>

Software asset demands approved

</td><td>

Software Asset Demand \[samp\_demand\]

</td><td>

Software Asset Demand list view filtered by those that are approved.

</td></tr><tr><td>

Completed - entitlement import

 or

 Completed with errors - entitlement import

</td><td>

Entitlement Import \[samp\_bulk\_import\]

</td><td>

Entitlement import is successfully completed or completed with some errors.

**Note:** If the entitlement import fails, it’s shown as an alert.

</td></tr><tr><td>

New entitlement created via purchase receipts

</td><td>

Software Entitlements \[alm\_license\]

</td><td>

Number of entitlements created from purchase orders that have an associated procurement integration profile.**Note:** This notification appears only when the Asset Management - Procurement Integration \(app-itam-procurement-integration\) store application is installed. For more information, see [Install Asset Management - Procurement Integration](../../procurement/task/install-proc-int.md).

</td></tr></tbody>
</table>