---
title: Configure a connection for the Oracle Peoplesoft Financial spoke
description: Configure a connection to your Oracle Peoplesoft Financial instance. The Oracle Peoplesoft Financial spoke connection and credential aliases use these connections to perform actions in Oracle Peoplesoft Financial.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/integration-hub/psft-fin-conctn-config.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-10-14"
reading_time_minutes: 1
breadcrumb: [Set up the Oracle Peoplesoft Financial spoke, Oracle Peoplesoft Financial Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Configure a connection for the Oracle Peoplesoft Financial spoke

Configure a connection to your Oracle Peoplesoft Financial instance. The Oracle Peoplesoft Financial spoke connection and credential aliases use these connections to perform actions in Oracle Peoplesoft Financial.

## Before you begin

Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **Oracle\_PeopleSoft** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Oracle Peoplesoft Financial spoke, click **View Details**.

        \[Omitted image "psft-fin-connection.png"\] Alt text: Connection for the Oracle Peoplesoft Financial spoke with View Details highlighted.

    -   To manage more than one Oracle Peoplesoft Financial spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/integration-hub/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    \[Omitted image "psft-fin-connection-conf.png"\] Alt text: Initial connection configuration with Configure highlighted.

5.  On the form, fill in these fields:

<table id="table_psf_001_a06"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td colspan="2">

Connection Information

</td></tr><tr><td>

Connection Name

</td><td>

Name to identify the Oracle Peoplesoft Financial connection record.

</td></tr><tr><td>

Connection URL

</td><td>

Base URL obtained from the generated WSDL URL. **Note:** Remove the `<webservice-endpoint>.wsdl` part of the WSDL URL while specifying the Connection URL.

</td></tr><tr><td colspan="2">

Credential Information

</td></tr><tr><td>

User Name

</td><td>

User name with the required permissions to log in to your Oracle Peoplesoft Financial instance.

</td></tr><tr><td>

Password

</td><td>

Password to log in to your Oracle Peoplesoft Financial instance.

</td></tr></tbody>
</table>    \[Omitted image "psft-fin-conf-temp.png"\] Alt text: Configure a connection for the Oracle Peoplesoft Financial spoke.

6.  Click **Save**.


## Result

The Oracle Peoplesoft Financial spoke connection is configured and ready to be used.

