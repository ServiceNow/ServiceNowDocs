---
title: Allocating expenses
description: Expenses can also be allocated to a business entity that is responsible for the expense.
locale: en-US
release: zurich
product: Cost Management
classification: cost-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Cost Management, Strategic Portfolio Management]
---

# Allocating expenses

Expenses can also be allocated to a business entity that is responsible for the expense.

This is not considered charge-back or billing but could be used as a source for billing. The primary purpose of expense allocation is to represent the consumer of the process that has incurred some expense. This can be accomplished by defining expense allocation rules.

## Simple Example

This example demonstrates allocating every server-related expense line to the department responsible for the server.

To view the example:

1.  Navigate to **Financial Management** &gt; **Expense Allocation Rules**.
2.  Remove the list filter to view inactive rules as well as active ones.
3.  Select the **Server - Department** rule.

The rule states that for every expense line associated \(**Expense source** field\) with a server that has one of the selected statuses, generate an expense location record for 100% of the expense amount and assign the allocation to the server's department.

To view expense allocations, add the **Expense Allocation** related list to the form. The **Target** field is the business unit that the expense is allocated to.

![Cost Demo Alloc Exp](../image/CostDemoAllocExp.jpg "Cost Demo Alloc Exp")

## Complex Example

A more common example would be to allocate the costs of a business service to the business consumers. Since cost centers are generally used when referring to business finances, this example allocates business service costs to each cost center that is consuming the service and bases the amount allocated on the amount of the service the cost center consumes.

To view the example, navigate to **Financial Management** &gt; **Business Services** and select **Retail.** Switch to the **Cost** view to gain access to additional related lists.

The **Allocation Units** record defines the amount of capacity that this service provides. In this case, the Retail service can support 50 locations \(units\), of which 45 are allocated. A unit is a generic concept that can represent something that makes sense for that business service. This record uses units to represent allocation. The objective is to use the unit count and the cost center unit count to determine a percentage of total to calculate the allocation amount.

![Cost Demo Retail Allocation Units](../image/CostDemoRetailAllocunits.jpg "Cost Demo Retail Allocation Units")

The CI Cost Center Relationships list shows which cost centers are using the service and how many units they are using. This information is used to determine how much of the service expenses to allocate to each cost center. For example, the Trading department is using 10 of the 50 allocated units, so they will be allocated 20% of all Retail expenses. There's also an option to allocate based on the total \(10 or 45\).

![Cost Demo Retail Users](../image/CostDemoRetailUsers.jpg "Cost Demo Retail Users")

To see how the expense lines are allocated, select an entry in the **Expense Lines** related list and add the **Expense Allocation** related list to the Expense Line form.

The following is an expense from the dbaix901nyc server for $2,500. Two expense allocations are generated from the expense. The **Trading** cost center was allocated $500 \(20%\) of the expense based on the CI cost center relationship seen earlier.

![Cost Demo Retail Example](../image/CostDemoRetailExpallo.jpg "Cost Demo Retail Example")

This type of business-service-to-cost-center allocation is accomplished through the **Process Svc-CC Relationships** expense allocation rule. This is an advanced rule that uses script to determine the allocation logic.

**Parent Topic:**[Cost Management](../reference/r_CostManagement.md)

