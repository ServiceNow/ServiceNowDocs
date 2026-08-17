---
title: Configure Fortinet ADOM for connector instance
description: Configure a connector instance to poll a specific Fortinet ADOM for metric data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/configure-fortinet-allowlist.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Configure Fortinet SGC, Configure Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Configure Fortinet ADOM for connector instance

Configure a connector instance to poll a specific Fortinet ADOM for metric data.

## Before you begin

Role required: tsom\_visibility\_admin

## About this task

Each connector instance polls a single ADOM. To collect data from multiple ADOMs, create multiple connector instances, each configured with a different ADOM value. Distribute connector instances across MID Servers to avoid polling interval overruns in large-scale deployments.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Definitions**.

2.  Search for `Fortinet` in the search field.

3.  Select the connector from the list, then the Connector Instance.

4.  In the **Connector Instance Values** section, specify the ADOM from which you want to receive metric data.

    The connector retrieves logs only for the specified ADOM.

5.  Select **Update**.


## Result

The connector applies these values at each polling cycle.

