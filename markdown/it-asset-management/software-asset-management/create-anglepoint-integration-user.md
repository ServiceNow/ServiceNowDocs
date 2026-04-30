---
title: Create an API user for the Anglepoint integration
description: Create a user who is permitted to access the APIs used by the Anglepoint integration. These APIs provide the given user access to the Anglepoint integration resources that are available on your ServiceNow instance.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Creating a connection for the Anglepoint integration, Authorized SAM Provider \(ASP\) integrations for IBM, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Create an API user for the Anglepoint integration

Create a user who is permitted to access the APIs used by the Anglepoint integration. These APIs provide the given user access to the Anglepoint integration resources that are available on your ServiceNow instance.

## Before you begin

Role required: admin

## About this task

The Anglepoint integration uses the following APIs:

|API|API path|Description|
|---|--------|-----------|
|Transform \(POST\)|/api/sn\_samp\_ibm\_lic/ibm\_data/transform|Processes information for your installed IBM software.|
|Get Computer|/api/sn\_samp\_ibm\_lic/ibm\_data/computer|Retrieves information about the virtual machines \(VMs\) and hosts that your IBM software is installed on.|
|Get Entitlements|/api/sn\_samp\_ibm\_lic/ibm\_data/entitlement|Retrieves entitlement information for your installed IBM software.|
|Get Classification|/api/sn\_samp\_ibm\_lic/ibm\_data/classification|Retrieves classification information for your installed IBM software.|
|Post Classification|/api/sn\_samp\_ibm\_lic/ibm\_data/classification|Sends classification information for your installed IBM software.|

## Procedure

1.  Navigate to **All** &gt; **Organization** &gt; **Users** and then select **New**.

2.  On the form, fill in the fields.

<table id="table_dgy_by2_svb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User ID

</td><td>

Unique identifier for the user.

</td></tr><tr><td>

First name

</td><td>

First name of the user.

</td></tr><tr><td>

Last name

</td><td>

Last name of the user.

</td></tr><tr><td>

Title

</td><td>

Job title or job description of the user.

</td></tr><tr><td>

Department

</td><td>

Department that the user belongs to.

</td></tr><tr><td>

Password needs reset

</td><td>

Option to require the user to change the assigned password during the first login.**Note:** This option must be disabled.

</td></tr><tr><td>

Locked out

</td><td>

Option to lock the user out of the ServiceNow instance and terminate all active sessions.

</td></tr><tr><td>

Active

</td><td>

Option that indicates the user is active.**Note:** This option must be enabled.

</td></tr><tr><td>

Web service access only

</td><td>

Option to designate the user as a non-interactive user. Non-interactive users can use only assigned credentials to authorize API connections, including JSON, SOAP, and WSDL. See [Non-interactive sessions](https://www.servicenow.com/docs/access?context=c_NonInteractiveSessions&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for more information on non-interactive users.**Note:** This option must be enabled.

</td></tr><tr><td>

Internal Integration User

</td><td>

Option to designate the user as an internal integration user. See [Mark service accounts as internal integration users](https://www.servicenow.com/docs/access?context=t_MarkSvcAcctsAsInternalIntegUsers&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) for more information on internal integration users.

</td></tr><tr><td>

Email

</td><td>

Email address of the user.

</td></tr><tr><td>

Language

</td><td>

Language preference of the user.

</td></tr><tr><td>

Calendar integration

</td><td>

Calendar through which the user receives meeting invitations and notifications.

</td></tr><tr><td>

Time zone

</td><td>

Time zone that the user is located in.

</td></tr><tr><td>

Date format

</td><td>

Preferred date format for the user.

</td></tr><tr><td>

Business phone

</td><td>

Business phone number that is assigned to the user.

</td></tr><tr><td>

Mobile phone

</td><td>

Mobile phone number that is assigned to the user.

</td></tr><tr><td>

Photo

</td><td>

Photo of the user.

</td></tr></tbody>
</table>3.  Right-click the form header and then select **Save**.

    The form automatically reloads with additional form actions, related links, and related tabs.

4.  Generate a password for the user.

    1.  Select **Set Password**.

        The Set Password dialog box opens.

    2.  In the dialog box, select **Generate**.

        Your ServiceNow instance automatically generates a password for the user.

    3.  Copy the value in the **Password** field.

        Save it in a secure location for later use.

    4.  Select **Save Password**.

        The dialog box closes and you automatically return to the User form.

5.  Assign roles to the user.

    1.  On the **Roles** related tab, select **Edit...**.

    2.  From the Collection list on the Edit Members form, search for and select the following roles:

        -   snc\_platform\_rest\_api\_access
        -   oauth\_user
        -   sn\_samp\_ibm\_lic.sam\_ibm\_data\_integrator
    3.  Select the Add button ![Add button.](../image/add-icon.png) to move the selected roles from the Collection list to the Roles List.

    4.  Select **Save**.

        The Edit Members form closes and you automatically return to the User form.

    5.  Verify that all selected roles appear on the **Roles** related tab.


**Parent Topic:**[Creating a connection for the Anglepoint integration](../concept/creating-connection-anglepoint-elevate-platform.md)

