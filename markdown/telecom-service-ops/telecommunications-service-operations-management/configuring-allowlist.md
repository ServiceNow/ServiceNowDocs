---
title: Configure Cisco Meraki allowlists
description: Configure connector definitions to limit polling to specific Cisco Meraki organizations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/configuring-allowlist.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-06-21"
reading_time_minutes: 1
breadcrumb: [Configure Cisco Meraki SGC, Configure Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Configure Cisco Meraki allowlists

Configure connector definitions to limit polling to specific Cisco Meraki organizations.

## Before you begin

Role required: tsom\_visibility\_admin

## About this task

Use multiple connector instances with disjoint allowlists to distribute collection across MID Servers and avoid polling interval overruns in large-scale deployments. Only listed entities are included in the polling scope; all others are silently excluded.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Definitions**.

2.  Search for `Meraki` in the search field.

3.  Select the connector from the list, then the connector instance.

4.  In the **organizationsToWhitelist** field in the **Connector Instance Values** section, enter the organization names to be included in the polling scope, separated by commas.

    For example, `CompanyG,Corp,SoutheastRegion`.

5.  Select **Update**.


## Result

The connector applies these values at each polling cycle.

