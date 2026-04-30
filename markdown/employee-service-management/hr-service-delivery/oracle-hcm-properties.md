---
title: Configure properties
description: Once you set up HR Service Delivery integration with Oracle Cloud HCM, the source record for the Oracle HCM Cloud application is automatically created in the Enterprise Service Management Integrations Framework, Source module. The integrations source properties can be used to configure the HR Service Delivery integration with Oracle Cloud HCM.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, HR Service Delivery integration with Oracle Cloud HCM, Integrate with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configure properties

Once you set up HR Service Delivery integration with Oracle Cloud HCM, the source record for the Oracle HCM Cloud application is automatically created in the Enterprise Service Management Integrations Framework, Source module. The integrations source properties can be used to configure the HR Service Delivery integration with Oracle Cloud HCM.

These properties are available for HR Service Delivery integration with Oracle Cloud HCM.

To set the properties, navigate to **Integrations Framework** &gt; **Source** &gt; **Oracle HCM Cloud**.

<table id="table_cv3_kxc_cqb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

workers\_records\_per\_page

</td><td>

Number of worker records that are pulled per page from the Oracle HCM Cloud system.Default value: 100

</td></tr><tr><td>

locations\_records\_per\_page

</td><td>

Number of records that are pulled per page for locations from the Oracle HCM Cloud system.Default value: 100

</td></tr><tr><td>

departments\_records\_per\_page

</td><td>

Number of records that are pulled per page for departments from the Oracle HCM Cloud system.Default value: 100

</td></tr><tr><td>

position\_records\_per\_page

</td><td>

Number of records that are pulled per page for positions from the Oracle HCM Cloud system.Default value: 100

</td></tr><tr><td>

workers\_query

</td><td>

List of query fields. For example, PersonId, PersonNumber, DateOfBirth, ApplicantNumber DisplayName, FullName, and ListNameThe property can be left blank, or a relevant query can be provided in the format specified in Oracle HCM.

 **Note:** workers\_query is an optional property.

</td></tr><tr><td>

full\_pull

</td><td>

When set to **True**, all the records are pulled from the Oracle HCM system into respective tables in ServiceNow instance.

 When set to **False**, only modified records \(based on last successful schedule run time\) are pulled from the Oracle HCM system into respective tables in ServiceNow instance.

Default value: False

</td></tr></tbody>
</table>