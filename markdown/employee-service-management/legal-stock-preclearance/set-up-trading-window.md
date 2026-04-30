---
title: Set up a trading window
description: Set up a trading window for a period in which certain designated employees of the organization are permitted to trade in the securities of your organization.
locale: en-US
release: yokohama
product: Legal Stock Preclearance
classification: legal-stock-preclearance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up Legal Stock Preclearance, Legal Stock Preclearance, Legal Service Delivery Practice Applications, Legal Service Delivery, Employee Service Management]
---

# Set up a trading window

Set up a trading window for a period in which certain designated employees of the organization are permitted to trade in the securities of your organization.

## Before you begin

Role required: sn\_lg\_stock\_cp.stock\_config

## About this task

During an open trading window, the designated employees such as directors and executives can trade in compliance with your organization's Insider Trading Policies.

## Procedure

1.  Navigate to **All** &gt; **Legal Administration** &gt; **Stock Preclearance Admin** &gt; **Trading Windows**.

2.  Click **New** to set up a trading window.

3.  On the form, fill in the fields.

<table id="table_pql_2sd_4jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

Unique short description for the trading window.

</td></tr><tr><td>

Fiscal quarter

</td><td>

Fiscal quarter for which the trading window is open.

</td></tr><tr><td>

Opening date

</td><td>

Date the trading window opens.

</td></tr><tr><td>

Closing date

</td><td>

Date the trading window closes.

</td></tr><tr><td>

Request submission start date

</td><td>

Date from which you can start submitting preclearance requests.

</td></tr><tr><td>

Earnings date

</td><td>

Date of your company’s earnings.

</td></tr><tr><td>

Approval validity days

</td><td>

Number of days a stock preclearance approval is valid for.

</td></tr><tr><td>

Exclude trading holidays

</td><td>

Option to exclude trading on holidays that fall within the trading window. Selecting this option extends the approval validity days by the number of holidays during the trading period.**Note:** By default, weekend days are excluded for calculating the validity due date.

 For example, say that a trading window opens from January 1 to January 31 and you have set the approval validity days to 10 days. If January 24 and 25 are trading holidays, then,

-   If the preclearance is approved on January 8, the approval validity is until January 22 \(10 days from January 8 + 4 days of two weekends\).
-   If the preclearance is approved on January 15, the approval validity is until January 31 instead of January 25 \(10 days + 4 days of two weekends + 2 holidays from January 15\).
-   If the preclearance is approved on January 21, the approval validity is until February 6 \(10 days + 2 holidays from January 20 + 4 days of two weekends\). However, as the trading window closes earlier than the validity of approval, the last date is January 31 rather than February 6.


</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Setting up Legal Stock Preclearance](../concept/legal-stock-pre-administration.md)

