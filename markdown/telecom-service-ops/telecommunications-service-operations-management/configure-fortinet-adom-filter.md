---
title: Filter ADOMs for the Fortinet pull connector
description: Additional filter conditions required in Fortinet pull connector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/configure-fortinet-adom-filter.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-06-19"
reading_time_minutes: 1
breadcrumb: [Configure Fortinet SGC, Configure Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Filter ADOMs for the Fortinet pull connector

Additional filter conditions required in Fortinet pull connector.

## Before you begin

Role required: `tsom_visibility_admin`

## About this task

By default, the Fortinet pull connector collects metric data from all ADOMs. To limit collection to ADOMs that meet specific conditions, configure the following parameters on the connector instance \(for example, **Fortinet SD-WAN SLA Log**\):

|Parameter|Default|Description|
|---------|-------|-----------|
|`adomFilterEnabled`|`false`|Turns ADOM filtering on or off. When `false`, the connector collects all ADOMs and the filter is bypassed. When `true`, the connector collects only the ADOMs that the filter class accepts.|
|`adomFilterClass`|`FortinetAdomFilterVF`|Name of the MID Server script include that implements the filter. Evaluated only when `adomFilterEnabled` is `true`. The class must be active, deployed to the MID Server, and expose a `shouldIncludeAdom(adomData)` handler that returns a Boolean.|

Two filter classes are provided:

-   `FortinetAdomFilterVF` \(default\) collects only ADOMs where the `restricted_prds` property equals `fabric` and the `VF SDWAN Service Provided` meta field equals `yes`.
-   `FortinetAdomFilter` collects all ADOMs unconditionally.

**Warning:** Filtering fails closed. If you set `adomFilterEnabled` to `true` and `adomFilterClass` is not a valid script include that is deployed to the MID Server, all ADOMs are blocked and metric collection stops. Enable filtering only when the named class populates the conditions your FortiManager deployment supports.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Connectors**.

2.  Open the Fortinet pull connector instance.

3.  On the **Additional Parameters** related list, set `adomFilterEnabled` to `true`.

4.  Set `adomFilterClass` to the name of the filter class you want to apply.

    Use `FortinetAdomFilterVF` for the Vodafone filter, `FortinetAdomFilter` to collect all ADOMs, or the name of a custom filter class.

5.  Save the connector instance.

    The connector applies the filter at the next polling cycle and collects metric data only from the ADOMs that the filter class accepts.


## What to do next

To apply your own filtering logic, create a MID Server script include \(`ecc_agent_script_include`\) that exposes a `shouldIncludeAdom(adomData)` handler returning `true` to collect the ADOM or `false` to skip it, deploy it to the MID Server, and set `adomFilterClass` to its name.

