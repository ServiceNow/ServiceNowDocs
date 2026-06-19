---
title: Classify HR data
description: Assign data classifications to HR application-specific table columns in the Dictionary \[sys\_dictionary\] table. The assigned columns will appear in the “Classified Dictionary Entries” related list for a data classification.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/hr-service-delivery/classify-hr-data.html
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow Vault for HR Service Delivery, Integration of HR Service Delivery with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# Classify HR data

Assign data classifications to HR application-specific table columns in the Dictionary \[sys\_dictionary\] table. The assigned columns will appear in the “Classified Dictionary Entries” related list for a data classification.

## Before you begin

Role required: data\_classification\_admin

## Procedure

1.  In the Navigator pane, type `sys_dictionary.list`.

2.  Filter by Human Resources-related records.

    In the Table search field, type `sn_hr_core` or in the Package search field, type `human resources`.

3.  Select each of the records that you want to assign to a specific data classification.

4.  After selecting the elements, click **Actions on selected rows** &gt; **Classify**.

5.  In the Assign to data class dialog, select the data classifications you want to assign to your selected dictionary elements, then click **Classify**.

    **Warning:** This will overwrite any existing classifications for the selected dictionary items.

    You can select multiple data classifications as needed.

    See Data dictionary tables for additional information.


**Parent Topic:**[ServiceNow Vault for HR Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/vault-hr-service-delivery.md)

