---
title: Set the business organization code property
description: After importing Business Organizations information, update the com.snc.service\_organization.last.generated.code.tree.path property with the correct organization code value.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/set-csm-bo-code-property.html
release: brazil
topic_type: task
last_updated: "2026-09-09"
reading_time_minutes: 1
breadcrumb: [Import business organizations with guided setup, Create a business organization, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Set the business organization code property

After importing Business Organizations information, update the **com.snc.service\_organization.last.generated.code.tree.path** property with the correct organization code value.

## Before you begin

Role required: admin

## About this task

The **com.snc.service\_organization.last.generated.code.tree.path** system property stores the **Organization Code** value for the most recently created business organization in the Organization Core \[sn\_customer\_service\_organization\] table.

When you create a business organization record, the system uses this property to generate a unique organization code. The property is then updated with the latest value, confirming the next business organization record receives a new unique code.

The value of the **com.snc.service\_organization.last.generated.code.tree.path** property must match the value of the Organization Code field for the last inserted business organization record. When you create business organization records by importing data from other sources or instances, these values can get out of synchronization. If these values don’t match, the system generates an error on the creation of the next new record in the Organization Core table:

`java.sql.BatchUpdateException: Duplicate entry for key service_organization_path`

Use the following steps to fix this error.

## Procedure

1.  Determine the highest or last used organization code value from the Organization Core \[sn\_customer\_service\_organization\] table.

2.  Navigate to the System Property \[sys\_properties\] table.

3.  Set the **com.snc.service\_organization.last.generated.code.tree.path** property to the value determined in step 1.


