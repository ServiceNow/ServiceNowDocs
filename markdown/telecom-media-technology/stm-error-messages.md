---
title: Service Test Management error messages
description: Find the cause of a Service Test Management error message and the action that resolves it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/stm-error-messages.html
release: australia
topic_type: reference
last_updated: "2026-10-13"
reading_time_minutes: 3
keywords: [service test management errors, troubleshooting, cannot publish test group, cyclical relationship]
breadcrumb: [Reference, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Service Test Management error messages

Find the cause of a Service Test Management error message and the action that resolves it.

## Test group messages

|Message|Cause and resolution|
|-------|--------------------|
|No test definition is associated with this test group. You can not publish it.|A manual test group needs at least one test definition. Add a test definition, or change the execution type to Automated before you publish. See [Map test definitions to a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/add-test-definitions-to-test-group.md).|
|Test group state must be in Draft state.|You can change the definition mappings of a test group only while the group is in the Draft state.|
|Test group state must be in Published state.|Publish the test group before you relate it to a specification or a product model.|
|A record with the same Test Definition and Test Group already exists. Please provide unique values.|The test definition is already mapped to this test group. A definition can be mapped to a group only once.|
|You cannot update the 'Execution Type' field when the state is 'Published'.|Choose the execution type before you publish the test group.|

## Relationship messages

|Message|Cause and resolution|
|-------|--------------------|
|Provide exactly one of Specification or Product Model.|Fill in one of the two fields, not both and not neither.|
|Conditions cannot be set with Product Model; condition scoping is specification-driven.|Use a specification if you want to set conditions. See [Define conditions for a test group relationship](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/define-conditions-for-test-group-relationship.md).|
|Product Model must be populated.|Without the Product Model plugin, a test group relationship needs a product model.|
|A record with the same Product Model and Test Group already exists. Please provide unique values.|The test group already has a relationship for that product model.|
|Invalid update: this relationship creates a cyclical relationship between test definitions.|Choose a related test definition that doesn't lead back to this one.|

## Test definition messages

|Message|Cause and resolution|
|-------|--------------------|
|Related Test Definition can only be added or modified when the test definition is not empty and state is in the draft state.|You can change relationships, test measure definitions, threshold rules, and measure consequences only while the test definition is in the Draft state.|
|This test definition is used in published test definitions. You cannot retire it.|Retirement is blocked while a published test definition uses this one as a related test definition. Remove the relationship first.|
|The following test definition\(s\) are used in published test definitions. So these test def\(s\) won't be retired.|You retired several test definitions from a list, and some are the related definition of a published test definition. The system retires the others and skips these. Remove the relationship from the published definition to retire them.|
|Changing the state from \{0\} to \{1\} is not permitted.|A test definition can't move back to an earlier state. See [Test definitions in Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-definition-stm.md).|
|If Comparator Exact is true Target Exact must be populated.|One of several comparison messages on a threshold rule. Check the comparison rules in [Threshold Rule form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/threshold-rule-fields.md).|

## Other behavior

-   **A test definition doesn't appear when you select one for a test run**

    A test run can reference only a published test definition. Publish the definition first. For more information, see [Publish a test definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/publish-test-specification-spm.md).

-   **Archiving skips some test definitions and names them in a message**

    A test definition that a published definition uses as a related definition isn't archived. For more information, see [Archive test definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/archive-test-definitions.md).


