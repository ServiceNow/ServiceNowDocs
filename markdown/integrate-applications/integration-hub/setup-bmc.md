---
title: Set up the BMC Remedy spoke
description: Integrate the ServiceNow instance and BMC Remedy by using Remedy credentials to authenticate ServiceNow requests.Create Credential records for your BMC Remedy application. The BMC Remedy spoke connection and credential alias uses these credentials to authorize actions.Create Connection record for your BMC Remedy application. The BMC Remedy spoke connection and credential alias uses this connection to perform actions in BMC Remedy.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [BMC Remedy Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the BMC Remedy spoke

Integrate the ServiceNow instance and BMC Remedy by using Remedy credentials to authenticate ServiceNow requests.

## Before you begin

-   Request Integration Hub subscription.
-   Activate the BMC Remedy spoke.
-   Role required: admin.

**Note:** Ensure that you perform these steps in the **BMC Remedy Spoke** application scope only.

## Create Credential record for the BMC Remedy spoke

Create Credential records for your BMC Remedy application. The BMC Remedy spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the record for the **BMC Remedy spoke** whose **Type** is **Credential**, for example, `BMCRemedy_Credential`.

3.  From the **Credentials** tab, click **New**.

    The system displays the message `What type of Credentials would you like to create?`.

4.  Select **Remedy Credential**.

5.  On the form, fill in the fields.

<table id="table_sxv_zgp_gfb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, `Remedy Cred`.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the credential record.

</td></tr><tr><td>

User name

</td><td>

User name of the BMC Remedy user.**Note:** Administrator user isn't necessary. However, ensure that the BMC Remedy user has permissions to perform the required change, incident, and problem management actions.

</td></tr><tr><td>

Password

</td><td>

Password of the BMC Remedy user's account.

</td></tr><tr><td>

Credential alias

</td><td>

Credential alias record associated with this record.

</td></tr><tr><td>

Token Status

</td><td>

Status of the BMC Remedy token. Select **Active**.

</td></tr><tr><td>

Applies to

</td><td>

MID Servers that can use this credential record.

</td></tr><tr><td>

MID servers

</td><td>

Specific MID Servers that can use this credential record.**Note:** This field appears only when **Specific MID servers** is selected from **Applies to**.

</td></tr></tbody>
</table>6.  Right-click the form header and click **Save**.


### Result

The credential record the BMC Remedy spoke is created.

## Create Connection record for the BMC Remedy spoke

Create Connection record for your BMC Remedy application. The BMC Remedy spoke connection and credential alias uses this connection to perform actions in BMC Remedy.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the record of **BMC Remedy spoke** whose **Type** is **Connection and Credential**, for example, `BMCRemedy`.

3.  From the **Connections** tab, click **New**.

4.  On the form, fill these values.

    |Field|Value required|
    |-----|--------------|
    |Name|Name to uniquely identify the connection record. For example, enter `BMC Remedy Connection`.|
    |Credential|Credential record you created for BMC Remedy. For example, select **Remedy Cred**.|
    |Connection alias|Connection alias associated with this record.|
    |URL builder|Option to manually enter the connection URL or use system to build the URL based on the inputs.|
    |Connection URL|URL to launch the BMC Remedy application. For example, `http://<bmc-remedy-localhost>:8008/api`|
    |Use MID server|Option to use a MID Server.|
    |Capabilities|Capability of the MID Server. This field appears only when the **Use MID server** option is selected.|
    |MID Application|Option to use a MID Server. This field appears only when the **Use MID server** option is selected.|
    |Active|Option to actively use the connection record.|
    |Domain|Domain that the action runs in.|

5.  Click **Submit**.


### Result

The connection record the BMC Remedy spoke is created.

