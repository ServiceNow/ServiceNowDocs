---
title: Run your first scan with the Scan Engine
description: An initial full Scan Engine completion is required to set a baseline from a series of tasks performed that tune the instance environment to complete future scans quickly and efficiently.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-08-28"
reading_time_minutes: 2
breadcrumb: [Configure the Impact Store Application, Configuring Impact, Impact]
---

# Run your first scan with the Scan Engine

An initial full Scan Engine completion is required to set a baseline from a series of tasks performed that tune the instance environment to complete future scans quickly and efficiently.

## Before you begin

[Activate Scan Engine and review settings](configure-initial-scan-engine-settings.md) before beginning this task.

You can complete the configuration steps directly in the Guided Setup interface or can configure the properties using the indicated navigation path.

**Important:** Depending on the size of your instance, your first scan could take a few hours to complete. We recommend running your first scan overnight, especially in production instances.

Role required: impact admin role or admin

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Platform Health** &gt; **Scheduled Scan**.

2.  Select **Execute Now**.

    The scan progress is tracked within Platform Health.

3.  Navigate to **All** &gt; **Impact** &gt; **Platform Health** &gt; **Scan Engine** &gt; **Scan Status**.

    See [Analytics Dashboards](../concept/scan-engine-diagnostic-dashboards.md):

    -   View the different charts and reports available at **Impact****Platform Health****Analytics Dashboard**.
    -   Access refreshed Health Scan engine dashboards each time a scan is completed.
    The Scan Engine results display with the status of each table that is being scanned.

4.  **Mark as Complete** to progress to the next step in Guided Setup.


## What to do next

Configure the Impact Store Application and import data from the Impact Delivery Instance. See [Run the Service Exchange pre-configuration scan](perform_pre_configuration_health_checks_impact_store_app.md) for next steps.

After the Impact Store Application is configured, you can integrate with your other environments running Impact and utilize Scan Engine diagnostics. A one-time configuration, available in both Basic Auth and OAuth 2.0, is required to connect your instances. See [Scan Engine integrations](../concept/instance-integration-scan-engine.md) for details.

**Parent Topic:**[Configure the Impact Store Application](../concept/configuring-impact-platform.md)

**Previous topic:**[Activate Scan Engine and review settings](configure-initial-scan-engine-settings.md)

**Next topic:**[Run the Service Exchange pre-configuration scan](perform_pre_configuration_health_checks_impact_store_app.md)

