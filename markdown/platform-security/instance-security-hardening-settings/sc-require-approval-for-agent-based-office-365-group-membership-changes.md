---
title: Require approval for agent-based Office 365 group membership changes \[New in Security Center 7.0\]
description: Enable the approval flow for adding or removing Office 365 group members through the Microsoft 365 group membership AI Agent using a system property.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Require approval for agent-based Office 365 group membership changes \[New in Security Center 7.0\]

Enable the approval flow for adding or removing Office 365 group members through the Microsoft 365 group membership AI Agent using a system property.

Use the **sn\_itsm\_aia.office\_365\_group\_member\_approval.required** system property to control whether the approval flow for adding or removing Office 365 group members through the AI agent is on or off. When the approval workflow is enabled, an approval record must be set to approved by a member of the group specified in the **sn\_itsm\_aia.office\_365\_group\_member\_approval.group\_id** system property. If the **sn\_itsm\_aia.office\_365\_group\_member\_approval.group\_id** property isn't configured, the **Microsoft 365 group member approvers** group is used.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**sn\_itsm\_aia.office\_365\_group\_member\_approval.required**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Boolean

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Fallback value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.9
-   CVSS score: Medium
-   Any user who can access the Microsoft 365 group membership AI Agent can and add and remove Office 365 group members from the Azure AD group if explicit approval from the specified approvers group isn’t required. Ensure that these changes are approved to reduce the risk of elevation of privilege by adding/removing members without proper authorization.

</td></tr><tr><td>

Functional impact

</td><td>

When **sn\_itsm\_aia.office\_365\_group\_member\_approval.required** is set to **true**, a member of the group specified in **sn\_itsm\_aia.office\_365\_group\_member\_approval.&lt;group\_id&gt;** must approve the Incident requesting addition or removal of Office 365 group members. If **sn\_itsm\_aia.office\_365\_group\_member\_approval.required** is set to **false** then no approval is required and the AI Agent can autonomously handle the process of adding or removing members from an Office 365 group.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Access control](sc-access-control.md)

