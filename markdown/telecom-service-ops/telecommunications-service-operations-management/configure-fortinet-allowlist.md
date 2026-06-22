---
title: Configure Fortinet allowlist
description: Configure connector definitions to limit polling to specific Fortinet ADOMs using allowlist settings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/configure-fortinet-allowlist.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-06-22"
reading_time_minutes: 1
breadcrumb: [Configure Fortinet SGC, Configure Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Configure Fortinet allowlist

Configure connector definitions to limit polling to specific Fortinet ADOMs using allowlist settings.

## Before you begin

Role required: tsom\_visibility\_admin

## About this task

Use multiple connector instances with disjoint allowlists to distribute collection across MID Servers and avoid polling interval overruns in large-scale deployments. Specify the ADOM from which the connector pulls data.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Definitions**.

2.  Search for `Fortinet` in the search field.

3.  Select the connector from the list, then the Connector Instance.

4.  In the **Connector Instance Values** section, specify the ADOM from which you want to receive metric data.

    The connector retrieves logs only for the specified ADOM.

5.  Select **Update**.


## Result

The connector applies these values at each polling cycle.

