---
title: Quick start tests for Test Management 2.0
description: Validate that Test Management 2.0 still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: australia
product: Test Management
classification: test-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Test Management 2.0, Test Management applications, Strategic Portfolio Management]
---

# Quick start tests for Test Management 2.0

Validate that Test Management 2.0 still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.

Test Management 2.0 quick start tests require activating the Test Management 2.0 plugin \(com.snc.test\_management.2.0\). and the Test Management 2.0 - ATF Tests plugin \(com.snc.test\_management.2.0.atf\).

|Test|Description|Release version|
|----|-----------|---------------|
|Create test version should create test|Validate test creation and version.|Madrid|
|Should be able to mark test version as ready when it contains verification steps|Validate test state when test has verification steps.|Madrid|
|Should not able to mark test version as ready when it does not contain verification step|Validate test state when test does not have verification steps.|Madrid|
|Marking a test version as ready should retire other test version in ready state|Validate test state when marking test ready.|Madrid|

|Test|Description|Release version|
|----|-----------|---------------|
|When test run closed, should update execution suite progress|Validate execution state progress.|Madrid|
|Should not be able to assign a test not in ready state|Validate test assignment.|Madrid|
|Test progress should roll up for test plan and test cycle|Validate test progress for test plan and test cycle.|Madrid|

**Related topics**  


[Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=australia&pubname=australia-application-development&ft:locale=en-US)

