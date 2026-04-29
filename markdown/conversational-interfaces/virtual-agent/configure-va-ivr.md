---
title: Configure Conversational IVR with Amazon Connect
description: Configure Amazon Connect service provider to integrate with Virtual Agent and use interactive voice response.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring Conversational IVR with Amazon Connect, Conversational IVR with Amazon Connect, Integrating Virtual Agent with Voice channels, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Configure Conversational IVR with Amazon Connect

Configure Amazon Connect service provider to integrate with Virtual Agent and use interactive voice response.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings** &gt; **Virtual Agent**.

2.  On the Virtual Agent Settings page, navigate to the **Configure your interactive voice response \(IVR\)** tile.

    **Note:** To see the **Configure your interactive voice response \(IVR\)** tile on your Virtual Agent Settings page, ensure that you have updated the Omni-Experience Standard Feature Set plugin \(sn\_oe\_sfs\).

3.  In the Configure pre-built adapter section, click **Configure IVR**.

4.  In the Select IVR service provider page, select **VA Amazon Connect Adapter Provider** as the IVR service provider from the drop-down.

    **Note:** VA Amazon Connect Adapter Provider is available by default, with the Conversational IVR with Amazon Connect application installation. To use the Amazon Connect adapter, get the Conversational IVR with Amazon Connect app from the ServiceNow Store.

    Conversational IVR with Amazon Connect supports multiple service provider applications and you can create new ones if you want.

    ![Selecting the VA Amazon Connect Service Provider for configuring interactive voice response.](../images/amzn-cnct-provider.png)

5.  To finish setting up Amazon Connect, select the application name from the Provider Channel Identities section.

6.  On the form, fill in the fields.

    **Note:** From the AWS Console, copy and paste the authentication information for Amazon Connect below:

<table id="table_i4h_1sn_5tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Identifier Type

</td><td>

Indicates the type of identifier for the provider channel identity.For example, you can configure Amazon Connect on your ServiceNow instance via Phone number or ARN.

</td></tr><tr><td>

Phone number

</td><td>

The phone number being configured for this provider channel identity.**Note:**

-   The **Phone number** field is available only when you select Phone Number in the **Identifier Type** drop-down.
-   From Vancouver release, you can use multiple phone numbers from an AWS account and create provider identity channels for each configuration to accommodate multiple points of contact.


</td></tr><tr><td>

Instance ARN

</td><td>

The instance ARN from the AWS Console.

</td></tr><tr><td>

Static/hash token

</td><td>

Your static or hash token from AWS Console.

</td></tr><tr><td>

Token type

</td><td>

Confirmation for the token provided in the **Static/hash token** field.

</td></tr><tr><td>

Connect Login URL

</td><td>

The login URL from the AWS Console.

</td></tr></tbody>
</table>7.  Click **Save**.


## What to do next

-   [Sync agents to set up live agent transfer](setup-live-agent-transfer.md)
-   [Configure user authentication for Conversational IVR](setup-user-authentication-ivr.md)
-   [Manage bot messages for Conversational IVR](edit-va-ivr-messages.md)

-   **[Enroll user Soft PIN and Device in ServiceNow instance](enrol-user-softpin-device.md)**  
Enroll the user Soft PIN and Device in your ServiceNow instance to setup callback authentication.
-   **[Set up the Amazon Connect spoke for Conversational IVR](setup-amzn-connect-spoke.md)**  
Set up the Amazon Connect spoke to integrate your ServiceNow instance with Amazon Connect.
-   **[Sync agents to set up live agent transfer](setup-live-agent-transfer.md)**  
After the installation and configuration of Amazon Connect, you must sync agents to enable live transfer. You can sync agents stored in Amazon Connect with the agents on your ServiceNow agents.
-   **[Configure user authentication for Conversational IVR](setup-user-authentication-ivr.md)**  
You must configure the authentication level for how the end-user can be authenticated to be the logged-in ServiceNow user using Voice.
-   **[Manage bot messages for Conversational IVR](edit-va-ivr-messages.md)**  
Edit your custom messages to ensure that your conversations are optimized for Conversational IVR.
-   **[Provider properties for Amazon Connect](provider-properties-ivr.md)**  
View and update the provider properties available for Amazon Connect

**Parent Topic:**[Configuring Conversational IVR with Amazon Connect](../concept/configuring-ci-ivr-amazon-connect.md)

