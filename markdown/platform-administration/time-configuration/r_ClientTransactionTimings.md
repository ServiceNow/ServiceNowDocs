---
title: Client transaction timings
description: The Client Transaction Timings plugin enhances the system logs by providing additional information about the durations of transactions taking place between the client and the server.
locale: en-US
release: australia
product: Time Configuration
classification: time-configuration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Client transaction timings

The Client Transaction Timings plugin enhances the system logs by providing additional information about the durations of transactions taking place between the client and the server.

You can track down performance issues to their source by viewing where the time is being consumed, and how time was spent during a transaction.

This plugin requires the [Response Time Indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_ResponseTimeIndicator.md) [Response Time Indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_ResponseTimeIndicator.md) to be enabled, and collects information from the following browsers:

-   Firefox
-   Internet Explorer
-   Chrome

## Client Transactions Information

Installing the plugin adds the Client Transactions module to the System Logs application. It provides a list of every logged transaction between client and server within the last day:

<table id="table_h2d_ljs_44"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Created

</td><td>

Moment the transaction was recorded.

</td></tr><tr><td>

Response Time

</td><td>

Number of ms spent by the server in fulfilling the transaction.

</td></tr><tr><td>

Business Rule Time

</td><td>

Number of ms spent by business rules triggered by the transaction.

</td></tr><tr><td>

SQL Time

</td><td>

Number of ms spent by the SQL database.

</td></tr><tr><td>

Client Response Time

</td><td>

\(Load\_completion\_time\) - \(start\_time\). It is inclusive of server time.

</td></tr><tr><td>

Client Network Time

</td><td>

Number of ms spent by the network the client is connecting through.

</td></tr><tr><td>

Browser Time

</td><td>

Number of ms spent by the browser during the transaction.

</td></tr><tr><td>

Client Script Time

</td><td>

The number of ms spent executing client scripts.

</td></tr><tr><td>

UI Policy Time

</td><td>

Number of ms spent executing ui policy.

</td></tr><tr><td>

Type

</td><td>

Type of transaction:-   Form
-   List
-   Other

</td></tr><tr><td>

Table

</td><td>

Name of table that appeared. For example, incident, change\_request.

</td></tr><tr><td>

View

</td><td>

View for this form/list.

</td></tr></tbody>
</table>## Client Detailed Information

A more detailed breakdown of the client timings for all Form rendering \(but not list rendering\) is also tracked. To see details, drill into a particular client transaction record and observe the related list at the base of the screen.

|Field|Description|
|-----|-----------|
|Order|Order during the load in which this operation occurred.|
|Type|Type of operation.|
|Name|Descriptive name of this particular operation|
|Duration|Number of ms this operation took to complete.|

-   **[Components installed with Client Transaction Timings](../concept/c_InstalledComponents.md)**  
The Client Transaction Timings plugin installs several components.
-   **[Timing values](r_TimingValues.md)**  
Timing values are broken down into several sections.

**Parent Topic:**[Time configuration references](../reference-time-configuration.md)

