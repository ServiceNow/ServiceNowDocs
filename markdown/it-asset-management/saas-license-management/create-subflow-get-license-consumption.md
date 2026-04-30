---
title: Create a subflow to get license consumption
description: Create a subflow to add license consumption data to the Subscription Consumption Summaries \[sam\_saas\_consumption\_summary\] table.
locale: en-US
release: yokohama
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [SaaS License Connections, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Create a subflow to get license consumption

Create a subflow to add license consumption data to the Subscription Consumption Summaries \[sam\_saas\_consumption\_summary\] table.

## Before you begin

This subflow is applicable to any integration that uses the SaaS license connection framework, including custom integrations.

Role required: flow\_designer or admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

    The Flow Designer launches in a new tab.

2.  On the Flow Designer home page, click **New** and then select **Subflow**.

    The Subflow Properties dialog box opens.

3.  On the dialog box, fill in the following fields.

<table id="table_dk4_brb_njb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Subflow Name

</td><td>

Name of the subflow. For example, `Download License Consumption`.

</td></tr><tr><td>

Description

</td><td>

Description of the subflow.

</td></tr><tr><td>

Application

</td><td>

Application scope to which you want the subflow to apply. Set this field to **Software Asset Management - SaaS License Management Integrations**.**Note:** If you save the subflow in the Software Asset Management - SaaS License Management Integrations application scope, it's included with your Software Asset Management subscription. If you save the subflow in any other application scope, you may be charged for ServiceNow® Integration Hub transactions. If you're publishing your custom spoke application on the ServiceNow Store, select your custom application scope instead.

</td></tr><tr><td>

Accessible From

</td><td>

Application scope from which the subflow is accessible. Set this field to **All application scopes**.

</td></tr><tr><td>

Category

</td><td>

Subflow category. Leave this field empty.

</td></tr><tr><td>

Protection

</td><td>

Read-only protections for your subflow. Set this field to **None**.

</td></tr><tr><td>

Sublow Annotation

</td><td>

Message that appears under the subflow title in the subflow picker. Leave this field empty.

</td></tr><tr><td>

Run As

</td><td>

Option to specify whether the flow runs as a system user or user who initiates the session. Set this field to **User who initiates session**.

</td></tr><tr><td>

Run with role\(s\)

</td><td>

Roles with which this subflow runs.

</td></tr></tbody>
</table>4.  Click **Submit**.

    The Flow Designer creates the draft subflow and then redirects you to the subflow configuration page.

5.  From the subflow configuration page, add an integration profile input.

    1.  Under INPUTS &amp; OUTPUTS, click the plus icon \(+\) to add an input for your subflow.

    2.  In the Inputs section, click the plus icon \(+\).

    3.  When prompted, enter the following information for your integration profile input.

        |Label|Name|Type|Mandatory|
        |-----|----|----|---------|
        |Integration profile|integration\_profile|Reference.Integration Profile|Yes|

    4.  Click **Done**.

6.  Add a data stream action for getting license consumption data.

    1.  Under ACTIONS, click the plus icon \(+\) and then select **Action** to add a new action.

    2.  When prompted, select the **Global** spoke from the list of INSTALLED SPOKES.

    3.  From the list of Default actions, select **Get &lt;saas-application&gt; Consumption**.

    4.  Click **Done**.

7.  Add an Upsert Consumption action as a child of the Get &lt;saas-application&gt; Consumption action.

    The Upsert Consumption action uploads license consumption data to the Consumption Summary table on your ServiceNow instance.

    1.  Under the Get &lt;saas-application&gt; Consumption action, click the plus icon \(+\) and then select **Action**.

    2.  When prompted, select **Software Asset Management** from the list of INSTALLED SPOKES.

    3.  From the list of Default actions, select **Upsert Consumption**.

        The Upsert Consumption action inputs appear.

    4.  From the Product \[Software Product\] list, search for and select the software product that you are connecting to with your integration.

        This value must be a reference to the Software Product \(samp\_sw\_product\) table. If the product does not exist in the table, [add a custom software product](t_AddACustomProduct.md).

    5.  Use values from the Data panel to fill in the remaining action inputs.

        Your request to the SaaS API may not return data for all inputs. Fill in the inputs that are applicable to your integration.

        |Field|Value|
        |-----|-----|
        |Version|Version of the SaaS application.|
        |Edition|Edition of the SaaS application, such as `Standard` or `Enterprise`.|
        |Unit of consumption|Unit of measure for the software units that can be consumed.|
        |Total units|Total number of software units that you have purchased across all active entitlements for the software product.|
        |Units consumed|Total number of software units that your users have consumed.|
        |Contract start|Start date of your contract.|
        |Contract end|End date of your contract.|

    6.  Click **Done**.

8.  Verify that your subflow is working properly by clicking **Test**.

    View the test results and system logs for details about any errors in your subflow. You can view system logs by navigating to **System Logs** &gt; **System Log** &gt; **All** in your ServiceNow instance.

9.  After verifying that the subflow is working as expected, click **Publish**.

    **Tip:** You can still edit the subflow after it's published.


## What to do next

View analytics such as subscription usage, cost, and compliance of your SaaS applications on [SaaS overview dashboard in workspace](../reference/saas-dashboard-workspace.md).

