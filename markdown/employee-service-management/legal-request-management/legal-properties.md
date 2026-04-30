---
title: Legal Service Delivery properties
description: There are several properties that you can use to configure integrations for Legal Service Delivery apps.
locale: en-US
release: yokohama
product: Legal Request Management
classification: legal-request-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Legal Request Management, Legal Service Delivery, Employee Service Management]
---

# Legal Service Delivery properties

There are several properties that you can use to configure integrations for Legal Service Delivery apps.

These properties are available for Legal Service Delivery.

**Note:** To configure these properties, navigate to **All** &gt; **Legal Administration** &gt; **Legal Integrations** &gt; **Properties**.

<table id="table_zpv_stv_b5b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

External Storage section

</td></tr><tr><td>

Maximum number of attempts before removing the permission records with errors

 sn\_lg\_ops.external\_storage\_clear\_errored\_records\_after

</td><td>

The number of retries permitted before removing all errored permission entries from the job execution queue.

 -   Type: integer
-   Default value: 5
-   Learn more: [Configure an external storage system for legal requests and legal matters](../task/integrate-legal-ext-storage.md)

</td></tr><tr><td>

Time in minutes to retry permission records execution

 sn\_lg\_ops.integration\_retry\_after

</td><td>

The amount of time the system waits in minutes before retrying to execute permission records.

 -   Type: integer
-   Default value: 20
-   Learn more: [Configure an external storage system for legal requests and legal matters](../task/integrate-legal-ext-storage.md)

</td></tr><tr><td>

Maximum number of permission records to include in a job execution

 sn\_lg\_ops.integration\_external\_storage\_job\_batch\_limit

</td><td>

The number of permission records that can be included in single job execution.

 -   Type: integer
-   Default value: 30
-   Learn more: [Configure an external storage system for legal requests and legal matters](../task/integrate-legal-ext-storage.md)

</td></tr><tr><td>

Maximum number of failed calls before marking the flow status as errored

 sn\_lg\_ops.integration\_retry\_record\_threshold

</td><td>

The maximum number of failed job execution calls permitted before the flow status is marked as errored.

 -   Type: integer
-   Default value: 5
-   Learn more: [Configure an external storage system for legal requests and legal matters](../task/integrate-legal-ext-storage.md)

</td></tr><tr><td class="sub-head" colspan="2">

Legal Integration Core section

</td></tr><tr><td>

IntegrationCore script schema override

 sn\_lg\_ops.integration\_schema\_overrides

</td><td>

Your custom schema structure, which takes precedence over the schema in the IntegrationCore script. You can use an existing schema structure from the IntegrationCore script as a starting point for creating your schema structure.

 -   Type: string
-   Default value: \{\}

</td></tr></tbody>
</table>The property is available for Legal Request Management.

**Note:** To configure the property, navigate to **All** &gt; **Legal Administration** &gt; **Legal Request Management** &gt; **Properties**.

<table id="table_tt1_db3_dwb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_lg\_ops.allow\_request\_closure\_with\_open\_matters

</td><td>

The property allows the closure of a legal request even if it has open matters associated.

 -   Type: boolean
-   Default value: false

</td></tr></tbody>
</table>**Parent Topic:**[Legal Request Management reference](legal-request-management-reference.md)

