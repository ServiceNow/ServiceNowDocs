---
title: Create a demand requirement
description: Create a demand requirement for rationalizing your SaaS and SSO applications.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Overlapping usage view, Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Create a demand requirement

Create a demand requirement for rationalizing your SaaS and SSO applications.

## Before you begin

Role required: sam\_admin or sam\_user

**Note:** The sam\_admin and sam\_user roles must have the it\_demand\_user role to create demand.

The PPM Standard \(com.snc.financial\_planning\_pmo\) plugin must be installed to create demands.

## Procedure

1.  Navigate to **Software Asset Workspace** &gt; **Overlapping usage**.

2.  Select the **Application feature usage** tab.

3.  Select the application in a category for which you want to create a demand.

4.  Select **Create demand**.

    The **Create demand** option is available only when you select an application that you want to create a demand for.

5.  Select the **Demand Requirements** tab.

6.  Select **New**.

    All the fields are auto-populated.

7.  On the form, fill in the fields.

<table id="table_bgs_5l2_4xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr class="sub-head"><td>

Demand Requirement

</td><td>

 

</td></tr><tr><td>

Number

</td><td>

Unique auto-generated identification number for the demand requirement.

</td></tr><tr><td>

Software asset demand

</td><td>

Software asset demand for which you’re creating the requirement.

</td></tr><tr><td>

Product

</td><td>

Product or application for which the demand requirement is created.

</td></tr><tr><td>

Main category

</td><td>

Category of the application. For example, if you select **Zoom** in the **Product** field, the **Main category** field would be set to **Video Conferencing**.

</td></tr><tr><td>

Action

</td><td>

Action items identified for the demand.-   Discontinue after expiration
-   Migrate to approved product
-   Discontinue immediately
-   Reclaim licenses
-   No action


</td></tr><tr><td>

Description

</td><td>

Description of the demand requirement.

</td></tr><tr><td>

Notes

</td><td>

Additional notes for the demand requirement.

</td></tr><tr class="sub-head"><td>

Spend Information

</td><td>

 

</td></tr><tr><td>

Spend amount

</td><td>

Total spend on the application based on entitlements.

</td></tr></tbody>
</table>8.  Select **Save**.


## Result

The demand requirement for the demand is created. You can view the created demand on the Software Asset Demand \[samp\_demand\] table.

## What to do next

To view all Software Asset Management demand requirements, navigate to **Software Asset** &gt; **Software Asset Demand** &gt; **Demand Requirements**.

