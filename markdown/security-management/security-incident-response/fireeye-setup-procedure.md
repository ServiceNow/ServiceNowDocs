---
title: Set up your NowPlatform instance for FireEye integration
description: Verify and review the following configuration procedure to set up NowPlatform instance for Fireeye integration.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [FireEye Endpoint Security integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up your NowPlatform instance for FireEye integration

Verify and review the following configuration procedure to set up NowPlatform instance for Fireeye integration.

## Before you begin

Role required: ServiceNow AI Platform administrator \(sn\_si.admin\)

The following section lists the setup tasks that are required to complete in your NowPlatform instance prior to installing the application for the FireEye integration.

Verify that you have completed the following tasks before you install the application from ServiceNow Store.

<table id="table_rbn_ppy_4qb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verify that you have assigned the required NowPlatform and Security Incident Response \(SIR\) roles.

</td><td>

The following roles are required:1.  User with system administrator \(admin\) role is required to install the application for the integration.
2.  User with security incident administrator \(sn\_si.admin\) role is required to configure the integration, create, activate, and remove profiles.
3.  User with security incident analyst \(sn\_si.analyst\) role is required to work with security incidents. A user with this role can initiate any of the capabilities available in the integration.

</td></tr><tr><td>

Verify that you have installed and configured a MID Server.

</td><td>

Configure MID Server: A MID Server in your NowPlatform instance is required to manage files and connect to the FireEye service deployed within your organization network. For more information on MID servers, see [https://servicenow.com/docs](https://servicenow.com/docs)

</td></tr><tr><td>

Verify that the ServiceNow core applications that are required to support the integration are installed and activated before you install the application.

</td><td>

The following applications must be installed and activated from the ServiceNow Store before installing this application. Install and then activate one application at a time in the order listed below to ensure a smooth installation:1.  Security Incident Response Support
2.  Security Support Core
3.  Security Support Common
4.  Security Incident Response
5.  Threat Intelligence Support Common
6.  ServiceNow Integration Hub Enterprise Pack Installer

</td></tr><tr><td>

Before you enable the approval option for profiles, verify that you have created an approval group.

</td><td>

An optional approval workflow is available for isolating host machines, restoring them back to the network, getting file, and running additional actions on end point.If your organization wants an extra level of control over these actions, enable the Require approval option during the configuration of the profiles.

 In the absence of a profile if a capability is invoked from the Related List directly, Approvals can be handled from the FireEye default setting module.

 As a Security Administrator, you can set up approval while configuring the profiles and the default settings. An approval group must be available on the Groups list in your instance.

</td></tr><tr><td>

 

</td><td>

 

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **User Administration** &gt; **Groups**.

2.  Click **New** in the Groups list.

3.  Fill the form with the following details:

    |Field|Description|
    |-----|-----------|
    |Name|Name of the group that is displayed when an approval request is submitted.|
    |Group email|\(Optional\) Group email distribution list or the email address of the point of contact, such as the group manager.|
    |Manager|\(Optional\) Name of group manager. Click the search icon to view the list.|
    |Parent|\(Optional\) Name of the parent group, if associated with a parent.|
    |Hourly rate|\(Optional\) The amount paid for every hour worked.|
    |Description|\(Optional\) Additional information about the group.|

4.  Click **Submit**.

    ![Group list](../image/fireeye-users.png)

    The new group is displayed in the Groups list. You have successfully created an approval group. Add users to your new group as required who can approve the requests submitted by the security analyst. A user inherits roles from all groups to which the user belongs. You can also assign roles directly to a user.

    To monitor and process requests submitted by users with the sn\_si.analyst role, each member of the approval group should navigate to My Approvals in the ServiceNow AI Platform. Alternatively, the approvers can find the requests submitted specifically for FireEye integration under the FireEye Approvals.


## What to do next

The next step is to install and configure the application from ServiceNow Store.

