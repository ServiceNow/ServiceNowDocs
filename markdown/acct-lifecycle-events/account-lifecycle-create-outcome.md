---
title: Create a primary success outcome
description: Create a primary success outcome that can be used to measure the achievement of a success objective.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Basic setup, Customer success, Customer Success Management, Customer Success Management]
---

# Create a primary success outcome

Create a primary success outcome that can be used to measure the achievement of a success objective.

## Before you begin

Role required: sn\_acct\_lc.customer\_success\_agent

## About this task

Primary success outcomes are measurable components of success objectives. They’re both measurable and actionable and progress can either be tracked automatically using data collected by the Data Context Engine, or manually for outcomes which aren't easily tracked through metrics.

## Procedure

1.  Navigate to **Workspace** &gt; **CSM/FSM Configurable Workspace** and select the **List** icon.

2.  Navigate to the **Customer Success** &gt; **All Outcomes** and select **New**.

3.  On the form, fill in the fields.

<table id="table_olw_rwv_zbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System generated unique number for the onboarding case record.

</td></tr><tr><td>

Account

</td><td>

The account number of the enterprise customer associated with the account.

</td></tr><tr><td>

Success objective

</td><td>

Select the success objective with which this outcome should be associated. This is a required field.

</td></tr><tr><td>

Owner

</td><td>

The internal person responsible for tracking the achievement of this outcome.

</td></tr><tr><td>

State

</td><td>

State of the primary success outcome.-   New
-   In progress
-   Paused
-   Canceled
-   Closed


</td></tr><tr><td>

Progress

</td><td>

Current progress of this outcome.-   Not Started
-   On-Track
-   At Risk
-   Paused
-   Completed
-   Canceled


</td></tr><tr><td>

Priority

</td><td>

Priority of this outcome in comparison to others.-   Critical
-   High
-   Medium
-   Low
-   Very Low


</td></tr><tr><td>

Planned start

</td><td>

Date on which the work for this outcome is scheduled to start.

</td></tr><tr><td>

Planned stop

</td><td>

Date on which the work for this outcome is scheduled to stop.

</td></tr><tr><td>

Title

</td><td>

Enter a title for this outcome. This is a required field.

</td></tr><tr><td>

Watch list

</td><td>

Select the users who should be notified of any updates to the outcome.

</td></tr><tr><td>

Work notes list

</td><td>

Select the users who should be notified of any updates to the worknotes.

</td></tr><tr><td>

Description

</td><td>

Enter a description for this outcome. This is a required field.

</td></tr><tr><td>

Work notes

</td><td>

Any internal notes regarding this outcome.

</td></tr><tr><td>

Unit

</td><td>

Unit of measurement of this success outcome.

</td></tr><tr><td>

Tracking method

</td><td>

Tracking method for this outcome.-   Manual: Enter the measurement unit and values manually.
-   Metric: Select a metric from the list. The values are populated automatically if the data source and context engine mapping have been configured.

**Note:** The metric values are automatically populated if:

    -   The context for the data source must be configured to reference the primary success outcome table. See [Define the data source](../concept/account-lifecycle-define-data-source.md).
    -   The source and the resolving context tables must be correctly configured. See [Configure the Context Engine Mapper](../concept/account-lifecycle-define-context-engine-mapper.md).


</td></tr><tr><td colspan="2">

![Context engine mapping](../image/account-lifecycle-success-obj-mapping.png)

</td></tr><tr><td>

Base value

</td><td>

Starting point or base value for this outcome.

</td></tr><tr><td>

Target value

</td><td>

Target value that is to be achieved.

</td></tr><tr><td>

Current value

</td><td>

Current value of the primary success outcome.

</td></tr></tbody>
</table>4.  Select **Save** to create a primary success outcome.


**Parent Topic:**[Basic customer success setup](../concept/account-lifecycle-basic-config.md)

