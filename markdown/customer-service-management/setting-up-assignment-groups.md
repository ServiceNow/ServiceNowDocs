---
title: Setting up assignment groups
description: Associate your assignment groups with an internal or an external business location. This association forms a one-to-many \(1:M\) relationship, which means, one or more groups can be associated with a service organization. This process makes it easier to route cases to the appropriate team member using the inter-organization support capability.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure Service Model Foundation, Data models, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Setting up assignment groups

Associate your assignment groups with an internal or an external business location. This association forms a one-to-many \(1:M\) relationship, which means, one or more groups can be associated with a service organization. This process makes it easier to route cases to the appropriate team member using the inter-organization support capability.

Lets look at the following example to understand the one-to-many relationship.

When you’re assigned to a group within your organization, you get access to specific roles and features associated with that group. The Admin sets up these groups and assigns roles via Access Control Lists \(ACLs\) that control what you can do. You can belong to multiple groups based on your function, and each group can have subgroups with additional roles. For example, if you join Group A, which has subgroups A-1 and A-2, you get the roles from Group A and its subgroups. If you join the Service Desk group as well, you get additional permissions from that group.

For details on creating groups, see [Creating groups](https://www.servicenow.com/docs/access?context=ua-creating-groups&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

The following table outlines some typical configuration tasks required for setting up assignment groups at your business organization.

|Task|Description|
|----|-----------|
|[Create a group](../task/create-a-group-so.md)|Create a group to associate it with a service organization.|
|[Configuring a group](configuring-a-group.md#)|Configure a group that includes adding group members and assigning them required roles.|
|[Associate a group to a business location](../task/associate-a-group-to-a-business-location-so.md)|Establish a one-to-many \(1:M\) relationship between a group and a business location.|
|[Add group members to a business location](../task/add-group-members-to-a-business-location-so.md)|Enroll group members to a business location and have a dedicated group working on cases.|

