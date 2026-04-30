---
title: Quick start tests for multicurrency in Next Experience for Demand Management
description: Validate that multicurrency in Next Experience for Demand Management works correctly after making configuration changes such as applying an upgrade or developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: zurich
product: Portfolio Planning
classification: portfolio-planning
topic_type: concept
last_updated: "2026-03-03"
reading_time_minutes: 1
breadcrumb: [Multicurrency, Configure, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Quick start tests for multicurrency in Next Experience for Demand Management

Validate that multicurrency in Next Experience for Demand Management works correctly after making configuration changes such as applying an upgrade or developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.

**Danger**

By default, the system property that is used to run automated tests is disabled to prevent you from accidentally running these tests on a production system. To avoid data corruption or an outage, run tests only on development, test, and other non-production instances. See [Enable or disable executing Automated Test Framework tests](https://www.servicenow.com/docs/access?context=atf-enable-tests&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

Activate the PPM Standard Multicurrency – ATF Tests plugin \(com.snc.ppm\_multicurrency.atf\) to use demand currency quick start tests.

|Test|Description|
|----|-----------|
|Verify cost in demand currency on cost plan|Validates the calculation of cost plan breakdown with budget reference rate and verifies the roll up to cost plan in demand currency.|
|Verify benefit in demand currency on benefit plan|Validates the calculation of benefit plan breakdown with budget reference rate and verifies the roll up to benefit plan in demand currency.|

**Related topics**  


[Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=zurich&pubname=zurich-application-development&ft:locale=en-US)

