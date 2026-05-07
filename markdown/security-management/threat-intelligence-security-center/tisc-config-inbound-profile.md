---
title: Configuring Inbound Intel Sharing Profiles
description: This section describes the inbound intelligence sharing profiles used to receive intelligence from external organizations into TISC.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring Inbound Intel Sharing, Configuring Threat Intelligence External Sharing, Administer, Threat Intelligence Security Center, Security Operations]
---

# Configuring Inbound Intel Sharing Profiles

This section describes the inbound intelligence sharing profiles used to receive intelligence from external organizations into TISC.

## Before you begin

Role required: sn\_sec\_tisc.admin

**Note:**

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Administration** &gt; **Inbound Intel Sharing**.

2.  Select **Inbound Intel Sharing Profiles**.

3.  Select **New** to create an Inbound Intelligence Profile.

4.  On the form, fill in the fields.

<table id="table_syl_ztc_mfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the inbound intelligence profile.

</td></tr><tr><td>

Industry

</td><td>

Select the industry category such as Aerospace, Agriculture for which the inbound intelligence profile is applicable to.

</td></tr><tr><td>

Description

</td><td>

Description of the inbound intelligence profile.

</td></tr><tr><td colspan="2">

**Inbound Intelligence Settings**

</td></tr><tr><td>

Data Format

</td><td>

Supported data formats for inbound intelligence sharing profile.Currently, two data formats are supported for inbound intelligence sharing:

-   STIX 2.1
-   MISP
For more information on the data formats description, see [Configuring Outbound Intel Sharing Profiles](tisc-outbound-sharing-profiles.md).

</td></tr><tr><td>

User for authentication \(should have sn\_sec\_tisc.api\_post\_intel role\)

</td><td>

Select the user whose credentials should be used for authentication when an external system shares intelligence with TISC for this profile.**Note:** Users with sn\_sec\_tisc.api\_post\_intel role only be available in the drop-down list.

</td></tr><tr><td>

Default Confidence

</td><td>

Indicates the default confidence level applied to all intelligence records received from this profile when the source doesn’t provide a confidence value.

</td></tr><tr><td>

Expiry period \(days\)

</td><td>

Specifies the number of days after which the intelligence records received from sharing profile expires.Once expired, the intelligence records might no longer be visible, shared, or considered valid.

</td></tr><tr><td>

Default TLP

</td><td>

Specifies the default TLP applied to all intelligence records received from this profile when the source doesn’t provide a TLP value.

</td></tr><tr><td>

Enable Notification

</td><td>

Select this check to send a notification to the sender on approval or rejection of the inbound intelligence record.

</td></tr><tr><td>

Notify On

</td><td>

Use this option to choose when to notify the email recipients configured \(for example, on approval or rejection or both of a record\).**Note:** This option appears only if **Enable Notification** is selected.

</td></tr><tr><td>

Email Recipients

</td><td>

Enter the email addresses of users who should be notified based on the criteria configured in the **Notify On** field.**Note:** This field is only visible when **Enable Notification** is checked. Multiple email addresses can be entered, separated by commas.

</td></tr><tr><td>

TISC Tags

</td><td>

Specifies the tags to be added to all the inbound intelligence received from external system.

</td></tr></tbody>
</table>5.  Select **Save**.

6.  **Copy Profile ID**:

    The external organizations require this profile ID to share the information.

7.  Select **Copy Profile ID** button to copy your profile ID for sharing.

8.  Additionally, select **Email Profile ID** to email the sharing profile details.

    When you select this option, an email composer dialog box is displayed. Fill the email details to whom you want to share the profile.

9.  Select **Send** to send the details to the external user.


**Parent Topic:**[Exploring Inbound Intel Sharing](../concept/tisc-inbound-intel-sharing.md)

**Related topics**  


[Configuring Inbound Intel Sharing Groups](tisc-config-inbound-groups.md)

[Defining Approval Rule for Inbound Intel](tisc-approval-inbound-intel.md)

[Configuring Inbound Intel Sharing Groups](tisc-config-inbound-groups.md)

[Defining Approval Rule for Inbound Intel](tisc-approval-inbound-intel.md)

