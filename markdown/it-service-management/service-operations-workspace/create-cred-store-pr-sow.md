---
title: Create credential store for Password Reset in Service Operations Workspace
description: Create a password reset credential store record to configure access to your credential store server while a user is changing or resetting a password.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting up Service Desk assisted Password Reset in Service Operations Workspace, Setting up integrations in Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Create credential store for Password Reset in Service Operations Workspace

Create a password reset credential store record to configure access to your credential store server while a user is changing or resetting a password.

## About this task

In addition to host connection information, you can specify the password hints that users should see, restrictions on password reuse, the allowed number of failed reset attempts, and other settings.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Overview**.

2.  On the **Admin Center** page, do one of the following:

    -   In the **Overview** tab, select the **Configure** button in the **Service Desk Assisted Password Reset** card.
    -   In the **Configurations** tab, select **Service Desk Assisted Password Reset** card.
3.  On the **Credential stores** card, select **Configure**.

    The default credential store is displayed.

4.  On the form, fill in the fields.

<table id="table_sdt_2dm_zbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the credential store for service desk assisted password reset.

</td></tr><tr><td>

Description

</td><td>

Detailed information about the credential store.

</td></tr><tr><td>

Type

</td><td>

Type of credential store that you are connecting to. A ServiceNow credential store type is a template that provides the required set of capabilities for a particular kind of credential store.Credential stores inherit the functionality of the credential store type.

</td></tr><tr><td>

Auto generate password

</td><td>

Script include that generates a temporary password for use during the reset process.If you select the **Enforce history policy** check box, then you must specify a value for **Auto-generate password** that is compliant with the password policy.

</td></tr><tr><td>

Child Alias

</td><td>

Child aliases are associated with the base alias. After creating a connection and credential alias, you can create a child alias to configure multiple connections for a password reset credential store.When a password reset request is made, the flow checks whether there are child alias connections at the process level. If the child alias is configured at the credential store level, the flow picks the aliases connections and proceeds with the request.

</td></tr><tr><td>

Enable password policy

</td><td>

See [Enable password policies on your instance](https://www.servicenow.com/docs/access?context=enable-password-policies&version=australia&pubname=australia-platform-security&ft:locale=en-US)

</td></tr><tr><td>

Enable password strength

</td><td>

Select the check box to:

 -   Option to display the text box for the strength rule script so that you can update the script.
-   Display the graphical password strength bar to the user while the user changes or resets the password.


</td></tr><tr><td>

Password policy

</td><td>

Default password policy.

</td></tr><tr><td>

Enforce history policy

</td><td>

Option to ensure that the users don’t reuse passwords. For example, you might configure the history policy to not allow the user to reuse any of the previous 10 passwords. Follow this procedure to use the feature: 1.  Select the **Enforce history policy** check box.
2.  In the **Password Reset Credential Store Parameters** related list, create a **password\_history\_limit**parameter.
3.  Set the value of the parameter to the number of previous passwords that cannot be used \(maximum 10\). The default value of 0 \(zero\) enables use of any previous password.


</td></tr></tbody>
</table>5.  Select **Submit**.

6.  Select **Test Connection**.

    You must test the connection to a credential store after you configure a new credential store.


**Parent Topic:**[Setting up Service Desk assisted Password Reset in Service Operations Workspace](../concept/setup-password-reset-sow.md)

