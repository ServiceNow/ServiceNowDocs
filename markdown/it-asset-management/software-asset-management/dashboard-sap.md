---
title: Software Publisher Analytics dashboard for SAP in Software Asset Management classic
description: View your license compliance position for SAP on the Software Publisher Analytics dashboard in the Software Asset Management classic application.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Software Publisher Analytics dashboard for SAP in Software Asset Management classic

View your license compliance position for SAP on the Software Publisher Analytics dashboard in the Software Asset Management classic application.

Access the dashboard by navigating to **All** &gt; **Software Asset** &gt; **SAP Compliance and Optimization** &gt; **Overview**.

The dashboard is updated whenever a new reconciliation result is available.

## End users and roles

|End user and goal|Required role|
|-----------------|-------------|
|SAM user: Can view the dashboard to track SAP license compliance and potential savings.|sam\_user|

## SAP dashboard

![Software Publisher Analytics dashboard for SAP.](../image/publisher-dashboard-sap.png)

<table id="table_qc5_wn3_qfb"><thead><tr><th>

Report

</th><th>

Source list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Products Out of Compliance

</td><td>

Software Model Result

</td><td>

Number of software models that are out of compliance.

</td></tr><tr><td>

True-up Cost

</td><td>

Software Model Result

</td><td>

Cost to be compliant based on the average prices for entitlements. The cost covers Named User Types and Engines.

</td></tr><tr><td>

Potential Savings

</td><td>

Software Model Result

</td><td>

Amount saved if removal candidates are reclaimed. The savings covers Named User Types and Engines.

</td></tr><tr><td>

Over-licensed Amount

</td><td>

Software Model Result

</td><td>

Cost of licenses that are owned but not used. The cost covers Named User Types and Engines.

</td></tr><tr><td>

Inactive Users

</td><td>

SAP System Users

</td><td>

SAP users who logged in over 90 days ago.

</td></tr><tr><td>

System Users Without a Named User Assignment

</td><td>

SAP System Users

</td><td>

SAP users who do not have a named user assignment.

</td></tr><tr><td>

Un-used Engines

</td><td>

License Metric Results

</td><td>

Number of SAP engines that have not been used but have active software entitlements.

</td></tr><tr><td>

Engines Usage Reached 90% and Above

</td><td>

License Metric Results

</td><td>

Number of SAP engines that reached 90% usage or higher.

</td></tr><tr><td>

Locked Out Licensed SAP Users

</td><td>

SAP System Users

</td><td>

Locked SAP users consuming a license.

</td></tr><tr><td>

Licensed Non-Dialog Users

</td><td>

SAP System Users

</td><td>

SAP non-dialog users that have a named user assignment.

</td></tr><tr><td>

Users For Roles Based License Optimization

</td><td>

SAP System Users

</td><td>

Number of SAP users that could have their role changed to optimize license consumption.

</td></tr><tr><td>

Users for Transaction Based License Optimization

</td><td>

SAP System Users

</td><td>

Number of SAP users for which Software Asset Management has detected user transaction-based license optimizations.

 Select the report to view the list of users that can be optimized.

</td></tr><tr><td>

Potential Indirect Access \(Transaction Activity\)

</td><td>

SAP System Users

</td><td>

Number of SAP users with indirect access to the SAP system based on user transaction activity. Users are given a score based on the amount of data received or sent by each connection.

</td></tr><tr><td>

Potential Indirect Access \(User Activity\)

</td><td>

SAP System Users

</td><td>

Number of SAP users that have indirect access to the SAP system.Users are given a score based on total CPU time, peak count, and steps.

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management publisher pack for SAP](../concept/sap-publisher-pack.md)

**Related topics**  


[Tables installed with the SAP publisher pack](../concept/component-installed-sap-plugin.md)

[Deploy the ABAP program for SAP](../task/import-abap-program-sap.md)

[Establish an SAP connection](../task/add-sap-connection.md)

[Create entitlements for SAP](../task/create-entitlement-sap.md)

[Create software models for SAP](../task/add-software-model-sap.md)

[Create a custom SAP named user type](../task/create-named-user.md)

[Map a role to a named user type](../task/create-named-user-type-role-mapping.md)

[Create custom SAP price lists](../task/create-sap-pricelist.md)

[Import custom SAP named user types](../task/import-custom-sap-named-user-type.md)

[Import custom SAP price lists](../task/import-custom-sap-price-list.md)

[SAP USMM-based optimization](../concept/usmm-optimization.md)

[User transaction activity for named user types](../concept/sap-named-user-transaction-activity.md)

[Self-declaring SAP engine license usage](../concept/self-declaring-sap-engine-usage.md)

[Publisher overview for SAP in the Software Asset Workspace](publisher-overview-sap.md)

