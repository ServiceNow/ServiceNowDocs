---
title: View transaction data for automated test results
description: To help troubleshoot performance issues with automatic tests, you can inspect related records from the transactions log entry \[syslog\_transaction\] table.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Optimizing automatic test performance, Administering the Automated Test Framework \(ATF\), Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# View transaction data for automated test results

To help troubleshoot performance issues with automatic tests, you can inspect related records from the transactions log entry \[syslog\_transaction\] table.

## Before you begin

Role required: test\_admin or admin

## About this task

**Note:** The system may not be able to log some transactions with short durations.

## Procedure

1.  Navigate to related transaction record in the system transaction log.

    -   From the [Step results record](../reference/atf-step-result-record.md), view transactions in the Step transactions related list.
    -   From the [Test Results record](../reference/atf-test-results-record.md), view transactions in the Test Transactions related list.

**Parent Topic:**[Optimizing automatic test performance](../concept/atf-optimize-perf.md)

