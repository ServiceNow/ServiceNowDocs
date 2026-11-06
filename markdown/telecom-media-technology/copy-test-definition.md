---
title: Copy a test definition
description: Copy a test definition to create a draft that you can edit, instead of building a similar test from the start.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/copy-test-definition.html
release: australia
topic_type: task
last_updated: "2026-10-13"
reading_time_minutes: 1
keywords: [copy test definition, duplicate test definition]
breadcrumb: [Setting up test definitions, Setting up test configuration records, Configure, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Copy a test definition

Copy a test definition to create a draft that you can edit, instead of building a similar test from the start.

## Before you begin

The test definition must be saved.

Role required: sn\_st\_mgmt.test\_def\_manager

## About this task

Copying is useful when a test definition is published and therefore locked. For more information about the states, see [Test definitions in Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-definition-stm.md).

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Definitions** &gt; **All**.

2.  Select the test definition that you want to copy.

3.  Select **Copy**.


## Result

The system creates a copy in the Draft state with a new number, and copies these related records:

-   Characteristics, when the Product Model plugin is active.
-   Test definition relationships.
-   Test measure definitions, with their threshold rules and measure consequences.

If a related record can't be copied, the system shows a message that lists the record types.

