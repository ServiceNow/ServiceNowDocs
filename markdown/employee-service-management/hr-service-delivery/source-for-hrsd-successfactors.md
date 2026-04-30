---
title: Source for HR Service Delivery Integration with SuccessFactors
description: Once you set up the HR Service Delivery Integration with SuccessFactors application, the source record for SuccessFactors application is automatically created in Enterprise Service Management Integrations Framework, Source module. The SuccessFactors source record in the in Enterprise Service Management Integrations Framework application contains a predefined set of properties and HR Integration Services.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, HR Service Delivery Integration with SuccessFactors, Integrate with third-party systems, HR Service Delivery, Employee Service Management]
---

# Source for HR Service Delivery Integration with SuccessFactors

Once you set up the HR Service Delivery Integration with SuccessFactors application, the source record for SuccessFactors application is automatically created in Enterprise Service Management Integrations Framework, Source module. The SuccessFactors source record in the in Enterprise Service Management Integrations Framework application contains a predefined set of properties and HR Integration Services.

<table id="table_tyz_xpj_1nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Full-pull

</td><td>

When set to **True**, all the active users, active trainings, incomplete to-dos from the SuccessFactors system are pulled into respective tables in ServiceNow instance.

 When set to **False**, only modified users, modified trainings, modified transcripts \(based on last successful schedule run time\) are pulled from the SuccessFactors system are pulled into respective tables in ServiceNow instance.

 **Note:** If there is no information on the last successful schedule run time, the first pull will always be a full pull.

</td></tr></tbody>
</table>**Parent Topic:**[HR Service Delivery Integration with SuccessFactors reference](../concept/hr-service-delivery-integration-with-success-factors-reference.md)

