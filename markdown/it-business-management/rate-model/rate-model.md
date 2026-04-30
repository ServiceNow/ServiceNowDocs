---
title: Rate Models
description: Use a rate model to derive date-effective, criteria-driven hourly rates for calculating planned and actual resource costs for a project or demand.
locale: en-US
release: xanadu
product: Rate Model
classification: rate-model
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Project Portfolio Management, Strategic Portfolio Management]
---

# Rate Models

Use a rate model to derive date-effective, criteria-driven hourly rates for calculating planned and actual resource costs for a project or demand.

Unlike labor rates, which are based on the user attribute only, a rate model can derive hourly rates based on up to ten attributes. These attributes can be selected from predefined entities such as projects, demands, users, and roles.

## Rate lines

A rate model is a collection of multiple rate lines. A rate line is a unique combination of different criteria values that defines the hourly rate for a resource, group, or role for a specific date range. For the same set of criteria, you can create multiple rate lines with different rates for different date ranges provided that the dates don't overlap.

## Rate model processing

To derive hourly rates from a rate model for the resource plans and time cards of a project or demand, associate the rate model with the project or demand.​

**Note:** A project or demand without a rate model uses the labor rate cards associated with rate type to find a rate for the time cards.

The rate model associated with a project or demand evaluates the rate lines to find and return the hourly rate that matches the requested criteria. The rates are derived from the rate model during resource planning or allocation, and during time card processing.

The rate is returned in the functional currency specified in the matching rate line.

![Flow diagram of rate model processing](../image/rate-model-processing-flowdiagram.png "Rate model processing flow diagram")

The following video describes how to set up a rate model and the evaluation method to find and return the hourly rate for a request.Video explaining how to work with rate models

When a rate is requested, the rate model uses the following process.

1.  Finds the rate lines in the requested date range and discards the remaining rate lines.
2.  Evaluates the identified rate lines to find values matching the requested value in the first criteria column and discards the remaining rate lines.

    If the requested value is empty, it checks for rate lines containing NULL.

    If no exact match is found, it checks for the rate line having the value `All other (*)`.

    The evaluation is repeated for the other criteria columns in order of priority until all criteria columns are processed.

3.  Returns the rate if one or more rate lines match the request.

    -   If a single rate line is found, the corresponding rate is returned.

    -   If multiple rate lines are found, the system determines the number of hours in the request that applies to each rate.
    -   For example, say the rate requested is for resource allocation from July 1 to July 30. The rate model has one rate from July 1 to July 15 and a different rate from July 16 to July 30 for the same set of criteria. The rate model applies the first rate to the requested hours for July 1–15 and the second rate to the requested hours for July 16–30.
    If no rate lines match the request, then the request uses the [default rate card](../../cost-management/reference/r_InstalledWithCostManagement.md).


-   **[Create or modify a rate model](../task/create-rate-model.md)**  
Create or modify a rate model that can be linked to a project or demand to determine planned costs and actuals for their resource. The rate model provides date-effective, criteria-driven hourly rates for these investments.
-   **[Define criteria of a rate model](../task/define-rate-model-criteria.md)**  
Set the criteria of a rate model by adding attributes from a set of predefined entities to derive resource hourly rates based on the criteria.
-   **[Create a rate line](../task/create-rate-line.md)**  
In a rate model, create a rate line to define an hourly rate based on a set of criteria for a given date range.
-   **[Export rate lines to a file](../task/export-rate-lines.md)**  
Export rate lines to a Microsoft Excel or CSV file to quickly update or add new rate lines and import them back into the rate model.
-   **[Import rate lines into a rate model](../task/import-rate-lines.md)**  
Use the import rate lines function to quickly add multiple rate lines from an export file into a rate model.

**Parent Topic:**[Project Portfolio Management](../../project-portfolio-suite/concept/c_ProjectPortfolioSuite.md)

