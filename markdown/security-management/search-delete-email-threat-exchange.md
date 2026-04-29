---
title: Check Compliance Search Status Action
description: The Check Compliance Search Status action check the status of created compliance search on exchange server and if the status is completed return the information regarding email search found for the compliance search.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Common Security Operations integration flows and orchestration activities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Check Compliance Search Status Action

The Check Compliance Search Status action check the status of created compliance search on exchange server and if the status is completed return the information regarding email search found for the compliance search.

## Input variables

Input variables determine the initial behavior of the action.

|Variable|Description|
|--------|-----------|
|targetId|Mandatory target host identifier field where the Exchange Server is located.|
|searchName|Mandatory name of compliance search created on exchange server.|

## Output variables

The output variables contain data that can be used in subsequent actions.

|Variable|Description|
|--------|-----------|
|response|Contains status of the compliance search and number of emails found on the exchange server for the compliance search.|

## Exit Conditions

Possible exit conditions for this action are:

|Variable|Description|
|--------|-----------|
|Search In Progress|When status of compliance search is in progress.|
|Search Complete - No Threat Emails Found|When status of compliance search is completed, and no emails are found as a part of compliance search.|
|Search Complete - Threat Emails Found|When status of compliance search is completed, and emails are found as a part of compliance search.|
|Error Checking Status|When status checking fails due to exception in exchange server.|
|Error|When exception occurs in flow action.|

**Parent Topic:**[Common Security Operations integration flows and orchestration activities](../../../security-operations-common/concept/common-wf-activities.md)

