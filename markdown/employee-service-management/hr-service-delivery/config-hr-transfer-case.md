---
title: Configure HR transfer case
description: The base system provides examples of HR transfer case configuration types. You can also create your own.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/hr-service-delivery/config-hr-transfer-case.html
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Transfer an HR case, Use HR Case Management, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Configure HR transfer case

The base system provides examples of HR transfer case configuration types. You can also create your own.

## Before you begin

Role required: sn\_hr\_core.admin

## About this task

If you are creating a transfer case configuration, you must also create a script include to implement the sn\_hr\_core HR case transfer extension point. For more information, see Registering custom script includes against the scripted extension points.

Refer to the existing script includes as examples:

-   hr\_TransferCase
-   ReclassifyCaseTransfer
-   StandardCaseTransfer

The hr\_TransferCase script include provides a list of fields ignored in the transfer and acts as a utility for the other two script includes.

**Note:** Refer to Script includes.

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Transfer Case Configuration**.

2.  Select **New**.

3.  Fill in the form.

<table id="table_o31_kh1_nhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the HR case transfer type.The defaults are:

-   Reclassify
-   Standard


</td></tr><tr><td>

Display text

</td><td>

The HR case transfer type that appears on the Transfer Case menu from the HR case form. The defaults are:-   Transfer with existing case number
-   Transfer to a new case number


</td></tr><tr><td>

HR criteria

</td><td>

Defines what HR agents can view and use this transfer type when performing an HR case transfer from the HR case form.See [HR criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/hr-criteria.md).

**Note:** When defining conditions like case sensitivity or null values, see API GlideFilter - Scoped, Global.

</td></tr><tr><td>

Is default

</td><td>

Indicates that the transfer type is the default and appears first in the Transfer Case menu from the HR case form.**Note:** To mark a transfer type as the default, click the **Set as Default** button at the bottom.

</td></tr><tr><td>

Active

</td><td>

Indicates if the HR case transfer type is active and available for use. Inactive indicates that the transfer type does not appear in the Transfer Case menu from the HR case form.

</td></tr></tbody>
</table>4.  Select **Submit** or **Update**.


**Parent Topic:**[Transfer an HR case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/reclassify-hr-case.md)

