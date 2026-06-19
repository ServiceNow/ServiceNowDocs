---
title: Configure ServiceNow user story integration
description: Configure the ServiceNow instance user story integration to create stories in a production instance directly from finding records on a non-production instance.TScript variables and leading practices for writing field mapping scripts in the ServiceNow instance user story integration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/configuring-sn-integration-options.html
release: australia
product: Impact
classification: impact
topic_type: task
last_updated: "2026-05-05"
reading_time_minutes: 2
breadcrumb: [User story integration, Scan Engine integrations, Configure the Impact Store Application, Configuring Impact, Impact]
---

# Configure ServiceNow user story integration

Configure the ServiceNow instance user story integration to create stories in a production instance directly from finding records on a non-production instance.

## Before you begin

-   My SN Instances registration and authentication must be complete. See [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/register-your-instance.md).
-   The User Story Table must exist on both the source and target instances before configuring field mappings.

Role required: Scan Engine Admin \(sn\_se.scan\_engine\_admin\).

## Procedure

1.  Navigate to **ALL** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties** and select the **User Story Integration** properties tab.

2.  Set **Integration Type** to `ServiceNow instance`.

3.  Set the **User Story Table**.

    This table must exist on both the source and target instances.

4.  Define field mappings in **User Story Field Mapping**.

    The mapping script executes once on the Source instance and once on the Target instance. Use the available script variables to control behavior in each context. See [ServiceNow integration script leading practices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configuring-sn-integration-options.md) guidance on writing effective field mapping scripts.


**Parent Topic:**[User story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/user-story-integration-properties.md)

## ServiceNow integration script leading practices

TScript variables and leading practices for writing field mapping scripts in the ServiceNow instance user story integration.

### Script variables

The field mapping script executes twice, once on the Source \(Development\) instance and once on the Destination \(Production\) instance. Use the `isSource` and `isDestination` variables to scope logic appropriately for each context.

|Variable|Description|
|--------|-----------|
|`isSource`|True when executing on the Source \(Development\) instance.|
|`isDestination`|True when executing on the Destination \(Production\) instance.|
|`payload`|User-defined variable for passing data between instances.|
|`grFinding`|GlideRecord of the finding. Available on the Source instance only.|
|`grTask`|GlideRecord of the task being created on the Destination instance.|

### Leading practices

-   **Scope logic by instance context**

    Always wrap Source-side logic in `if (isSource)` and Destination-side logic in `if (isDestination)`. The script runs in both contexts — accessing `grFinding` on the Destination instance will fail because the finding record does not exist there.

-   **Use payload to pass data across instances**

    Populate `payload` on the Source instance with any values you need on the Destination. For example, set `payload.shortDescription = grFinding.short_description` on the Source, then read `payload.shortDescription` on the Destination to set the task field.

-   **Enable ES12 mode for modern JavaScript**

    To use modern JavaScript syntax such as arrow functions, destructuring, or template literals, enable **ECMAScript 2021 \(ES12\) mode** in Scan Engine Properties before writing your mapping script.

-   **Validate field existence before mapping**

    Confirm that all target fields in `grTask` exist on the User Story Table in the production instance. Mapping to a non-existent field fails silently and the value is discarded.


