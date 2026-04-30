---
title: Contract Rate Card form
description: The Contract rate card form enables you to generate expense lines for recurring expenses automatically by providing detailed price information for a contract. There can be multiple rate cards for the same contract.
locale: en-US
release: yokohama
product: Contract Management
classification: contract-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a contract rate card, Contracts, Contract Management use, Contract Management, IT Asset Management]
---

# Contract Rate Card form

The Contract rate card form enables you to generate expense lines for recurring expenses automatically by providing detailed price information for a contract. There can be multiple rate cards for the same contract.

|Field|Description|
|-----|-----------|
|Number|Contract rate card number.|
|Contract|Internal contract number.|
|Summary type|Contract rate card type. Categorizing rate cards can be useful for reporting. Select **Grow Business**, **Run Business**, or **Transform Business**.|
|Name|Descriptive name for the contract rate card.|
|Active|Option that indicates whether the rate card is available for use.|
|Short description|Brief description of the contract rate card.|
|Start date|Date on which the contract rate card becomes active. Expense lines are generated for the costs incurred beginning on the date specified. For financial calculations to work, the date cannot be before the start date of the contract.|
|End date|Date on which the contract rate card becomes inactive. For financial calculations to work, the date cannot be after the end date of the contract. If no value is entered, the date is automatically set to the end date of the contract if the contract has an end date. No expense lines are generated for costs incurred after the end date.|
|Interval|The amount of time between rate card charges. For example, **Monthly**, **Quarterly**, or **Annually**.|
|Cost center|The cost center financially responsible for the rate card.|
|Last processed|The most recent date on which the rate card was charged.|
|Next process|The next date on which the rate card will be charged.|
|Description|Detailed information about the rate card.|
|Sales tax|Option that indicates whether to apply sales tax to the total cost.|
|Tax rate|The effective tax rate to apply to the total cost. This tax rate is usually the average tax rate charged.|
|Distribute cost|The method for distributing the amount listed in the **Base cost** field and generating expense lines.|
|Value|Type of value to use when **Allocate and distribute cost based on value** is selected in the **Distribute cost** field.|
|Base cost|The amount that must be paid before taxes.|
|Tax cost|Total cost of the tax.|
|Total cost|Final cost of the rate card after adjustments such as taxes have been applied.|

**Parent Topic:**[Create a contract rate card](../task/t_ContractRateCardsAndExpenseLines.md)

**Related topics**  


[Create a new expense line](../task/t_CreatingANewExpenseLine.md)

[Generating expense lines based on assets or users](../task/t_GenExpnsLinOnAssetsUsers.md)

[View contract expense lines](../task/t_ViewingContractExpenseLines.md)

