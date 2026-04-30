---
title: Data policy
description: Data policies enable you to enforce data consistency by setting mandatory and read-only states for fields.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Data policy

Data policies enable you to enforce data consistency by setting mandatory and read-only states for fields.

Data policies are similar to [UI policies](../../form-administration/task/t_CreateAUIPolicy.md#), but UI policies only apply to data entered on a form through the standard browser. Data policies can apply rules to all data entered into the system, including data brought in through import sets or web services and data entered through the mobile UI.

For example, suppose that you are configuring a web service that allows users from outside the platform to update problems on the ServiceNow instance. Since these problems are not updated through the instance UI, they are not subject to the UI policies on the problem form. To ensure that the **Close notes** field is completed before a problem is marked **Closed/Resolved**, you can create a data policy that applies to server-side imports. Data that does not comply with this data policy produces an error. You can also apply the policy on the browser by selecting the **Use as UI Policy on client** check box in the data policy record.

Since UI policies can also manage the visibility of fields on a form, you may want to augment UI policies with data policies rather than replace them.

By default, data policies are applied to all GlideRecord operations including those used in Scripted REST APIs, and the REST Table API. You can opt out of applying the data policy to:

-   Target records of SOAP web services
-   Import sets
-   Client-side UI policies

The admin role is required to edit data policies.

**Note:** Defining a data policy enforces the policy when a record is submitted from the UI. This behavior cannot be changed.

-   **[Installed with data policy](c_InstalledWithDataPolicy.md#)**  
Data policy includes several components that are installed on the instance.
-   **[Create a data policy](../task/t_CreateADataPolicy.md)**  
You can create a new data policy to define data rules for a table.
-   **[Convert a UI policy to a data policy](../../form-administration/task/t_ConvertAUIPolicyToADataPolicy.md)**  
To make a UI policy the default setting, convert the UI policy to a data policy.
-   **[Convert a data policy to a UI policy](../task/t_ConvertADataPolicyToAUIPolicy.md)**  
Convert a data policy to a UI policy if a data policy already exists but needs to apply only to records created or updated in the browser.
-   **[Data policy debugging](../reference/r_DataPolicyDebugging.md)**  
Debug messages can help administrators identify and resolve data policy problems.

**Parent Topic:**[Field administration](../../reference-pages/concept/c_IntroductionToFields.md)

