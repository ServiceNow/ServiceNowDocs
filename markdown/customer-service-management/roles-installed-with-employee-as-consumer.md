---
title: Roles installed with Employee as a Consumer
description: Use different roles to establish the relationships between your users and entities. By using the Employee as a Consumer functionality within the Customer Service Management \(CSM\) application, your organization can support both requesters and supporters.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring a user as a Unified Consumer, Configuring a Unified User, User management, Set up your environment, Configure, Customer Service Management]
---

# Roles installed with Employee as a Consumer

Use different roles to establish the relationships between your users and entities. By using the Employee as a Consumer functionality within the Customer Service Management \(CSM\) application, your organization can support both requesters and supporters.

## Overview

The Unified Consumer \(sn\_customerservice.unified\_consumer\) role enables a user to have both the snc\_internal and snc\_external roles, which means that roles have greater control over consumer behavior, whether it's internal or external.

Earlier, the Consumer \(sn\_customerservice.consumer\) role automatically included the snc\_external role, which created a limitation. This limitation helped to prevent an organization from assigning the snc\_internal role to a user and restricted the simultaneous use of both the snc\_internal and snc\_external roles. To address these limitations, a new role, independent of the snc\_external role, was introduced to complement the sn\_customerservice.consumer role. This additional role can be associated with both the snc\_internal and snc\_external roles, which means that your organization now has increased flexibility in managing a user's behavior.

## Employee as a Consumer existing and new roles

The following diagram shows the existing roles and the new roles that enable the Employee as a Consumer functionality.

![Existing and new roles that enable the Employee as a Consumer functionality. For a detailed explanation of these roles, refer to the Roles and description table.](../image/unified-consumer.png "Existing and new roles")

**Note:** With the Employee as a Consumer functionality, the Requester \(sn\_customerservice.requester\) and the Unified Consumer \(sn\_customerservice.unified\_consumer\) roles were introduced. Both these roles are independent of the snc\_internal and snc\_external roles​.

<table id="table_kyc_fs4_5zb"><thead><tr><th>

Role \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Requester \[sn\_customerservice.requester\]

</td><td>

Supports requesters and implements the base functionality. It serves as a base role, running in parallel with the Enterprise Service Management \(ESM\) User \(sn\_esm\_user\) role.

</td></tr><tr><td>

Unified Consumer\[sn\_customerservice.unified\_consumer\]

</td><td>

Supports consumers and runs parallel to the Consumer \(sn\_customerservice.consumer\) role. It inherits the Requester \(sn\_customerservice.requester\) role.

</td></tr></tbody>
</table>**Related topics**  


[Configuring a user as a Unified Consumer](../concept/configuring-employee-as-a-consumer.md)

[Supported and unsupported roles and features](features-supp-and-unsupp-by-unified-consumer.md)

[Setting up a user as a Unified Consumer](../concept/setting-up-a-user.md)

