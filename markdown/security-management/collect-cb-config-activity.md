---
title: Collect Carbon Black Configurations Flow Action
description: The Collect Carbon Black Configurations flow action gathers configuration information to use in the flow.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Security Operations Carbon Black Integration - Get Running Processes Flow, Security Operations Integration- Get Running Processes capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Collect Carbon Black Configurations Flow Action

The Collect Carbon Black Configurations flow action gathers configuration information to use in the flow.

The Collect Carbon Black Configurations flow action gathers Carbon Black configuration information to use in the flow.

## Results

Possible results for this flow action are:

|Result|Description|
|------|-----------|
|Success|Configuration succeeded.|
|Failure|An error occurred while attempting to verify the configuration. More error information is available in the flow action output error.|

## Input variables

There are no input variables for this flow action.

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|endpoint\_base|Base URL of the third-party integration API.|
|use\_mid\_server|Determines whether the REST flow action uses the MID server to interact with Carbon Black or not.|
|api\_token|Third-party integration API key.|

**Parent Topic:**[Security Operations Carbon Black Integration - Get Running Processes Flow](../concept/secops-integration-cb-get-running-processes-workflow.md)

