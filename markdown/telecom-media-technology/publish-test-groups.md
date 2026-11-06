---
title: Publish a test group
description: Publish a test group so that you can relate it to a specification or a product model and your teams see only approved test groups.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/publish-test-groups.html
release: australia
topic_type: task
last_updated: "2026-10-23"
reading_time_minutes: 1
keywords: [publish test group, test group state]
breadcrumb: [Setting up a test group, Setting up test configuration records, Configure, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Publish a test group

Publish a test group so that you can relate it to a specification or a product model and your teams see only approved test groups.

## Before you begin

The test group must be in the Draft state.

A manual test group needs at least one test definition. For more information, see [Map test definitions to a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/add-test-definitions-to-test-group.md).

Role required: sn\_st\_mgmt.test\_def\_manager

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Groups** &gt; **All**.

2.  Select the test group that you want to publish.

3.  Select **Publish**.


## Result

The state of the test group changes from Draft to Published. You can't change its definition mappings or its execution type after it's published.

## What to do next

Relate the published test group to a specification or a product model. See [Associate a test group to a specifications or product model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/define-relationship-test-group-specifications.md).

