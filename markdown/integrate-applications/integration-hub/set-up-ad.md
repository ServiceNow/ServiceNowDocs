---
title: Set up Microsoft Active Directory spoke
description: Integrate the ServiceNow instance and your Microsoft AD account using Windows credentials to authenticate ServiceNow requests.Create a Credential record for the Microsoft Active Directory host. The Microsoft AD spoke connection and credential alias uses this credential to authorize actions.Create a Connection record to your Microsoft Active Directory host machine. The Microsoft AD spoke connection and credential alias uses this connection to perform actions in Microsoft Active Directory.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Microsoft Active Directory Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up Microsoft Active Directory spoke

Integrate the ServiceNow instance and your Microsoft AD account using Windows credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Microsoft Active Directory spoke.
-   Role required: admin.

## Create Credential record for the Microsoft AD spoke

Create a Credential record for the Microsoft Active Directory host. The Microsoft AD spoke connection and credential alias uses this credential to authorize actions.

### Before you begin

-   Request Integration Hub subscription
-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message **What type of Credentials would you like to create?**.

3.  Select **Windows Credentials**.

    A blank Windows Credentials form displays.

4.  Enter these values.

    |Field|Value required|
    |-----|--------------|
    |Name|Enter any name to uniquely identify the record. For example, enter `AD Credential`.|
    |Active|Enable|
    |User name|Enter a user name with access to the target Windows host. For more information about Windows permissions, see [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).|
    |Password|Enter the password for the account.|
    |Applies to|Select the MID Servers that can use this credential. For example, select **All MID servers**.|
    |Order|Select the order to apply this credential. For example, enter `100`.|

5.  Click **Submit**.


## Create Connection record for the Microsoft AD spoke

Create a Connection record to your Microsoft Active Directory host machine. The Microsoft AD spoke connection and credential alias uses this connection to perform actions in Microsoft Active Directory.

### Before you begin

-   Request Integration Hub subscription
-   [Create Credential record for the Microsoft AD spoke](set-up-ad.md#)
-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Click Connections.

3.  On the AD card, click **View Details**.![Microsoft AD connection card.](../image/click-AD-spoke-card.png)

4.  Click **Configure**.![Configure button to configure Microsoft AD alias connection record.](../image/click-AD-alias-connection.png)

5.  Enter these values.

    |Field|Value required|
    |-----|--------------|
    |Name|Enter any name to uniquely identify the connection record. For example, enter `AD Connection`.|
    |Credential|Select the Credential record you created for Windows Active Directory. For example, select **AD Credential**.|
    |Host|Enter the fully qualified domain name of the target host where Microsoft Active Directory is installed. For example, `<host>.<domain>.com`.|
    |Use MID server|Enable|
    |Override default port|Enter the target port used by the connection. If blank, the system uses the default port.|

6.  Click **Submit**.


