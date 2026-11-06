---
title: Publish a test definition
description: Publish a test definition in the Service Test Management application so that test runs can reference it and your teams see only approved tests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/publish-test-specification-spm.html
release: australia
topic_type: task
last_updated: "2026-10-23"
reading_time_minutes: 1
keywords: [publish test definition, test definition state]
breadcrumb: [Setting up test definitions, Setting up test configuration records, Configure, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Publish a test definition

Publish a test definition in the Service Test Management application so that test runs can reference it and your teams see only approved tests.

## Before you begin

The test definition must be in the Draft state.

Role required: sn\_st\_mgmt.test\_def\_manager

## About this task

You can publish a test definition that has no test measure definitions.

With the Product Model plugin active, the system also validates the characteristics of the test definition. A characteristic with options requires a unique, valid option. A characteristic without options must have no option set. See [Test Characteristic form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-characteristic-fields.md).

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Definitions** &gt; **All**.

2.  Select the draft test definition that you want to publish.

3.  Select **Publish**.


## Result

The state of the test definition changes from Draft to Published, and the definition is locked. You can't change the definition or its related records while it's published.

To change a published test definition, copy it and edit the draft copy. See [Copy a test definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/copy-test-definition.md). For more information about the test definition states, see [Test definitions in Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-definition-stm.md).

