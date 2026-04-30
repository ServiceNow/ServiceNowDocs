---
title: Creating a decision table for recommending assignment groups
description: Create a decision table with name Assignment group for a router issue that provides an assignment group as a result for a given product and problem combination.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Example: Recommend an assignment group for a router issue, Example configurations of recommended actions, Recommended Actions configuration, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Creating a decision table for recommending assignment groups

Create a decision table with name **Assignment group for a router issue** that provides an assignment group as a result for a given product and problem combination.

This decision table requires two inputs:

|Input|Type|
|-----|----|
|Product|String|
|Problem|String|

For the result, create the Assignment group column with Result type selected as Reference and Result table selected as Group \[sys\_user\_group\].

Configure the decision table conditions, results, and values as displayed in the following table. For more information, see [Decision Tables](https://www.servicenow.com/docs/access?context=decision-table&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

|Condition columns|Result column|
|Product|Problem|Assignment group|
|-----------------|-------------|
|-------|-------|----------------|
|Router M-series|Internet connectivity issue|Router-M-Team-A|
|Router M-series|Router is heating up|Router-M-Team-B|
|Router M-series|Network outage|Router-M-Team-C|
|Router M-series|Security concerns|Router-M-Team-D|
|Router N-series|Internet connectivity issue|Router-N-Team-A|
|Router N-series|Router is heating up|Router-N-Team-B|
|Router N-series|Network outage|Router-N-Team-C|
|Router N-series|Security concerns|Router-N-Team-D|

