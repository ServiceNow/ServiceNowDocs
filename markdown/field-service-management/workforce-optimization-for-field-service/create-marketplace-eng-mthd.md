---
title: Create a marketplace engagement method
description: Create a marketplace engagement method to specify how contractors respond to requests.
locale: en-US
release: xanadu
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Field Service Marketplace, Configuring contractor capabilities, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Create a marketplace engagement method

Create a marketplace engagement method to specify how contractors respond to requests.

## Before you begin

Role required: sn\_mktplace\_core.mktplace\_admin

## About this task

Marketplace engagement methods determine the criteria that contractors can respond to for requests. Field Service Marketplace comes installed with following methods:

<table id="table_vcw_hpb_1cc"><thead><tr><th>

Engagement method

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Task acceptance

</td><td>

The task acceptance engagement method closes the request after the set duration. Participants can either accept or reject requests.

</td></tr><tr><td>

Time and cost based

</td><td>

The time and cost based engagement method closes after the set duration and enable participants to share time or cost estimates for the request.

</td></tr><tr><td>

Cost based

</td><td>

The cost based engagement method allows participants to respond with cost details for the request. The Request is progressively pushed based on acceptance or specified wait duration, whichever occurs first.

</td></tr><tr><td>

Auto-assign on acceptance

</td><td>

The Auto-assign on acceptance engagement method closes the request and auto-assigns it once an eligible contractor accepts the request.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  In the **Search** field, enter **marketplace\_engagement\_method**.

3.  Select **Marketplace engagement method**.

4.  Select **Show List**.

5.  Select **New**.

6.  In the form, fill in the fields:

<table id="table_pwz_xbq_21c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the engagement method.

</td></tr><tr><td>

Description

</td><td>

Description of the engagement method.

</td></tr><tr><td>

Lead time

</td><td>

Time after which the marketplace request is ready for responses

</td></tr><tr><td>

Progressive push

</td><td>

Using contractor ranking, incrementally pushes request to marketplace participants in numerical order based on specified wait duration.

If the contractor does not respond or accept within a specified time frame, the request is shared automatically to the next ranked candidate. This process continues sequentially down the ranking list until it is shared with all contractors.

</td></tr><tr><td>

Wait duration

</td><td>

Default time period to wait for acceptance before request is made visible to the next marketplace participant.This is applicable when progressive push is set to true.

</td></tr><tr><td>

Duration

</td><td>

Duration the request remains active for.

</td></tr><tr><td>

Close condition

</td><td>

The condition that closes the request.

</td></tr><tr><td>

Active

</td><td>

Determines whether this method is active or inactive.

</td></tr><tr><td>

Allow sharing estimates

</td><td>

Determines whether participants can share their cost or time estimate for the request.

</td></tr><tr><td>

Mandate cost estimate

</td><td>

Determines whether participants are required to provide cost estimate.

</td></tr><tr><td>

Mandate time estimate

</td><td>

Determines whether participants are required to provide time estimate.

</td></tr><tr><td>

Response evaluation flow

</td><td>

This sets the criteria for assessing contractor responses. This subflow evaluates the responses received from fulfillers and takes a single response as input then performs the necessary calculations based on it.Any value entered into Response evaluation flow should be a subflow.

**Note:** The subflow should accept only response as an input.

There are two default option for Response evaluation flow:

-   Override wait duration - Automatically overrides the specified wait duration when a bid is being progressively pushed. In scenarios where the first contractor responds before the wait time is up, this setting will bypass the remaining wait time and immediately continue with sending out the next request. This process continues until the bid is assigned or there are no fulfillers left for assignment, whichever comes first.
-   Auto assign - Automatically assigns the bid to the first eligible contractor to accept.
**Note:** Customers can create their own subflows to evaluate responses.

</td></tr></tbody>
</table>7.  Select **Submit**.


