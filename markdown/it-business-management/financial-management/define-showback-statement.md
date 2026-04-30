---
title: Define, generate, and publish a showback statement
description: Showback tells the consumers what it costs a service organization such as IT to deliver services to them. Defining a showback statement helps to capture the reporting entity \(for example, a business unit\) to whom you want the showback statement to be reported to.
locale: en-US
release: xanadu
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 3
breadcrumb: [Financial charging application setup, Financial Charging, Financial Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Define, generate, and publish a showback statement

Showback tells the consumers what it costs a service organization such as IT to deliver services to them. Defining a showback statement helps to capture the reporting entity \(for example, a business unit\) to whom you want the showback statement to be reported to.

## Before you begin

Role required: service\_charging\_analyst

**Important:**

This feature is available only when you own an ITBM Analyst license.

## About this task

The showback statement is a collection of charges representing the statement items \(the services consumed by the business unit\) and is generated for a fiscal period.

Showback statements provide the business unit a visibility of the services consumed and the charges associated with these services. It also brings an awareness and helps them to be judicious in using the business services and conscious of the cost factor associated with it.

You can create multiple showback statements based on the same Statement Item by drilling down to its lowest level. The showback statements can be for different reporting entities. For example, you can use a drilldown entity that has the source data on a Statement Item to create showback statements for different reporting entities such as a Cost Center, Business Unit, or Department.

## Procedure

1.  Navigate to **All** &gt; **Financial Charging** &gt; **Administration** &gt; **Showback Statement Definition**.

2.  Click **New** to create a showback statement definition or click the name of an existing showback statement definition that you want to edit.

3.  Fill in the form fields.

<table id="table_ebp_22p_tz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the showback statement definition.

</td></tr><tr><td>

Description

</td><td>

Description for the showback statement definition.

</td></tr><tr><td>

Reporting entity

</td><td>

Report generated to show the entity of its consumption details.

</td></tr><tr><td>

Reporting user field

</td><td>

Reporting entity head who sees the report.

</td></tr><tr><td>

Frequency

</td><td>

Fiscal frequency for which the report is generated.

</td></tr><tr><td>

Reporting user group field

</td><td>

User group who can see the report.All the members of the user group can see the report.

</td></tr></tbody>
</table>4.  Click **Submit** to save the record or **Update** if you have edited an existing record.

5.  Click **Generate** to generate the showback statement for the selected fiscal period.

    The generated report is made available for viewing purpose to the reporting entity \(business unit\). The showback statement gives the information that the reporting entity has used the services mentioned in the statement lines.

    As a financial analyst, you can generate the showback statement and publish it so that the showback user can view it.

    As a designated showback user \(normally a business unit owner or a business unit finance lead\), you can view the published showback statements assigned to you or your unit. You can review and accept them or raise a dispute if there is discrepancy and resolve it with the service owner or service charging analyst through the task workflow.

6.  Click **Publish**.

    1.  Select the fiscal period in the **Fiscal Period** choice list of the Publish showback statement pop-up that opens up.

    2.  Click **OK**.

        **Note:**

        The fiscal period for which you have generated and not yet published the showback statement is listed in the choice list. By publishing, the showback statement for the said fiscal period is available and the showback users can view it in My Showback Statements menu in the application navigator.

7.  Click **Delete** to delete the record.

    [Create statement lines](determine-statement-item.md) for the Showback Statement by clicking the Showback Statement Line Definitions **New** button.


## What to do next

[Monitor the showback statements in the service pricing console](view-service-pricing-console.md).

**Parent Topic:**[Financial charging application setup](../concept/financial-reporting-appln-setup.md)

