---
title: Create a safety risk category
description: Create or modify a risk category to group your workplace hazards into logical categories.
locale: en-US
release: xanadu
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure settings, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Create a safety risk category

Create or modify a risk category to group your workplace hazards into logical categories.

## Before you begin

Role required: sn\_hs\_rm.risk\_category\_manager or sn\_hs\_rm.risk\_category\_writer

## Procedure

1.  Select **All**.

2.  In the navigation filter of the application navigator, enter the following command:

    `sn_hs_rm_risk_category.list`

    The Risk categories list appears.

3.  Create a risk category or update an existing one.

    -   To create a risk category, select **New**.
    -   To modify an existing risk category, open it from the list.
4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Number|System-generated unique number for the risk category.|
    |Name|Name of the risk category.|
    |Short description|Description of the risk category.|
    |Order|Order at which this risk category is listed on the Select hazards form when submitting a Job safety analysis \(JSA\).|
    |Active|Option to mark this risk category available for use. A risk category must be active to be used.|

5.  Select **Submit**.


## Result

-   The risk category is created and saved in the Risk category \[sn\_hs\_rm\_risk\_category\] table.
-   The category is listed in the **Risk category** field on the Hazard details form.
-   It is also displayed on the Select hazards form when submitting a Job safety analysis \(JSA\). However, a risk category with no hazards associated with it doesn't appear on the Select hazards form.

## What to do next

Associate related hazards with the risk category. For more information, see [Define Health and Safety hazards](hs-define-hazards.md).

**Parent Topic:**[Setting up Health and Safety Risk Management](../concept/hs-setting-up-risk-mgmt.md)

