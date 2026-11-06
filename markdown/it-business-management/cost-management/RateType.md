---
title: Rate type in labor rate card
description: The rate type functionality is used to categorize different types of work. For example, Standard versus Overtime.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/cost-management/RateType.html
release: australia
product: Cost Management
classification: cost-management
topic_type: concept
last_updated: "2026-11-06"
reading_time_minutes: 1
breadcrumb: [Manage a labor rate card, Task and labor rate cards, Cost Management, Strategic Portfolio Management]
---

# Rate type in labor rate card

The rate type functionality is used to categorize different types of work. For example, Standard versus Overtime.

The Labor Rate Card form lets you specify the rate type, the hourly rate for that type, and the users it applies to. A single user can be associated with multiple labor rate cards that have different rate types.

Assume that a user logs time against a task and selects the rate type Standard in the Time Cards form. After approval, the system derives the expense line \(cost\) for the time card. The system looks for a labor rate card that is assigned to the user and has the same rate type. If the user has multiple matching cards, the system uses the card with the lowest value in the Order field. If no labor rate card matches the user and rate type, the system uses the default hourly rate. This rate is in the Time Sheets Administration Time Sheet Policy form \(com.snc.time\_card.default\_rate\) property.

**Note:** A user can enter a rate type only if it is permitted by the users [Time sheet policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/time-card-management/time-sheet-policies.md).

**Parent Topic:**[Manage a labor rate card](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/cost-management/t_ManageALaborRateCard.md)

**Related topics**  


[Create a rate type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/time-card-management/CreateRateType.md)

