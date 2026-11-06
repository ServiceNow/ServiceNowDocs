---
title: Flows, subflows, and actions installed
description: Find the flows, subflows, custom actions, events, and clean-up rules that Service Test Management installs to run tests in the background.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/stm-flows-and-actions.html
release: australia
topic_type: reference
last_updated: "2026-10-13"
reading_time_minutes: 4
keywords: [flows, subflows, custom actions, automated test run creation tool]
breadcrumb: [Reference, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Flows, subflows, and actions installed

Find the flows, subflows, custom actions, events, and clean-up rules that Service Test Management installs to run tests in the background.

## Flows and subflows

|Name|Purpose|
|----|-------|
|Execute Test Group|Starts when a test group run reaches the New state and processes the test runs of the test group run.|
|Execute test run|Runs one test run by calling the adapter and waiting for a result.|
|Outbound Flow for service test run STM|Sends the test run to an external system.|
|Outbound subflow for service test run|Contains the outbound call for a single test run. The outbound flow calls it.|
|Set Result on Each Test Measure|Writes the values that the external system returned to the test measures of a test run.|
|Evaluate Test Run Result|Compares the test measures of a completed test run with the threshold rules, creates violations, and applies consequences.|
|Automated test run creation tool|Subflow that creates a test run for a test definition within a test group run. See the inputs and output below.|
|Trigger resolution task creation for a test run|Creates resolution tasks for a failed test run that is linked to a service problem case.|
|Trigger resolution tasks for test groups|Creates resolution tasks for the failing test runs of a test group.|
|Create Diagnostic Task for case for test management|Subflow that creates a diagnostic task from a table and field values that you pass in, and returns the diagnostic task.|
|STM test run demo adapter|Demo adapter that simulates a test result without an external system.|
|TEMPLATE: Execute test run|Template to copy when you build an adapter for your own external system.|
|TEMPLATE: Execute test group|Template to copy when you build your own test group orchestration.|

## Automated test run creation tool

The subflow creates a test run for a test definition within a test group run and returns it. It can run a separate flow that creates test characteristics, wait for user input, and wait for the test run to complete.

|Name|Type|Description|
|----|----|-----------|
|Test definition GR|Reference, required|The test definition to run.|
|Test group run GR|Reference, required|The test group run that the new test run belongs to.|
|Test characteristics creation flow|Reference to a flow|A flow that creates the test characteristics of the test run. Optional.|
|Wait for input|True or false, default false|Makes the subflow wait for user input before it continues.|
|Wait for test run completion|True or false, default false|Makes the subflow wait until the test run completes.|
|Enable timeout|True or false, default false|Limits how long the subflow waits for completion.|
|Timeout duration|Duration|The time limit that applies when you enable the timeout.|
|testRunGR \(output\)|Reference to a test run|The test run that the subflow created.|

The new test run is named after the test definition, described as "Automated test run for" followed by the name of the definition. It is then linked to the test group run, and created in the Draft state with its start time set to the current time.

## Custom action types

|Action|Purpose|
|------|-------|
|Calculate Test Run Result|Calculates the result of a test run from the evaluation of its test measures.|
|Execute test groups|Starts the execution of a test group from a flow, using the group and the product context.|
|Get Ordered Test Runs Data for a Test Group|Returns the draft test runs of a test group run, grouped by the order of their test group to definition mappings.|
|STM update test run response|Writes the response of the external system to the test run.|
|STM Prepare request body|Builds the request body from the test run and its test measure definitions.|
|Create diagnostic task for a task|Creates a diagnostic task for any record that extends the Task table.|
|Get test groups for task|Finds the test groups that apply to a task.|
|Check If GenAI Plugin Installed|Returns whether the generative AI plugin is installed, so that a flow can branch.|
|Split String into Array|Splits a delimited string into an array that a flow can loop over.|

## Events, script actions, and clean-up

|Item|What it does|
|----|------------|
|Business rule: Add schedule run event to queue|Runs after a test group run is inserted. If the record has a scheduled time, it sets the state to Scheduled and queues the event for that time.|
|Event: sn\_st\_mgmt.schedule\_test\_group\_run|Schedules the execution of a test group run at the time that the user specified. It is fired by a business rule on the Test Group Run table.|
|Script action: Execute test group run on specific time|Runs asynchronously when the event fires. If the test group run is still Scheduled, it sets the state to New.|
|Clean-up rule on the Test Run table|Deletes test runs in the Cancelled, Completed, or Failed state 30 days after they were created, together with records that depend on them.|
|Decision tables|Two decision tables decide whether the Diagnose tab and the Run diagnostics panel appear on a record, based on the table and state of the record.|

