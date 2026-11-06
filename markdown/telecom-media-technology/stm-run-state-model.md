---
title: Test group run and test run states
description: Test group runs and test runs move through system-controlled states. The state determines what the system does next, what an external system can update, and when records are deleted.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/stm-run-state-model.html
release: australia
topic_type: concept
last_updated: "2026-10-13"
reading_time_minutes: 3
keywords: [test group run state, test run state, state transitions, scheduled]
breadcrumb: [Explore, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Test group run and test run states

Test group runs and test runs move through system-controlled states. The state determines what the system does next, what an external system can update, and when records are deleted.

The **State** field of a test group run and of a test run is read-only on the form. The system, a flow, or an external system changes it.

## Test group run states and transitions

A test group run has seven states. The default state is Draft.

|State|Meaning|
|-----|-------|
|Draft|The test group run is created but not started. This is the default.|
|Scheduled|The test group run is created with a scheduled time and is waiting for that time.|
|New|The test group run is ready to run. Execution starts from this state. See [Test group run in Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-group-run-initiation.md).|
|Pending for input, In progress, Cancelled, Completed|The test group run is waiting for input, running, stopped before it finished, or finished.|

|From|To|What causes it|
|----|---|--------------|
|Draft|Scheduled|The test group run is created with a scheduled time. The business rule **Add schedule run event to queue** sets the state and queues a timed event.|
|Draft|New|You start the run from a workspace without a scheduled time. The system sets the state immediatly.|
|Scheduled|New|The scheduled time arrives. The script action **Execute test group run on specific time**sets the state, but only if the state is still Scheduled. The script action runs in the background.|
|New|Other states|The flows that run the test group run set the next states.|

## Test run states

A test run has ten states. The default state is New. The result of a test run is a separate field with the values Pass, Fail, Inconclusive, and Timed out.

|State|Meaning|
|-----|-------|
|Draft|The test run is prepared but not started. The workspace or the Automated test run creation tool subflow create test runs in this state. The Execute Test Group flow processes the draft test runs of a test group run.|
|New|The default state of a test run that is created without one.|
|Acknowledged|Test runs in this state appear in the Scheduled list under Test Runs in the application menu.|
|Pending for Input, Rejected, Pending, In progress|The test run is waiting for input, was rejected, is waiting, or is running.|
|Cancelled, Completed, Failed|The test run has ended. The system deletes test runs in these states 30 days after they were created.|

An external system can set the state of a test run when it updates the test run through the Service Test Management Open API \(TMF 653\). See [Test run execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-run-execution.md).

## State rules and constraints

-   A test group run can reference only a published test group, and a test run can reference only a published test definition.
-   A scheduled test group run starts only if its state is still Scheduled when the scheduled time arrives.
-   The Execute Test Group flow processes only the draft test runs of a test group run.
-   The system deletes test runs in the Cancelled, Completed, or Failed state 30 days after they were created.
-   The system doesn't let you close a diagnostic task that is marked Automated.

**Related topics**  


[Service Test Management automation framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-automation-framework.md)

[States and choice values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-states-choices.md)

