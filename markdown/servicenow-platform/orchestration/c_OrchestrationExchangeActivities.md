---
title: Exchange activity pack
description: The Exchange activity pack allows workflows to manage Microsoft Exchange mail systems.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Exchange activity pack

The Exchange activity pack allows workflows to manage Microsoft Exchange mail systems.

The use of Orchestration Exchange activities requires the following:

-   Microsoft Exchange 2010, 2013, or 2016.
-   A MID Server configured to run Powershell 2.0
-   A target Exchange server in the same Active Directory domain as the instance.
-   Powershell Remoting enabled on the target Exchange server.

**Note:** These activities cannot be used to interact with Microsoft Exchange Online.

Orchestration provides custom Exchange activities that were created with the Orchestration activity designer template. These activities perform the same functions as Exchange activities by the same name from previous releases and replace those activities for all new workflows. The custom Exchange activities were built with a [Powershell activity template](../../orchestration-activity-designer/task/t_CreateAPowershellActivity.md#), which gives workflow administrators the ability to store input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

**Note:** Existing workflows from earlier versions that were created with legacy Exchange activities continue to function normally after an upgrade to Geneva. However, all new workflows must use these custom Exchange activities.

To use the Microsoft Exchange custom activities, you must [request activation](../task/t_ActivateAnActivityPack.md) of the Orchestration - Exchange plugin. The custom Exchange activities are available in the Workflow Editor on the **Custom** tab. Expand the **Custom Activities** tree and select the **Exchange** category for the activity you want to use.

![Accessing custom exchange activities](../image/CustomExchangeActivities.png "Accessing custom Exchange activities")

-   **[Configure MID Server for Exchange](../task/t_ConfigureMIDServerForExchange.md)**  
Configure a MID Server with defined IP ranges to use Exchange.
-   **[Pass multivalued properties with an Exchange activity](../task/t_PassMultivaluedProperties.md)**  
To set a multivalued property using an Exchange activity, you must use a specific parameter format.
-   **[Create Address List activity](../reference/r_CreateAddressListActivity.md)**  
The Create Address List activity creates a new address list that acts as an alias for emailing all users in the group.
-   **[Delete Address List activity](../reference/r_DeleteAddressListActivity.md)**  
The Delete Address List activity removes an existing address list from an Exchange server.
-   **[Get Address List activity](../reference/r_GetAddressListActivity.md)**  
The Get AddressList activity retrieves all attributes from the specified Exchange address list.
-   **[Move Address List activity](../reference/r_MoveAddressListActivity.md)**  
The Move Address List activity moves a Microsoft Exchange address list to another location in the address hierarchy.
-   **[Set Address List activity](../reference/r_SetAddressListActivity.md)**  
The Set Address List activity modifies a Microsoft Exchange address list.
-   **[Update Address List activity](../reference/r_UpdateAddressListActivity.md)**  
The Update Address List activity adds or removes users from the specified address list and immediately applies any cached address list changes to the server.
-   **[Create Mailbox activity](../reference/r_CreateMailboxActivity.md)**  
The Create Mailbox activity creates a new Active Directory user, if that user does not already exist, and a Microsoft Exchange mailbox for that user.
-   **[Delete Mailbox activity](../reference/r_DeleteMailboxActivity.md)**  
The Delete Mailbox activity deletes the Microsoft Exchange mailbox of an Active Directory user.
-   **[Disable Mailbox activity](../reference/r_DisableMailboxActivity.md)**  
The Disable Mailbox activity disables the mailbox associated with a specified Active Directory account.
-   **[Enable Mailbox activity](../reference/r_EnableMailboxActivity.md)**  
The Enable Mailbox activity creates a new mailbox for an existing Active Directory user.
-   **[Get Mailbox activity](../reference/r_GetMailboxActivity.md)**  
The Get Mailbox activity gets the mailbox for the specified user or all mailboxes on a Microsoft Exchange server.
-   **[Set Mailbox activity](../reference/r_SetMailboxActivity.md)**  
The Set Mailbox activity modifies the settings of an existing Microsoft Exchange mailbox.

**Parent Topic:**[Orchestration activity packs](c_OrchestrationActivityPacks.md)

