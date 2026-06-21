---
title: Data Management roles
description: These roles are available for the application
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/roles-by-product/roles\_datamanagement.html
release: australia
topic_type: reference
last_updated: "2024-03-11"
reading_time_minutes: 1
breadcrumb: [Roles for all products]
---

# Data Management roles

These roles are available for the application

<table><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th><th>

Groups with this role

</th><th>

Special considerations

</th></tr></thead><tbody><tr><td>

Data Management tools admin \[data\_mgt\_tools\_admin\]

</td><td>

The data\_mgmt\_tools\_admin role is a granular admin role designed to provide more targeted permissions for data management tasks, reducing the need to grant full admin access.

</td><td>

None.

</td><td>

None.

</td><td>

Granting data\_mgmt\_tools\_admin alone is not sufficient for most data management operations. To enable full functionality for the data\_mgmt\_tools\_admin role, you must also assign the following roles:

 These roles are not embedded within data\_mgmt\_tools\_admin by default. You must assign these additional roles to the user explicitly.

 After assigning these roles, also add roles that provide CRUD \(Create, Read, Update, Delete\) access to data tables \(for example, itil and itil\_admin\). For example, adding the itil\_admin enables an ITIL administrator to archive or update records in the associated ITIL tables \(incident, problem, change, and so on\) depending on configuration. If these roles aren’t assigned, some or all data management functionality will be limited or unavailable.

</td></tr></tbody>
</table>**Parent Topic:**[Roles for all products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/roles-by-product/roles-for-all-products.md)

