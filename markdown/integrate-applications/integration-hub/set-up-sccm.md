---
title: Set up SCCM spoke
description: Integrate the ServiceNow instance and SCCM using Windows credentials to authenticate ServiceNow requests.Create a Credential record to the SCCM server. The SCCM spoke connection and credential alias uses this credential to authorize actions.Create a Connection record to your SCCM host machine. The SCCM spoke connection and credential alias uses this connection to perform actions in SCCM.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Microsoft SCCM Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up SCCM spoke

Integrate the ServiceNow instance and SCCM using Windows credentials to authenticate ServiceNow requests.

## Before you begin

-   Request Integration Hub subscription
-   Role required: admin
-   [Configure the MID Server for SCCM activities](https://www.servicenow.com/docs/access?context=t_ConfigMIDServerForSCCMActivities&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

**Note:** Ensure that user must be able to establish remote PowerShell sessions with the Microsoft SCCM server. The spoke scripts use **Microsoft.PowerShell32** configuration for creating sessions. For user permissions, see [User permissions](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_remote_requirements?view=powershell-7.4#user-permissions) in [Microsoft Learn](https://learn.microsoft.com/en-us/).

## Create Credential record for the SCCM spoke

Create a Credential record to the SCCM server. The SCCM spoke connection and credential alias uses this credential to authorize actions.

### Before you begin

-   Request Integration Hub subscription
-   Role required: admin
-   [Configure the MID Server for SCCM activities](https://www.servicenow.com/docs/access?context=t_ConfigMIDServerForSCCMActivities&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message **What type of Credentials would you like to create?**.

3.  Select **Windows Credentials**.

    A blank Windows Credentials form displays.

4.  Enter these values, then click **Submit**.

    |Field|Value required|
    |-----|--------------|
    |Name|Enter any name to uniquely identify the record. For example, enter `SCCM Credential`.|
    |Active|Enable|
    |User name|Enter a user name with access to the target Windows host. For more information about Windows permissions, see [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).|
    |Password|Enter the password for the account.|
    |Applies to|Select the MID Servers that can use this credential. For example, select **All MID servers**.|
    |Order|Select the order to apply this credential. For example, enter `100`.|


## Create Connection record for the SCCM spoke

Create a Connection record to your SCCM host machine. The SCCM spoke connection and credential alias uses this connection to perform actions in SCCM.

### Before you begin

-   Request Integration Hub subscription
-   [Create Credential record for the SCCM spoke](set-up-sccm.md#)
-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open for the record for **SCCM**.

3.  From the **Connections** tab, click **New**.

    The system displays a blank Basic Connection form.

4.  Enter these values, then click **Submit**.

    |Field|Value required|
    |-----|--------------|
    |Name|Enter any name to uniquely identify the connection record. For example, enter `SCCM Connection`.|
    |Credential|Select the Credential record you created for Windows. For example, select **SCCM Credential**.|
    |Host|Enter the fully qualified domain name of the target host where the SCCM server is installed. For example, `<host>.<domain>.com`.|
    |Use MID server|Enable|
    |Override default port|Enter the target port used by the connection. If blank, the system uses the default port.|


### What to do next

[Configure MID Server as WinRM trusted host](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

