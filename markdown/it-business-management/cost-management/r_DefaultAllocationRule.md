---
title: Default allocation rule
description: For every expense line generated for a business service, the default allocation rule Process Svc-CC Relationships will attempt to process the expense and create allocations for each cost center that is consuming the service.
locale: en-US
release: zurich
product: Cost Management
classification: cost-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use business services with expenses, Cost Management, Strategic Portfolio Management]
---

# Default allocation rule

For every expense line generated for a business service, the default allocation rule Process Svc-CC Relationships will attempt to process the expense and create allocations for each cost center that is consuming the service.

The amount of the expense allocation is calculated by dividing the number of units the cost center is consuming by the total number of units for the business service. This calculation method is refereed to as "all unit" allocation as it uses the total unit capacity to determine the allocation percentage.

Refer to the demo walk-through for a detailed example.

For a given business service expense line, it is typical that less than 100% of the expense would be allocated using this method not all units have been allocated to cost centers. The unallocated expenses could be considered IT overhead. Some organizations prefer to show 100% expense allocation regardless of how many units are in use. This method is referred to as "allocated unit" since the percent of allocation calculated by dividing the number of units the cost center is consuming by total number of allocated units from all cost centers.

|Allocation calculation method|Example|
|-----------------------------|-------|
|all\_units|Service supports 100 units but only has 50 units allocated, and cost center ABC is allocated 25 units. This method will result in an allocation cost of 25/100, or 25% of the total cost of the service. 50% of the expenses \(from the 50 unallocated units\) will not be allocated.|
|allocated\_units|Service supports 100 units but only has 50 units allocated, and cost center ABC is allocated 25 units. This method will result in an allocation cost of 25/50, or 50% of the total cost of the service. 100% of the expenses will be allocated, showing full cost recovery.|

This is a system wide setting that can be configured by navigating to **Financial Management** &gt; **Properties** module and selecting an option from the choice list.

**Parent Topic:**[Use business services with expenses](../concept/c_UseBusinessServicesWithExpenses.md)

