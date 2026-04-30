---
title: Instance Data Replication roles
description: Instance Data Replication \(IDR\) is installed with these roles.Admin role for accessing all IDR tables.Read role for reviewing IDR tables.Role required for making a diagnostic request.
locale: en-US
release: zurich
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Instance Data Replication roles

Instance Data Replication \(IDR\) is installed with these roles.

To learn more about managing subscriptions, see [Managing per-user subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) and contact your account representative.

**Parent Topic:**[Instance Data Replication reference](../concept/reference-instance-data-replication.md)

**Related topics**  


[Data privacy in Instance Data Replication](../concept/data-privacy-consumers-idr.md)

[Adapter descriptions for Instance Data Replication](adapter-descriptions.md)

[Excluded tables in Instance Data Replication](IDR-excluded-tables.md)

[Domain separation and IDR](instance-data-replication-domain-separation.md)

[Instance Data Replication system properties](instance-data-replication-properties.md)

## IDR administrator \[idr\_admin\]

Admin role for accessing all IDR tables.

### Contains Roles

List of roles contained within the role: idr\_rest.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## IDR read \[idr\_read\]

Read role for reviewing IDR tables.

### Contains Roles

List of roles contained within the role: idr\_rest.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## IDR rest \[idr\_rest\]

Role required for making a diagnostic request.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

