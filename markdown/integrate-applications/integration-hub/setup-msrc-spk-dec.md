---
title: Set up the Microsoft Security Response Center spoke
description: Set up an outbound integration between your ServiceNow instance and the Microsoft Security Response Center instance by setting up a connection and credential record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/setup-msrc-spk-dec.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Microsoft Security Response Center Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Microsoft Security Response Center spoke

Set up an outbound integration between your ServiceNow instance and the Microsoft Security Response Center instance by setting up a connection and credential record.

## Before you begin

-   Admin access to the Microsoft Security Response Center portal.
-   Request an Integration Hub subscription.
-   Activate the Microsoft Security Response Center spoke.
-   Role required: admin

## Procedure

1.  Obtain the API key from the Microsoft Security Response Center portal that you must provide in the connection and credential record.

2.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

3.  Click the **Integrations** tab.

4.  Click the **Connections** tab.

5.  In the Search all connections field, enter `Microsoft Security Response Center`.

6.  In the Microsoft Security Response Center tile, select **View Details**.

    \[Omitted image "microsoft-sec-resp-center-view-details.png"\] Alt text: View Details button on Microsoft Security Response Center alias card.

7.  Select **Configure**.

    \[Omitted image "msc-spoke-configure.png"\] Alt text: Configure button to configure Microsoft Security Center spoke connection record.

8.  Fill the Configure Connection form.

<table id="table_khg_jgw_nxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Unique name of the connection record. **Note:** The default and read-only name of the first connection record is Microsoft Security Response Center. To provide a custom connection name, select **Add Connection**to create a connection record.

</td></tr><tr><td>

Connection URL

</td><td>

The URL to the Microsoft Security Response Center server. The URL is https://api.msrc.microsoft.com.

</td></tr><tr><td>

API Key

</td><td>

API key that you copied from the [Microsoft Security Update API](https://portal.msrc.microsoft.com/en-us/developer) page.

</td></tr></tbody>
</table>    \[Omitted image "msc-spoke-connection-form.png"\] Alt text: Connection form.

9.  Select **Configure Connection**.

    The spoke connection is configured and ready to be used.


