---
title: Set up security tag groups and tags
description: You can assign tags to security incidents, response tasks, vulnerable items, observables, IoCs, and security cases to create metadata on the responding record and define who should have access to specific types of security content. The tags can be added to security groups to organize them.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Security Operations common functionality, Security Operations]
---

# Set up security tag groups and tags

You can assign tags to security incidents, response tasks, vulnerable items, observables, IoCs, and security cases to create metadata on the responding record and define who should have access to specific types of security content. The tags can be added to security groups to organize them.

## Before you begin

-   Manual security tags are preserved when automatic tags are applied to security incidents to avoid any analyst-curated information loss. The Source column in the Applied Security Tags table tracks whether tags are added manually or automatically by rules.
-   Role required: sn\_si.admin

## Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Security Tags** &gt; **Groups**.

    Three default classification groups are included in the base system.

    -   **Enrichment allow list/deny list**: This group defines whether a record is to be treated as an allow list or deny list record. Allow list records are generally of less significance, so they can be ignored. Deny list records are generally of higher interest.
    -   **Metatag**: This group is provided as demo data. You can use it to create custom classification tags that are used by security operations applications.
    -   **Traffic Light Protocol** \(TLP\): This group is used to ensure that sensitive information is shared with the correct audience. It employs four colors \(White, Green, Amber, and Red\) to indicate different degrees of sensitivity. For each color, you can assign the appropriate read/write access roles. When sharing observables to a trusted security circle, the tag assigned to the trusted security circle profile determines which TLP-tagged observables can be shared to the circle, as follows:

        -   **TLP: WHITE:** Only observables with TLP: WHITE can be shared to a TLP: WHITE profile.
        -   **TLP: GREEN:** Observables with TLP: GREEN and TLP: WHITE can be shared to a TLP: GREEN profile.
        -   **TLP: AMBER:** Observables with TLP: AMBER, TLP: GREEN, and TLP: WHITE can be shared to a TLP: AMBER profile.
        -   **TLP: RED:** All observables, regardless of their TLP tag, can be shared with a TLP: RED profile since TLP: RED is the highest ranked TLP tag.
        **Note:** You can add other TLP colors, but any in addition to the four colors included are considered not valid by the Forum for Incident Response and Security Teams \([FIRST](https://www.first.org/)\).

2.  Select **New Group**.

3.  Fill in the fields on the form, as appropriate.

<table id="table_t4d_4bd_5s"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the security group.

</td></tr><tr><td>

Allow multi-selection

</td><td>

Option to assign multiple security tags to a record that shares a group. The following options are available:

-   True: Multiple tags from this group can be selected simultaneously.
-   False: Only one tag from this group can be active at a time.


</td></tr><tr><td>

Active

</td><td>

Option to turn the group on or off.

</td></tr><tr><td>

Description

</td><td>

Brief description of this group.

</td></tr></tbody>
</table>4.  Select **Save**.

    The Security Tags related list appears.

5.  In the Security Tags related list, select **New**.

6.  Fill in the fields on the form, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Name|The name of the classification tag.|
    |Security Tag Group|If the tag was created using the **New** button in the group related list, this field defaults to the current group. Optionally, you can add the tag to a different group.|
    |Order|The order in which the tag appears on forms or within a list.|
    |Color|The color for this tag.|
    |Enforce restricted access|Option to assign read and/or write roles needed by users to read or write to records that have this security tag.|
    |Active|Option to turn the tag on or off.|
    |Description|A description of this tag.|
    |Roles \(read access\)|To assign read access to a security tag, select the lock icon, select the appropriate access roles, and select the lock icon again. This field appears only if you have selected the **Enforce restricted access** check box.|
    |Roles \(write access\)|To assign write access to a security tag, select the lock icon, select the appropriate access roles, and select the lock icon again. This field appears only if you have selected the **Enforce restricted access** check box.|

7.  Repeat as needed to create more security tags.

8.  Select **Save**.

    **Note:** You can also create tags by selecting **New** button on the list view. The procedure is the same.


-   **[Create security tag rules](create-security-tag-rules.md)**  
Security tag rules provide filtering for security tag access.
-   **[Import security tag rules](import-security-tag-rules.md)**  
You can import security tag rules from other tables in your deployment.

**Parent Topic:**[Security Operations common functionality](../concept/sec-ops-common-functionality.md)

