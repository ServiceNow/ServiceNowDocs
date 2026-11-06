---
title: Archive test definitions
description: Archive retired test definitions in the Service Test Management application to take them out of the working list.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/archive-test-definitions.html
release: australia
topic_type: task
last_updated: "2026-10-13"
reading_time_minutes: 1
keywords: [archive test definition, retired test definition]
breadcrumb: [Setting up test definitions, Setting up test configuration records, Configure, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Archive test definitions

Archive retired test definitions in the Service Test Management application to take them out of the working list.

## Before you begin

The test definitions must be in the Retired state. See [Retire test definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/retire-test-definition.md).

Role required: sn\_st\_mgmt.test\_def\_manager

## About this task

You can archive several test definitions at once from the list.

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Definitions** &gt; **All**.

2.  Select the check box for each retired test definition that you want to archive.

3.  In the list actions, select **Archive**, and then confirm.


## Result

The state of each test definition changes from Retired to Archived.

A test definition that a published test definition uses as a related test definition isn't archived. The system shows a message that names the definitions it skipped.

**Related topics**  


[Test definitions in Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-definition-stm.md)

