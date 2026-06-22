---
title: Filter ADOM discovery for the Fortinet Service Graph Connector
description: Restrict which Fortinet ADOMs the SGC discovers by activating the predefined Vodafone filter or by providing your own implementation of the ADOM filter extension point.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/filter-fortinet-sgc-adoms.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-06-22"
reading_time_minutes: 1
breadcrumb: [Configure Fortinet SGC, Configure Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Filter ADOM discovery for the Fortinet Service Graph Connector

Restrict which Fortinet ADOMs the SGC discovers by activating the predefined Vodafone filter or by providing your own implementation of the ADOM filter extension point.

## Before you begin

Role required: `tsom_visibility_admin`

## About this task

By default, the SGC for Fortinet discovers all ADOMs returned by FortiManager. To restrict discovery to a subset of ADOMs based on their properties, use the `sn_sgc_fortinet.FortinetCustomizedAdomFilter` extension point. An implementation defines a `shouldIncludeAdom(adom)` handler that returns `true` to discover the ADOM or `false` to skip it, where `adom` is the ADOM object returned by the Fortinet API.

A predefined implementation, `FortinetDefaultAdomFilter`, is provided for Vodafone deployments. It discovers only ADOMs where the **VF SDWAN Service Provided** meta field equals `yes` and the **restricted\_prds** property equals `fabric`. This implementation is inactive by default, so it doesn't affect discovery unless you activate it.

**Warning:** Activate the predefined filter only if your FortiManager deployment populates the required meta fields. If you activate it without them, no ADOM matches the filter and discovery returns no data.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Extension Instances**.

2.  Filter the list by **Point** equals `sn_sgc_fortinet.FortinetCustomizedAdomFilter`.

3.  Open the **FortinetDefaultAdomFilter** record.

4.  Set **Active** to true and save the record.

    The SGC applies the filter at the next polling cycle and discovers only the ADOMs that satisfy it.


## What to do next

To apply your own filtering logic instead, create an implementation of the `sn_sgc_fortinet.FortinetCustomizedAdomFilter` extension point in your own scope, define the `shouldIncludeAdom(adom)` handler, and activate its extension instance. Leave the predefined `FortinetDefaultAdomFilter` instance inactive.

