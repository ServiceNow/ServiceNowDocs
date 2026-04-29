---
title: Running Schedule Optimization jobs for large workloads
description: Run Schedule Optimization as multiple jobs for large workloads.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Running Schedule Optimization jobs for large workloads

Run Schedule Optimization as multiple jobs for large workloads.

For large workloads, Schedule Optimization runs as multiple jobs rather than one job at a time. The jobs use available ML trainers to process portions of the territories or assignment groups, reducing total processing time for large workloads.

Batch, intraday, and prioritized optimization are supported. On‑demand optimization is not supported.

Split qualifiers are a configuration setting that controls whether Schedule Optimization creates multiple jobs for a single run. Configure how Schedule Optimization processes large workloads by using the following system properties:

-   `sn_schedule_optim.qualifier_distribution`
-   `sn_schedule_optim.qualifier_distribution_splits`

By default, Schedule Optimization supports three concurrent jobs. For information about adjusting this limit, see the `sn_schedule_optim.so_max_solution_threshold` property description.

For property descriptions and supported values, see [Schedule Optimization properties](../reference/schedule-optimization-properties.md).

## When to use split qualifiers

Consider enabling split qualifiers when:

-   You're optimizing large numbers of territories or work orders
-   You want to process optimization workloads faster
-   Your instance has ML trainer capacity available

## When not to use split qualifiers

Don't enable split qualifiers when:

-   Workloads are small and current optimization times are acceptable
-   Your instance has limited ML trainer capacity

**Note:**

When data sets are small, splitting qualifiers may add extra processing without improving performance.

## Use cases

## Batch optimization times out before processing is finished

**Scenario:** Nightly batch optimizations for multiple territories consistently times out before completion.

**Solution:** Enable split qualifiers for batch optimization with 2-3 splits to distribute the workload across parallel jobs. Each job completes within the timeout threshold.

## Intraday optimization performance is degrading

**Scenario:** Your intraday optimization configuration includes many qualifiers with high event volumes, causing optimization jobs to take longer than expected.

**Solution:** Enable split qualifiers for intraday optimization to distribute qualifiers across multiple parallel jobs. Each job processes fewer qualifiers and completes faster.

## Accommodate higher processing volumes

**Scenario:** Your organization expands the number of territories used, and optimization times increase beyond acceptable thresholds.

**Solution:** Enable split qualifiers for both batch and intraday optimization, incrementally increasing split count as needed to maintain acceptable optimization times.

