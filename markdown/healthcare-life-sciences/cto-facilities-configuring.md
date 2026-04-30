---
title: Configuring Care Team Operations for Facilities
description: Set up the Care Team Operations for Facilities application.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Care Team Operations for Facilities, Healthcare Operations, Healthcare and Life Sciences]
---

# Configuring Care Team Operations for Facilities

Set up the Care Team Operations for Facilities application.

## Configuration overview

1.  [Install Care Team Operations for Facilities](../task/cto-facilities-activate.md)

    Install the Care Team Operations for Facilities application \[sn\_cto\_facilities\] if you have the admin role.

2.  [Set up work order synchronization in Care Team Operations for Facilities](cto-facilities-fsm-plugin.md)

    The Field Service Management \[com.snc.work\_management\] plugin is required for work order synchronization to function with Care Team Operations for Facilities.

3.  [Set up roles for Care Team Operations for Facilities](../task/cto-facilities-assign-roles.md)

    Ensure that the appropriate roles are assigned to users of Care Team Operations for Facilities.

4.  [Create healthcare organizations for your healthcare facilities support teams](../task/cto-facilities-create-support-team.md)

    Create a healthcare organization to represent the fulfilling healthcare organization for healthcare facilities cases.

5.  [Create a group for all location support agents in Care Team Operations for Facilities](../task/cto-facilities-create-group-support-agents.md)

    Create a group for location support agents with the sn\_cto\_facilities.loc\_support\_agent role assigned so that users added to this group will inherit the collection of roles for Care Team Operations for Facilities

6.  [Create a group for all location managers in Care Team Operations for Facilities](../task/cto-facilities-create-group-managers.md)

    Create a group for location managers with the sn\_customerservice.svc\_location\_manager assigned so that users added to this group will inherit the collection of roles for Care Team Operations for Facilities.

7.  [Set up assignment groups for Care Team Operations for Facilities](../task/cto-facilities-assignment-groups.md)

    Associate assignment groups with your healthcare organizations to determine which user groups are associated with specific healthcare organizations.

8.  [Modify state decision tables in Care Team Operations for Facilities](cto-facilities-modify-state-tables.md)

    Use Decision Builder to change the state mappings for cases and incidents work orders in Care Team Operations for Facilities.

9.  [Add custom record producers to the service catalog in Care Team Operations for Facilities](../task/cto-facilities-add-customer-record-producer.md)

    Add custom record producers you've configured into service catalogs in Care Team Operations for Facilities.


