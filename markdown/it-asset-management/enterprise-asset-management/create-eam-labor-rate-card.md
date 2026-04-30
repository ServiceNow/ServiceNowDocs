---
title: Create a labor rate card in Enterprise Asset Workspace
description: Create a labor rate card to capture costs by the time consumed on an hourly basis.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Total Cost of Ownership for enterprise assets, Create and manage enterprise assets, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Create a labor rate card in Enterprise Asset Workspace

Create a labor rate card to capture costs by the time consumed on an hourly basis.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager

## About this task

Labor rate cards are included in the base system. Except for the **Number** field, all other fields on the default labor rate cards are editable. You can't delete any of the base system labor rate cards. The following steps are to create a labor rate card.

## Procedure

1.  Navigate to **Enterprise Asset Workspace** &gt; **Admin center** &gt; **TCO configuration** &gt; **Labor rate card**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Number|A unique number automatically created for each labor rate card.|
    |Name|Name of the labor rate card.|
    |Rate code|Code for each labor rate card.|
    |Rate type|Standard rate type. You can add your own rate types.|
    |Active|Indicates if the labor rate card is being used or not. By default, this check box is selected.|
    |Short description|Short description of the labor rate card.|
    |Hourly rate|The currency code and the cost per hour.|
    |Set conditions|Filter to run on the table selected to determine whether this rate card applies to a given task. This field uses the Condition Count widget to preview what records would be returned by the conditions.|
    |Description|Detailed description of the labor rate card.|

4.  Select **Save**.

    After a labor rate card is created, expense lines are created based on the value in the **Use time worked** field.


**Parent Topic:**[Configuring Total Cost of Ownership for enterprise assets](../concept/confifure-eam-asset-tco.md)

