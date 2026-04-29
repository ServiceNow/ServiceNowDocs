---
title: Access Management Automation
description: Automate access management request fulfillment using the Service Catalog or Service Portal. The catalog items and flows support requests in Okta, Microsoft Entra ID \(formerly Microsoft Entra ID\), and Microsoft Active Directory.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure a catalog in Service Portal, Create a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Access Management Automation

Automate access management request fulfillment using the Service Catalog or Service Portal. The catalog items and flows support requests in Okta, Microsoft Entra ID \(formerly Microsoft Entra ID\), and Microsoft Active Directory.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Application version

Access Management Automation v2.1.0 is the latest version.

## Catalog Items and flows

The Access Management Automation application provides catalog items and flows to automate tasks. When a catalog item is submitted, the related flow is triggered and the task is performed. Available catalog items include:

|Service|Catalog Item|Description|
|-------|------------|-----------|
|Microsoft Active Directory|Create Active Directory Group|Creates a group in Microsoft Active Directory with the provided details.|
|Create Active Directory User|Creates a user in Microsoft Active Directory.|
|Remove Active Directory User from Groups|Removes the specified user from the groups in the Microsoft Active Directory.|
|Enable Active Directory User|Enables the specified user in the Microsoft Active Directory.|
|Disable Active Directory User|Disables the specified user in the Microsoft Active Directory.|
|Add Active Directory User to Groups|Adds the specified user to groups in the Microsoft Active Directory.|
|Unlock Active Directory User|Unlocks the specified user in the Microsoft Active Directory.|
|Microsoft Entra ID \(formerly Microsoft Entra ID\)|Delete Microsoft Entra ID User|Deletes the specified user from Microsoft Entra ID.|
|Add Microsoft Entra ID User to Groups|Adds the specified user to groups in the Microsoft Entra ID.|
|Create Microsoft Entra ID Security Group|Creates a security group in Microsoft Entra ID.|
|Remove Owner From Microsoft Entra ID Group|Removes an owner from the specified Microsoft Entra ID group.|
|Create Microsoft Entra ID O365 Group|Creates an Office 365 group in the Microsoft Entra ID.|
|Disable Microsoft Entra ID User|Disables the specified user in the Microsoft Entra ID.|
|Enable Microsoft Entra ID User|Enables the specified user in the Microsoft Entra ID.|
|Remove Microsoft Entra ID User from Groups|Removes the specified user from groups in the Microsoft Entra ID.|
|Add Owner to Microsoft Entra ID Group|Adds an owner to the Microsoft Entra ID group.|
|Create Microsoft Entra ID User|Creates a user in Microsoft Entra ID.|
|Okta|Reset Okta User Factors|Resets factors of the specified Okta user.|
|Add Okta User to Okta Groups|Adds the specified user to groups at Okta.|
|Unlock Okta User|Unlocks the specified user at Okta.|
|Unsuspend Okta User|Unsuspends the specified user at Okta.|
|Create Group at Okta|Creates a group in Okta.|
|Create User at Okta|Creates a user at Okta.|
|Suspend Okta User|Cancels the specified user at Okta.|
|Remove Okta User from Okta Groups|Removes the specified user from groups in Okta.|
|Activate Okta User|Activates the specified user at Okta.|

## Subflows

The Access Management Automation application provides subflows to automate tasks. The available subflows include:

|Subflow|Description|
|-------|-----------|
|Create Incident|Creates an incident if automation fails.|
|Create Event|Creates an event if automation fails.|
|Dynamic Flow Template|Template to use the Create Event and Create Incident subflows.|
|Fetch Approvers and Assignee|Retrieves the details of approvers, assignees, and assignment groups for the requested item, catalog task, and incident from the decision tables.|

## Actions

The Access Management Automation application provides actions to automate tasks. The available subflows include:

|Action|Description|
|------|-----------|
|Convert Mask to password2|Converts a mask field to a password2 field.|
|Convert String to Array.Strings|Converts a string of comma-separated values to an array of strings.|

## Decision tables

The Access Management Automation application uses decision tables to save the approver and assignee information. The decision tables include:

|Decision table|Description|
|--------------|-----------|
|Access Mgmt. Catalog Task Group Assignment Policy|Used to choose the groups to assign the fulfillment catalog task to, if the automation fails.|
|Access Mgmt. Catalog Task User Assignment Policy|Used to choose the users to assign the fulfillment catalog task to, if automation fails.|
|Access Mgmt. Failed Automation Flow Policy|Used to choose the subflow that should execute if automation fails.|
|Access Mgmt. Incident Group Assignment Policy|If the subflow that executes when automation fails is Create Incident, this decision table is used to choose the groups to assign the incident to.|
|Access Mgmt. Incident User Assignment Policy|If the subflow that executes when automation fails is Create Incident, this decision table is used to choose the users to assign the incident to.|
|Access Mgmt. Requested Item Group Approval Policy|Used to choose the groups assigned as approver for the catalog requests.|
|Access Mgmt. Requested Item User Approval Policy|Used to choose the users assigned as approver for the catalog requests.|

## User roles

The Access Management Automation application provides the sn\_acc\_mgmt\_sc.access\_mgmt\_user role. Users with this role can view access management automation catalog items.

**Note:** User must have the sn\_acc\_mgmt\_sc.access\_mgmt\_user, ITIL, and Catalog Admin roles to create and submit catalog items.

