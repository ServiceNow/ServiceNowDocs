---
title: Using the Response Evaluation Flow
description: Use the response evaluation flow to set the criteria for automatically assessing contractor responses.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Assign task to a contractor, Field Service Marketplace, Scheduling and dispatching, Use, Field Service Management]
---

# Using the Response Evaluation Flow

Use the response evaluation flow to set the criteria for automatically assessing contractor responses.

This sets the criteria for assessing contractor responses. This subflow evaluates the responses received from fulfillers and takes a single response as input then performs the necessary calculations based on it.

Any value entered into Response evaluation flow should be a subflow.

**Note:** The subflow should accept only response as an input.

There are two default option for Response evaluation flow:

-   Override wait duration - Automatically overrides the specified wait duration when a bid is being progressively pushed. In scenarios where the first contractor responds before the wait time is up, this setting will bypass the remaining wait time and immediately continue with sending out the next request. This process continues until the bid is assigned or there are no fulfillers left for assignment, whichever comes first.
-   Auto assign - Automatically assigns the bid to the first eligible contractor to accept.

**Note:** Customers can create their own subflows to evaluate responses.

