---
title: Assigning Policy and Compliance Management roles to your users
description: Before you can successfully implement or use the Policy and Compliance Management application, you must assign roles to your users.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Perform, Implement, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Assigning Policy and Compliance Management roles to your users

Before you can successfully implement or use the Policy and Compliance Management application, you must assign roles to your users.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  Click the name of a user.

3.  Click the **Roles** tab.

4.  Click **Edit**.

5.  Move the roles you want to assign to the user from the Collection side to the Roles List, then click **Save**.

6.  Repeat these steps for each of your users.

    For a comprehensive list of compliance users, see [Roles installed with GRC: Policy and Compliance Management](../../grc-policy-and-compliance/reference/r_InstallWPolAndCompl.md#).

<table id="table_o14_t2s_2mb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Compliance Reader\[sn\_compliance.reader\]

</td><td>

The Compliance Reader has read-only access to all modules of the Policy and Compliance Management application. This role is typically assigned to users who need to see what policies and controls are within the organization. Users with the reader role are also often responsible for reporting and monitoring activities.

 The Compliance Reader role contains: sn\_grc.reader.

</td></tr><tr><td>

Compliance User\[sn\_compliance.user\]

</td><td>

The Compliance User, often referred to as the Compliance Analyst, has permissions enough to fulfill virtually any policy- or control-related task. Users assigned this role are often responsible for:

-   Creating new policies
-   Requesting policy exceptions
-   Responding to acknowledgement requests
-   Creating controls objectives and relating them to policies
-   Testing and monitoring control effectiveness
-   Attesting controls
-   Remediating issues
-   Assisting with risk assessments and audit tasks
 The Compliance User role contains:

-   sn\_grc.reader
-   sn\_grc.user
-   sn\_compliance.reader
**Note:** Users with the Compliance User role can be assigned controls, and have read-only access to the Risk Management application and modules.

</td></tr><tr><td>

Compliance Manager\[sn\_compliance.manager\]

</td><td>

The Compliance Manager is responsible for managing the day-to-day compliance process.

 Users assigned this role are often responsible for:

 -   Reviewing specific regulatory requirements and trends
-   Determining which regulations require a policy
-   Approving policies and policy exceptions
-   Setting up a policy acknowledgement campaign
-   Scoping controls using entity types and entities
-   Creating and assigning attestations
-   Continuously monitoring control effectiveness
-   Compiling and sharing reports highlighting data, such as non-compliant controls
 The Compliance Manager role contains:

-   sn\_grc.reader
-   sn\_grc.user
-   sn\_grc.manager
-   sn\_compliance.reader
-   sn\_compliance.user


</td></tr><tr><td>

Compliance Administrator\[sn\_compliance.admin\]

</td><td>

The Compliance Administrator administers the Policy and Compliance Management application.

 Users assigned this role are often responsible for:

-   Monitoring platform dependencies with other applications and modules
-   Controlling all compliance data
 The Compliance Administrator role contains:

-   sn\_grc.reader
-   sn\_grc.user
-   sn\_grc.manager
-   sn\_grc.admin
-   sn\_compliance.reader
-   sn\_compliance.user
-   sn\_compliance.manager


</td></tr><tr><td>

Compliance Developer\[sn\_compliance.developer\]

</td><td>

The Compliance Developer is responsible for maintaining various aspects of the platform, such as creating workflows, reports, dashboards, additional modules, and other platform-specific content that can enrich the application.The Compliance Developer role contains:

-   sn\_grc.reader
-   sn\_grc.user
-   sn\_grc.manager
-   sn\_grc.admin
-   sn\_grc.developer
-   sn\_compliance.reader
-   sn\_compliance.user
-   sn\_compliance.manager
-   sn\_compliance.admin


</td></tr><tr><td>

Attestation Creatorsn\_compliance.attestation\_creator

</td><td>

The Attestation Creator is responsible for creating and maintaining attestations. Attestations are one of the platform components used to attest controls and it is essential for keeping them lean, precise, and up-to-date.

</td></tr></tbody>
</table>
## What to do next

Return to the [Policy and Compliance Management setup checklist](policy-compliance-impl-checklist.md).

**Parent Topic:**[Perform Policy and Compliance Management administration](../concept/perform-policy-compliance-admin.md)

