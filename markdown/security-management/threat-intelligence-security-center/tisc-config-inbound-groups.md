---
title: Configuring Inbound Intel Sharing Groups
description: Inbound Intel Sharing Groups enable administrators to group similar inbound intelligence sharing profiles together. These groups can be used to define approval rules that apply to all profiles within the group.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-config-inbound-groups.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring Inbound Intel Sharing, Configuring Threat Intelligence External Sharing, Administer, Threat Intelligence Security Center, Security Operations]
---

# Configuring Inbound Intel Sharing Groups

Inbound Intel Sharing Groups enable administrators to group similar inbound intelligence sharing profiles together. These groups can be used to define approval rules that apply to all profiles within the group.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Administration** &gt; **Inbound Intel Sharing**.

2.  Select **Inbound Intel Sharing Groups**.

3.  Select **New** to create Inbound Intelligence Group.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the Inbound Intel Sharing Group.|
    |Description|Description of the Inbound Intel Sharing Group.|
    |Type|Specifies whether the group belongs to an internal or external organization.|

5.  Select **Save** to save the intelligence sharing group.

    Also, you can enable or disable the group based on the requirement.

6.  **Adding Group Members:**

    Using this section, you can attach multiple profiles to a group.

7.  Navigate to the **Group Members** section.

8.  Select **Add**.

    The Add Inbound Intelligence Profiles dialog box is displayed. This lists all the enabled inbound intelligence sharing profiles.

9.  Select one or more profiles.

10. Provide a reason for adding the selected inbound intelligence profiles to the groups.

11. Select **Add**.

    The selected profiles are added to the groups.

12. Additionally, select **Remove** to remove the profiles from the group.

    **Note:** You must add a reason for removal.


**Parent Topic:**[Exploring Inbound Intel Sharing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-inbound-intel-sharing.md)

**Related topics**  


[Configuring Inbound Intel Sharing Profiles]()

[Defining Approval Rule for Inbound Intel]()

[Configuring Inbound Intel Sharing Profiles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-config-inbound-profile.md)

[Defining Approval Rule for Inbound Intel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-approval-inbound-intel.md)

