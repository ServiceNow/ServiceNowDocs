---
title: Option 2: Using API key
description: Integrate the ServiceNow instance with your UiPath account using API key to authenticate ServiceNow requests.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# Option 2: Using API key

Integrate the ServiceNow instance with your UiPath account using API key to authenticate ServiceNow requests.

## Before you begin

Role required: admin

## Procedure

1.  From your UiPath cloud account, obtain the values of the required API refresh tokens.

    **Note:** These steps are applicable to UiPath cloud account.

    1.  Log in to your UiPath account as an admin.

    2.  Navigate to **Preferences** &gt; **Privacy &amp; Security**.

    3.  For the required tenant, click **View API access**.

        The values of **User Key**, **Organization ID**, **Tenant Name**, and **Client ID** are displayed.

    4.  Copy and record these values.

2.  In your ServiceNow instance, configure the required connection and credential alias.

    1.  Log in to your ServiceNow instance as an admin.

    2.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    3.  Open the record for **UiPath**.

    4.  For **Configuration Template**, select **UiPath Configuration Template - UiPath Cloud** or **UiPath Configuration Template - Private/Public Cloud** as per your requirement.

    5.  Click the **Create New Connection &amp; Credential** related link.

    6.  On the form, fill these fields.

        -   If you have selected **UiPath Configuration Template - UiPath Cloud** for **Configuration Template**, fill these fields.

            **Note:** This option is applicable if you are using UiPath cloud account.

            |Field|Description|
            |-----|-----------|
            |Connection Name|Name to identify the connection record. For example, `UiPath Connection`.|
            |Connection URL|Connection URL in this format: `https://platform.uipath.com/<account-logical-name>/<instance-logical-name>`|
            |Credential Name|Name to identify the credential record. For example, `UiPath Credential`.|
            |Token URL|Location of the token endpoint that the instance uses to retrieve and refresh tokens. For example, `https://account.uipath.com/oauth/token`.|
            |Client Id|Value of client ID you had copied from the UiPath Orchestrator application.|
            |Account Logical Name|Organization ID you had copied from the UiPath Orchestrator application.|
            |Tenant Logical Name|Tenant name you had copied from the UiPath Orchestrator application.|
            |User Key|User key you had copied from the UiPath Orchestrator application.|

        -   If you have selected **UiPath Configuration Template - Private/Public Cloud** for **Configuration Template**, fill these fields.

            |Field|Description|
            |-----|-----------|
            |Connection Name|Name to identify the connection record. For example, `UiPath Connection`.|
            |Connection URL|UiPath instance URL.|
            |Credential Name|Name to identify the credential record. For example, `UiPath Credential`.|
            |Token URL|Location of the token endpoint that the instance uses to retrieve and refresh tokens in this format: `http://<instance-URL>/api/account/authenticate`|
            |Tenant Name|Tenant logical name.|
            |Username or email|Username or email address to authenticate the UiPath Orchestrator API.|
            |Password|Associated password.|

        **Note:**

        -   You must enable **Use MID server** option in the connection record and create a SSL certificate from a trusted authority for on-prem support.
        -   The MID Server users must have the sn\_uipath\_spoke.uipath\_admin role.
    7.  Click **Create**.

    8.  Click **Submit**.

        Connection and credential records are created.

    9.  Open the UiPath Connection record, from the **Connections** tab.

    10. Select a value for the **Orchestrator Feature Enabled** field.


## Result

The Connection and Credential alias is configured and the UiPath spoke is set up using API key.

