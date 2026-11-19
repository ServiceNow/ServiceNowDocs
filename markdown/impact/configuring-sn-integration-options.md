---
title: Configure ServiceNow user story integration
description: Configure the ServiceNow instance user story integration to create stories in a production instance directly from finding records on a non-production instance.The following leading practices are guidelines for creating ServiceNow integration scripts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/impact/configuring-sn-integration-options.html
release: zurich
topic_type: task
last_updated: "2026-07-27"
reading_time_minutes: 2
breadcrumb: [User story integration, Scan Engine integrations, Scan Engine, Platform Health, Using Impact, Impact]
---

# Configure ServiceNow user story integration

Configure the ServiceNow instance user story integration to create stories in a production instance directly from finding records on a non-production instance.

## Before you begin

-   My SN Instances registration and validation must be complete for each instance in this integration. A source instance \(such as development\) and target instance \(such as production\) must be declared and validated. If those instances aren't created and validated, the stories will not be created in the target instance. See [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/register-your-instance.md).
-   The User Story Table must exist on both the source and target instances before configuring field mappings.

Role required: Scan Engine Admin \(sn\_se.scan\_engine\_admin\).

## Procedure

1.  Navigate to **ALL** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties** and select the **User Story Integration** properties tab.

2.  Set **Integration Type** to `ServiceNow instance`.

3.  Set the **User Story Table**.

    This table must exist on both the source and target instances.

4.  Define field mappings in **User Story Field Mapping**.

    The mapping script executes once on the Source instance and once on the Target instance. Use the available script variables to control behavior in each context. See [ServiceNow integration script leading practices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/configuring-sn-integration-options.md) guidance on writing effective field mapping scripts.


## ServiceNow integration script leading practices

The following leading practices are guidelines for creating ServiceNow integration scripts.

-   First, check the predefined variable isSourceto ensure that the script executes within the Source environment. Then check the predefined variable isDestination to ensure that the script is being executed in the Destination instance \(usually Production\).
-   The predefined variable payload is an object that can be used to store variables so that they are available in the Destination instance. You should load the payload with data when the script is executing on the Source instance, and extract the payload data when the script is executing on the Destination instance.
-   Use Violation in the script only when it is executing in the Source instance.
-   Use grTaskin the script only when it is executing in the Destination instance.
-   Use isSource in the script only when it is executing in the Source instance.
-   Use isDestination in the script only when it is executing in the Destination instance.
-   The payload object can be used regardless of the environment.

The predefined variables available for ServiceNow integrations are:

<table id="table_vgz_hzx_2hc"><tbody><tr><td>

isSource

</td><td>

True when on the Source instance \(Development\).

</td></tr><tr><td>

isDestination

</td><td>

True when on the Destination instance \(Production\).

</td></tr><tr><td>

payload

</td><td>

The user-defined variable that passes information between the instances.

</td></tr><tr><td>

grFinding

</td><td>

The glide record of the finding that sends the request, on the Defined instance in Source only.

</td></tr><tr><td>

grTask

</td><td>

The glide record being created on the Destination instance.

</td></tr></tbody>
</table>