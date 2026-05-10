---
title: Configure your ServiceNow AI Platform instance for external content indexing
description: Create and configure a non-interactive service user account on your ServiceNow AI Platform source instance to allow access by the ServiceNow instance external content connector.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [ServiceNow instance external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure your ServiceNow AI Platform instance for external content indexing

Create and configure a non-interactive service user account on your ServiceNow AI Platform® source instance to allow access by the ServiceNow instance external content connector.

## Before you begin

Role required: admin and security\_admin

**Note:** The security\_admin role is an elevated privilege role. To learn more about elevated privilege roles, see [Elevated privilege roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_ElevatedPrivilege.md). For details on the security\_admin elevated privilege role, see [Security\_admin role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-admin-role.md).

## About this task

The ServiceNow instance external content connector retrieves KB articles and security principals from a ServiceNow AI Platform instance. To allow the external content connector to access this content, you need to configure a non-interactive service user account that the connector will use when running document and user mapping crawls.

Perform all of these steps on the ServiceNow AI Platform instance that you want the external content connector to retrieve searchable content and metadata from. This is your source instance. The instance where the connector runs and populates search applications with the retrieved data is your destination instance.

## Procedure

1.  On your source instance, create a new non-interactive user and save its user ID.

    1.  Create a new user by following the steps from [Create a user](../../users-and-groups/task/t_CreateAUser.md).

        **Note:** Make sure to select the **Web service access only** option on the new user record. This option designates your new user as a non-interactive user. To learn more about how non-interactive users differ from interactive users, see [Non-interactive sessions](../../users-and-groups/concept/c_NonInteractiveSessions.md#).

    2.  Copy the **User ID** for your new source instance user account and store it in a secure location.

        **Important:** Your connector admin needs this user account's user ID when configuring the ServiceNow instance external content connector on your destination instance.

2.  On your source instance, generate and copy a strong password for your new user.

    1.  Generate a strong password for your new user by following the steps from [Configure password for a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/reset-your-password.md).

    2.  Store the copied password in a secure location.

        **Important:** Your connector admin needs this user account's password when configuring the ServiceNow instance external content connector on your destination instance.

3.  On your source instance, add your new user to the **MFA Exempted User Group** by following the steps from [Add a user to a group](../../users-and-groups/task/t_AddAUserToAGroup.md).

    **Note:** Inclusion in this group exempts your new user from the default requirement to use multi-factor authentication \(MFA\) when logging in to your source instance. This configuration is needed for proper operation of the ServiceNow instance external content connector.

4.  On your source instance, create a new custom role in the Global application scope.

    1.  Select the Global application scope, following the steps from [Select an application from the application picker](../../../build/applications/task/t_SelectAnAppFromTheAppPicker.md).

    2.  Navigate to **All** &gt; **User Administration** &gt; **Roles**.

    3.  Select **New**.

    4.  On the Role form, enter a name for your new custom role.

        As an example, you might enter `ext_cont_connectors_custom_role`.

    5.  Select **Submit**.

5.  On your source instance, create and edit ACLs \(access control lists\) to grant users with your new custom role access to the Security Attribute \[sys\_security\_attribute\] table.

    1.  Navigate to **All** &gt; **System Security** &gt; **Access Control \(ACL\)**.

    2.  Select **New**.

    3.  On the Access Control form, fill in the fields.

<table id="table_fgg_bpv_3hc"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Select **record**.

</td></tr><tr><td>

Operation

</td><td>

Select **read**.

</td></tr><tr><td>

Active

</td><td>

Select this option.

</td></tr><tr><td>

Name

</td><td>

In the **Tables** list, select the Security Attribute \[sys\_security\_attribute\] table.Leave the **Fields** list set to its default value.

</td></tr><tr><td class="sub-head" colspan="2">

Conditions

</td></tr><tr><td>

Requires role

</td><td>

Insert a new row with the name of your new custom role.

</td></tr></tbody>
</table>    4.  Select **Submit**, then select **Continue**.

        The new ACL record appears in the Access Control list view.

    5.  In the Access Control \[sys\_security\_acl\] table list view, create and apply a filter with the following condition.

        |Field|Operation|Value|
        |-----|---------|-----|
        |Sys ID|is|ee3ebfdc9f4112108647e8c40b0a1cb0|

        For details on creating and applying filters to limit records shown in a table's list view, see [Create a filter in List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/t_CreatingFilters.md).

        This filter should display a single Access Control record with Decision Type **Deny Unless**.

    6.  Open the filtered Access Control record.

    7.  On the Access Control form, in the Conditions section, find the **Requires role** condition list and insert a new row with the name of your new custom role.

    8.  Select **Update**.

6.  On your source instance, assign roles to your new user.

    1.  Assign your new custom role to your new user by following the steps from [Assign a role to a user](../../users-and-groups/task/t_AssignARoleToAUser.md).

    2.  Assign each of the following roles to your new user by following the steps from [Assign a role to a user](../../users-and-groups/task/t_AssignARoleToAUser.md).

        |Role|Description|
        |----|-----------|
        |access\_analyzer\_admin|Grants the user access to tables relating to access control in your source instance, including the Access Control \[sys\_security\_acl\], Role \[sys\_user\_role\], and Table \[sys\_db\_object\] tables. To learn more about access control, see [Access Control List Rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/access-control-rules.md).|
        |catalog\_manager|Grants the user access to Service Catalog items in your source instance. For more details on this base system role, see [Base system roles](../../roles/reference/r_BaseSystemRoles.md).|
        |itil|Grants the user access to incidents and user criteria in your source instance. For more details on this base system role, see [Base system roles](../../roles/reference/r_BaseSystemRoles.md).|
        |knowledge\_admin|Grants the user access to KB articles in your source instance. For more details on this base system role, see [Base system roles](../../roles/reference/r_BaseSystemRoles.md).|
        |snc\_platform\_rest\_api\_access|Grants the user access to Platform Rest APIs in your source instance. The ServiceNow instance external content connector uses the [Attachment API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/c_AttachmentAPI.md) and [Table API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/c_TableAPI.md) to access your source instance during crawls. For more details on this base system role, see [Base system roles](../../roles/reference/r_BaseSystemRoles.md).|
        |snc\_read\_only|Restricts the user to read-only access on all tables that it has access to. For more details on this base system role, see [Read-only role](../../user-administration/concept/c_ReadOnlyRole.md#).|


## What to do next

Provide the following items to the connector admin who will create the ServiceNow instance connector on your destination instance:

-   The URL for your ServiceNow AI Platform source instance. As an example, you might provide `https://example.service-now.com/` as the instance URL.
-   The user ID for the non-interactive service user you created on your source instance, as copied in step [1.b](configure-sn-aip-instance-external-content-indexing.md#store-service-user-id-step). As an example, you might provide `sn.instance.connector` as the user ID.
-   The password for the non-interactive service user you created on your source instance, as copied in step [2.b](configure-sn-aip-instance-external-content-indexing.md#store-service-user-password-step).

Your connector admin needs these items to configure a ServiceNow instance external content connector on your destination instance to retrieve content and security principals from your ServiceNow AI Platform source instance.

For details on creating and configuring a ServiceNow instance external content connector, see [Create a ServiceNow instance external content connector](create-ext-cont-connector-snow-instance.md).

**Parent Topic:**[ServiceNow instance external content connector](../concept/servicenow-instance-external-content-connector.md)

