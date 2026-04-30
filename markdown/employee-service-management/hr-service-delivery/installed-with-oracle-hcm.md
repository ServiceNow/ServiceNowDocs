---
title: Components installed with HR Service Delivery integration with Oracle Cloud HCM
description: Several types of components are installed with the activation of the HR Service Delivery integration with Oracle Cloud HCM \(sn\_hr\_oracle\_hcm\) application, including tables, user roles, and scheduled jobs.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference - HR Service Delivery integration with Oracle Cloud HCM, HR Service Delivery integration with Oracle Cloud HCM, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Components installed with HR Service Delivery integration with Oracle Cloud HCM

Several types of components are installed with the activation of the HR Service Delivery integration with Oracle Cloud HCM \(sn\_hr\_oracle\_hcm\) application, including tables, user roles, and scheduled jobs.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

HR Oracle HCM Cloud Admin \[sn\_hr\_oracle\_hcm.admin\]

</td><td>

Can access all the features and capabilities of the Enterprise Service Management Integrations Framework with the HR Service Delivery integration with Oracle Cloud HCM application.

</td><td>

Can access all features and capabilities of the Enterprise Integrations with Oracle HCM integration application.Contains the sn\_hr\_integr\_fw.admin role.

</td></tr></tbody>
</table>## Scheduled job installed

<table id="table_dx3_gb1_wdb"><thead><tr><th>

Scheduled flow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Trigger Oracle HCM Integration flow

</td><td>

Pull data from Oracle HCM Cloud to a ServiceNow® instance. By default, the flow is in inactive state. For information on how to activate the flow, see [Activate schedule flows](../task/setup-the-job.md).

</td></tr></tbody>
</table>## Tables installed

The tables required for HR Service Delivery integration with Oracle Cloud HCM are obtained from the Enterprise Service Management Integrations Framework. The tables get auto-installed with the Enterprise Service Management Integrations Framework installation when you activate the HR Service Delivery integration with Oracle Cloud HCM application. For more information, see [Components installed with Enterprise Service Management Integrations Framework](installed-with-hr-int-fra.md).

**Parent Topic:**[Reference - HR Service Delivery integration with Oracle Cloud HCM](reference-hrsd-int-oracle-cloud-hcm.md)

**Related topics**  


[Transform maps for HR Service Delivery integration with Oracle Cloud HCM](oracle-hcm-transform-maps.md)

