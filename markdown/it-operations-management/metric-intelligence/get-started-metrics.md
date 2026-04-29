---
title: Get started with Metric Intelligence
description: Complete the following setup and initial configuration steps to start using Metric Intelligence.
locale: en-US
release: australia
product: Metric Intelligence
classification: metric-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# Get started with Metric Intelligence

Complete the following setup and initial configuration steps to start using Metric Intelligence.

## Before you begin

Activate the Metric Intelligence plugin \(com.snc.sa.metric\).

Role required: evt\_mgmt\_admin

## About this task

Metrics have an expiration date. You can continue receiving data without interruption when a metric’s expiration date arrives by pushing ahead the expiration date. For details, contact customer support.

Metric Intelligence guided setup provides a sequence of tasks that help you configure Metric Intelligence on your ServiceNow instance. To open Metric Intelligence guided setup, navigate to **Guided Setup** &gt; **ITOM Guided Setup**, and click **Continue**. Then scroll to **Metric Intelligence**, and click **Continue**. For more information about using the guided setup interface, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

Alternatively, you can complete the following procedure.

## Procedure

1.  Configure a MID Server for Metric Intelligence.

    For details, see [MID Server and MID Server distributed cluster for Metric Intelligence](../concept/ops-intelligence-mid-server.md).

2.  Use the [Automated Metric Intelligence setup](auto-setup.md).

3.  [Choose a source for collecting metrics](../../agent-client-collector/concept/metric-collection-sources.md).

4.  [Choose and configure metrics to monitor](configure-metric-monitors.md).

5.  [Create event rules to map raw metric data to specific CIs](../concept/event-rule-bind-metrics-to-ci.md) and [Create an event rule to bind metric events to host CIs](event-rule-bind-metrics-to-host.md).

6.  About 10 minutes after the Metric Intelligence Metrics extension has started, run the [quick start tests for Metric Intelligence](../../../administer/atf-quick-start-tests/reference/quick-start-tests-ops-intelligence.md) to verify functionality.


