---
title: Service Test Request spoke selector
description: Review the request type, its inputs and output, and the request definition that selects the adapter flow that runs a test against an external system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/service-test-request-spoke-selector.html
release: australia
topic_type: reference
last_updated: "2026-10-13"
reading_time_minutes: 1
keywords: [spoke selector, service test request, adapter flow, request definition]
breadcrumb: [Reference, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Service Test Request spoke selector

Review the request type, its inputs and output, and the request definition that selects the adapter flow that runs a test against an external system.

## Request type

The spoke selector uses the Service Test Request as a contract between a test run and the adapter flow that runs it. The contract requires the plugin com.sn\_appss. See [Plugins installed with Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-requirements.md).

|Name|Type|Description|
|----|----|-----------|
|Table Name \(input\)|String, up to 200 characters|The table of the record that the request is about. For a test run, the value is sn\_st\_mgmt\_test.|
|Request Body \(input\)|JSON, up to 4,000 characters|The details of the test to run.|
|Response Body \(output\)|JSON, up to 4,000 characters|The response of the adapter flow.|

The internal name of the request type is sn\_st\_mgmt\_Service\_Test\_Request.

## Request definition

A request definition connects a request type to an adapter. The application installs one request definition.

|Field|Value|
|-----|-----|
|Name|Service Test Demo Request|
|Type|Service Test Request|
|Condition|Table Name is sn\_st\_mgmt\_test|
|Adapter type|Flow|
|Adapter|STM test run demo adapter|
|Order|100|
|Pre-processor and post-processor|Both return their data unchanged.|

The demo adapter simulates a result without an external system, so you can try the framework in a sandbox. To run tests against your own external system, you create a flow from the template and register it as the adapter. See [Service Test Management automation framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-automation-framework.md).

