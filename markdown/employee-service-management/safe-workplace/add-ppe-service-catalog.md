---
title: Add PPE models to Service Catalog
description: Add PPE models through Service Catalog so employees can request the items they need.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/safe-workplace/add-ppe-service-catalog.html
release: zurich
product: Safe Workplace
classification: safe-workplace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up Workplace PPE Inventory Management, Workplace PPE Inventory Management, Safe Workplace, Health and Safety, Employee Service Management]
---

# Add PPE models to Service Catalog

Add PPE models through Service Catalog so employees can request the items they need.

## Before you begin

Role required: catalog\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **** &gt; **Catalog Definitions** &gt; **Record Producers**.

2.  Filter the category to Personal Protective Equipment \(PPE\).

3.  Click one of the record producers.

    Any record producer in the Personal Protective Equipment \(PPE\) category will work.

4.  Click **Copy**.

5.  Update the **Name**, **Model**, **Description**, and **Picture** fields for the item.

6.  In the **Script** field, replace the sys\_id value with the sys\_id for the PPE model that you're adding to your service catalog.

    The sys\_id is a unique alphanumeric code. To get the sys\_id for a PPE model, navigate to the PPE model record, right-click the form header, and select **Copy sys\_id**.

7.  Click **Update**.


## What to do next

Add the Personal Protective Equipment \(PPE\) category to your service catalog so employees can see the items. To add the category, navigate to **Self-Service** &gt; **Service Catalog** and click the plus icon \(\[Omitted image "plus-icon.png"\] Alt text: plus icon\) in the upper right.

**Parent Topic:**[Set up Workplace PPE Inventory Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/safe-workplace/set-up-ppe.md)

**Previous topic:**[Create models for PPE items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/safe-workplace/create-ppe-model.md)

**Next topic:**[Add PPE stock](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/safe-workplace/add-ppe-stock.md)

