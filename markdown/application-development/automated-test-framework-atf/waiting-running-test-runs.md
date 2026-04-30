---
title: Waiting/running test runs
description: The Waiting/Running Test Run module opens a list of records showing the tests waiting to be run.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Run, Reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Waiting/running test runs

The Waiting/Running Test Run module opens a list of records showing the tests waiting to be run.

**Note:** To prevent conflicts, the system allows only one test to run at a given time. This is true even if you have multiple client test runner windows open. If you submit tests to run when another test is already running, the system holds the new tests in a queue to run later. If a test remains in the queue for more than ten minutes, the system cancels the test.

You can [cancel execution of a waiting automated test](atf-cancelling.md#).

**Parent Topic:**[Run](run-module.md)

