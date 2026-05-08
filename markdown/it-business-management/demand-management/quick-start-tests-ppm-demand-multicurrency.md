---
title: Quick start tests for Multicurrency in Demand Management
description: Validate that the multicurrency in Demand Management still works after you make any configuration change such as applying an upgrade or developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: australia
product: Demand Management
classification: demand-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Multicurrency, Configure, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Quick start tests for Multicurrency in Demand Management

Validate that the multicurrency in Demand Management still works after you make any configuration change such as applying an upgrade or developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.

**Danger**

By default, the system property that is used to run automated tests is disabled to prevent you from accidentally running these tests on a production system. To avoid data corruption or an outage, run tests only on development, test, and other non-production instances. See Enable or disable executing Automated Test Framework tests.

Demand currency quick start tests require activating the PPM Standard Multicurrency – ATF Tests plugin \(com.snc.ppm\_multicurrency.atf\).

|Test|Description|Release version|
|----|-----------|---------------|
|Verify cost in demand currency on cost plan|Validate the calculation of cost plan breakdown with budget reference rate and verify the roll up to cost plan in demand currency.|Quebec|
|Verify benefit in demand currency on benefit plan|Validate the calculation of benefit plan breakdown with budget reference rate and verify the roll up to benefit plan in demand currency.|Quebec|

**Parent Topic:**[Multicurrency in Demand Management](../../../product/planning-and-policy/concept/multicurrency-demand.md)

**Related topics**  


[bundle-cadev.quick-start-tests]

