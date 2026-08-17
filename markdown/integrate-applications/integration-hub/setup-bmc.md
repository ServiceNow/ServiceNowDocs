---
title: Set up the BMC Remedy spoke
description: Integrate the ServiceNow instance and BMC Remedy by using Remedy credentials to authenticate ServiceNow requests.Create Credential records for your BMC Remedy application. The BMC Remedy spoke connection and credential alias uses these credentials to authorize actions.Create Connection record for your BMC Remedy application. The BMC Remedy spoke connection and credential alias uses this connection to perform actions in BMC Remedy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/setup-bmc.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [BMC Remedy Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the BMC Remedy spoke

Integrate the ServiceNow instance and BMC Remedy by using Remedy credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
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

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **BMCRemedy** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the BMC Remedy spoke, click **View Details**.

        \[Omitted image "image.BMCRem\_Connection"\] Alt text: BMC Remedy spoke connection

    -   To manage more than one BMC Remedy spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    \[Omitted image "image.BMCRem\_Connect\_Conf"\] Alt text: BMC Remedy spoke connection configuration

5.  On the form, fill in these fields:

    |Field|Value required|
    |-----|--------------|
    |Connection Information|
    |Name|Auto-generated name to identify the connection record.|
    |URL|URL of the connection website.|
    |Credential Information|
    |User Name|User name of the BMC Remedy user.|
    |Password|Password of the BMC Remedy user's account.|
    |Token Status|Status of the BMC Remedy token. Select `Active`.|

    \[Omitted image "image.BMCRem\_Config\_temp"\] Alt text: BMC Remedy spoke configuration template.

6.  Click **Configure and Get OAuth Token**.


### Result

The connection record the BMC Remedy spoke is created.

