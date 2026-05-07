---
title: Configuring Outbound Intel Sharing Groups
description: Outbound Intel Sharing Groups allow you to combine multiple profiles and use them collectively when sharing data.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Outbound Intel Sharing, Configuring Threat Intelligence External Sharing, Administer, Threat Intelligence Security Center, Security Operations]
---

# Configuring Outbound Intel Sharing Groups

Outbound Intel Sharing Groups allow you to combine multiple profiles and use them collectively when sharing data.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Administration** &gt; **Outbound Intel Sharing**.

2.  Select **Outbound Intel Sharing Groups**.

3.  Select **New** to create an outbound intelligence sharing groups.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the Outbound Intel Sharing Group.|
    |Description|Description of the Outbound Intel Sharing Group.|
    |Type|Specifies whether the group belongs to an internal or external organization.|

5.  Click **Save** to save the intel sharing group.

6.  **Adding Group Members:**

    Using this section, you can attach multiple profiles to a group.

7.  Navigate to the **Group Members** section.

8.  Click **Add**.

    The Add Outbound Intelligence Profiles dialog box is displayed. This lists all the enabled outbound intelligence sharing profiles.

9.  Select one or more profiles.

10. Click **Add**.

11. Additionally, click **Remove** to remove the profiles from the group.

    After you make the necessary changes to the group, you can enable to make it active and usable in intelligence sharing. Otherwise you can disable it if it should no longer be used.

    **Note:** An information message is displayed indicating that the selected outbound intelligence profile\(s\) have been added or removed to this group. This message is displayed with the respect to the action either Add or Remove you select.


**Parent Topic:**[Exploring Outbound Intel Sharing](../concept/tisc-outbound-intel-sharing.md)

**Related topics**  


[Configuring Outbound Intel Sharing Controls](tisc-outbound-sharing.md)

[Configuring Outbound Intel Data Exclusion Rule](tisc-outbound-data-exclusion.md)

[Configuring Outbound Intel Sharing Profiles](tisc-outbound-sharing-profiles.md)

[Defining Approval Rule for Outbound Intel](tisc-approval-outbound-intel.md)

[Configuring Outbound Intel Sharing Templates](tisc-intel-sharing-templates.md)

[Working on the Redaction Library](tisc-redaction-library.md)

