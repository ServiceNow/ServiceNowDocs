---
title: Create a serverless schedule for Microsoft Certificate Authority \(CA\) discovery
description: Create a serverless discovery schedule to discover Microsoft Certificate Authority \(CA\) certificates.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2025-03-17"
reading_time_minutes: 3
breadcrumb: [Microsoft CA certificates, Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Create a serverless schedule for Microsoft Certificate Authority \(CA\) discovery

Create a serverless discovery schedule to discover Microsoft Certificate Authority \(CA\) certificates.

## Before you begin

-   Verify that the CA process is up and running on the host machine.
-   Verify that a Windows host was discovered during a previous horizontal discovery. For more information, see [Windows discovery](../../discovery/reference/r_DataCollDiscoWindowsComputers.md).

Role required: discovery\_admin

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Schedules**.

2.  Create the discovery schedule record.

    1.  Select **New**.

    2.  On the form, fill in the fields.

<table id="table_fqm_2f4_vcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for this discovery schedule. For example: Discover MS CA.

</td></tr><tr><td>

Discover

</td><td>

Scan type, which should be Certificates.

</td></tr><tr><td>

Certificate Discovery Type

</td><td>

Certificate type, which should be CA Trust Discovery.

</td></tr><tr><td>

MID server

</td><td>

Name of the MID Server to use for this schedule.

</td></tr><tr><td>

Active

</td><td>

Enables this schedule for discovery.

</td></tr></tbody>
</table>    3.  Select **Submit**.

3.  Create the execution pattern.

    1.  In the Discovery Schedules page, select the record you created.

    2.  In the **Serverless Execution Patterns** tab, select **New**.

        Discovery uses each execution pattern to discover up to 20,000 certificates. For deployments using more than 20,000 certificates, create several execution patterns.

    3.  On the form, fill in the fields.

<table id="table_e3x_tpx_r2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name for this record. For example: Discover MS CA.

</td></tr><tr><td>

Pattern

</td><td>

Pattern to be used for this schedule, which should be the Microsoft CA - Certificate Management pattern.

</td></tr><tr><td>

Proxy Host

</td><td>

CI name of the Windows host running the Microsoft CA Service, discovered in a previous discovery and populated in the CMDB.

</td></tr><tr><td>

Active

</td><td>

Option to enable this schedule for discovery.

</td></tr></tbody>
</table>    4.  Select **Submit**.

4.  Set the pattern launcher parameters.

    1.  In the **Discovery Pattern Launcher Parameters** tab, select the record you created.

    2.  On the form, fill in the fields.

<table id="table_wmm_xpx_r2c"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

template\_list

</td><td>

Determines whether to search on all the request IDs or a template ID to discover certificates. Possible values are **all** or the template ID number.-   all: Restricts discovery to all certificate request IDs in ascending order.

The request IDs are limited either by the default execution pattern limitation of 20,000 or values set in **start\_offset** or **limit**.

-   Template ID: Searches for certificates only in the specific template ID. Can be a single template ID or multiple IDs, separated by commas.

For example: 1.2.3.4,5.6.7.8,9.10.11.12

</td></tr><tr><td>

start\_offset

</td><td>

This optional parameter specifies the number of the certificate from which to start discovery and is relevant only when **template\_list** is set to all and for deployments with over 20,000 certificates. If you create multiple serverless execution patterns for deployments with over 20,000 certificates, use 1 for the first execution, 20001 for the second, and so on.

If this parameter remains empty, **start\_offset** defaults to 1.

</td></tr><tr><td>

limit

</td><td>

This optional parameter limits the certificate discovery to the specified value and is relevant only when **template\_list** is set to all. If the parameter remains empty, the limit defaults to 20,000 certificates.

</td></tr><tr><td>

ip

</td><td>

IP of the server on which the CA process \(certsrv\) is running.

</td></tr><tr><td>

discover\_SAN\_for\_template

</td><td>

When set to true, this optional parameter enables the discovery of the subject alternative name \(SAN\) of the certificates when a template ID is provided in the **template\_list** parameter.This parameter executes separate commands for each certificate within the template ID, which could impact performance.

When searching on all request IDs, SAN is automatically discovered, so this parameter should remain empty.

</td></tr></tbody>
</table>    3.  Select **Submit**.


## What to do next

Either execute discovery immediately by selecting **Discover now** or wait until the predefined schedule triggers the discovery.

**Parent Topic:**[Microsoft Certificate Authority \(CA\) certificates discovery](../reference/microsoft-ca-discovery.md)

**Related topics**  


[Microsoft Certificate Authority \(CA\) certificates discovery](../reference/microsoft-ca-discovery.md)

