---
title: Configuring Care Team Operations for Biomed
description: The following setup steps need to occur prior to using Care Team Operations for Biomed.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Care Team Operations for Biomed, Healthcare Operations, Healthcare and Life Sciences]
---

# Configuring Care Team Operations for Biomed

The following setup steps need to occur prior to using Care Team Operations for Biomed.

## Configuration overview

1.  [Install Care Team Operations for Biomed](cto-biomed-activate.md)

    Install the Care Team Operations for Biomed application \(sn\_cto\_biomed\) if you have the admin role.

2.  [Set up work order synchronization in Care Team Operations for Biomed](cto-biomed-plugin-info.md)

    The Field Service Management \[com.snc.work\_management\] plugin is required for work order synchronization to function with Care Team Operations for Biomed.

    For Care Team Operations for Biomed to create work orders from Healthcare Biomed cases, the Field Service Management \[com.snc.work\_management\] plugin must be installed.

3.  [Assign roles for Care Team Operations for Biomed](../task/cto-biomed-set-up-roles.md)

    Ensure that the correct roles are assigned to users of Care Team Operations for Biomed.

4.  [Create healthcare organizations for your biomed support teams](../task/cto-biomed-create-org.md)

    Create a healthcare organization to represent the fulfilling healthcare organization for healthcare biomed cases.

5.  [Create a group for all location support agents in Care Team Operations for Biomed](../task/cto-biomed-create-agent-groups.md)

    Create a group for location support agents with the sn\_cto\_biomed.loc\_support\_agent assigned so that users added to this group will inherit the collection of roles for Care Team Operations for Biomed.

6.  [Create a group for all location managers in Care Team Operations for Biomed](../task/cto-biomed-creare-manager-group.md)

    Create a group for location managers with the sn\_customerservice.svc\_location\_manager assigned so that users added to this group will inherit the collection of roles for Care Team Operations for Biomed.

7.  [Set up assignment groups for Care Team Operations for Biomed](../task/cto-biomed-set-up-assignment-groups.md)

    Associate assignment groups with your healthcare organizations to determine which user groups are associated with specific healthcare organizations.

8.  [Modify state decision tables in Care Team Operations for Biomed](cto-biomed-modify-states.md)

    Use Decision Builder to change the state mappings for cases and incidents work orders in Care Team Operations for Biomed .


