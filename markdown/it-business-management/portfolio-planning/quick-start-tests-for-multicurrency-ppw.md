---
title: Quick start tests for multicurrency in Next Experience for Demand Management
description: Quick tests enable you to validate that the multicurrency feature in Next Experience for Demand Management works correctly after configuration changes such as applying an upgrade or developing an application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-planning/quick-start-tests-for-multicurrency-ppw.html
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Multicurrency in demands, Configure, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Quick start tests for multicurrency in Next Experience for Demand Management

Quick tests enable you to validate that the multicurrency feature in Next Experience for Demand Management works correctly after configuration changes such as applying an upgrade or developing an application.

**Danger**

By default, the system property that is used to run automated tests is turned off to prevent you from accidentally running these tests on a production system. To avoid data corruption or an outage, run tests only on development, test, and other non-production instances. See Enable or disable executing Automated Test Framework tests.

To use demand currency quick start tests, the PPM Standard Multicurrency – ATF Tests plugin \(com.snc.ppm\_multicurrency.atf\) must have been activated.

For information about copying and then customizing quick start tests, see .

|Test|Description|
|----|-----------|
|Verify cost in demand currency on cost plan|Validates the calculation of cost plan breakdown with budget reference rate. Verifies the roll up to cost plan in demand currency.|
|Verify benefit in demand currency on benefit plan|Validates the calculation of the benefit plan breakdown with the budget reference rate. Verifies the roll up to benefit plan in demand currency.|

**Related topics**  


[bundle-cadev.quick-start-tests]

