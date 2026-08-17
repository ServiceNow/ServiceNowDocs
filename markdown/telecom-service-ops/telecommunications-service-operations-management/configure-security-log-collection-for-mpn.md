---
title: Configure security log collection for MPN
description: Configure the out-of-box Health Log Analytics security log data input, an Elasticsearch collector, to collect Mobile Private Network \(MPN\) security logs and convert them into structured log records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/configure-security-log-collection-for-mpn.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-07-15"
reading_time_minutes: 3
keywords: [Nokia MPN, security log, Elastic data input, Health Log Analytics]
breadcrumb: [Configure Telecom Assurance, Configure, Telecommunications Service Operations Management]
---

# Configure security log collection for MPN

Configure the out-of-box Health Log Analytics security log data input, an Elasticsearch collector, to collect Mobile Private Network \(MPN\) security logs and convert them into structured log records.

## Before you begin

Roles required:

-   tsom\_assurance\_admin
-   Assigned role for MID Server

For instructions on setting up a MID Server, see [Set up a MID Server role](https://www.servicenow.com/docs/r/servicenow-platform/mid-server/t_SetupMIDServerRole.html).

## About this task

MPN security log collection uses the out-of-box security log data input under Health Log Analytics, configured with values specific to the MPN security log source. The data input is an Elasticsearch collector that queries a security log index and passes each raw log document through a parser. The parser extracts structured fields, including a customer identifier, from the raw message text. For a list of the fields produced, see the [MPN security log fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/nokia-mpn-security-log-fields.md) reference.

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data inputs** and open the out-of-box security log data input.

    This data input is an Elasticsearch collector provided predefined for MPN security logs.

2.  Set **Execute on** to **Specific MID Server** and select the **MID** to use for the connection.

    Use the lookup to select a MID Server that is installed on your instance.

3.  Select the **Service instance** for this data input.

    The service instance is required. It is used to correlate configuration items \(CIs\) and service instances in the CMDB for root cause analysis.

4.  **Note:** Credentials aren't provided predefined.

    On the **Transport** tab, configure the connection to your security log store.

    Configure the following fields:

    -   **Server URL**: The endpoint of your security log store. A sample URL is provided predefined; replace it with the URL for your environment.
    -   **Authentication method**: The authentication mechanism for your store. The out-of-box configuration uses basic authentication.
    -   **Basic auth credentials**: The credentials for your store. Shown when **Authentication method** is set to **Basic authentication**.
5.  On the **Query Settings** tab, provide the following MPN-specific values.

    |Field|Value|
    |-----|-----|
    |**Index**|Index pattern for your security log store, for example `app-security-logging-staging`. Use your staging index pattern in non-production environments, and your production index pattern once you move to production.|
    |**Timestamp field**|`@timestamp`|
    |**Timestamp format**|`yyyy-MM-dd'T'HH:mm:ss.SSS'Z'`|

    **Warning:** Don't modify the **Timestamp field** or **Timestamp format** values. Changing them can break log ingestion.

6.  Attach the MPN security log source type parser to the data input.

    The parser is provided predefined, automatically detects the log source subtype, and extracts structured fields from each raw log document. If a structured `raw_data` field is present, the parser extracts from it directly; otherwise it falls back to regex parsing of the `message` field.

    The parser also maps log severity: `INFO` logs are treated as OK \(normal/informational activity\), `WARN` logs as Minor \(informational alerts\), and `ERROR` logs as Major/Critical \(for example, unauthorized access, denied operations, off-hours sensitive access, or failed logins\).

    All fields except the customer identifier are extracted automatically and require no configuration. The customer identifier is extracted using a configurable pattern in the parser's JavaScript function. To change how the customer identifier is derived, edit this pattern.

    **Note:** Properties longer than 256 characters aren't extracted and aren't indexed as keywords in Elastic.

7.  On the **Advanced** tab, set the collection **Frequency**.

    The frequency controls how often the data input pulls data. The default is every minute; adjust it as needed, for example every 5 or 10 minutes.

8.  Save and test the data input connection, then select **Publish**.

    When you publish the data input, its dependencies, including the streaming source, are created automatically by the Health Log Analytics infrastructure.


## Result

The data input starts streaming security log data from the configured Elasticsearch index and produces structured log records. For example, a raw log entry such as:

```
SECURITY: Wrong password **** customer: "C1234567", site: "<site-id>", user: "<user>", client: "<client-ip>", server: "<server>", request: "POST /auth **** HTTP/1.1", host: "<host>"
```

produces a structured record containing fields such as customer, site, user, client IP, and host, shown concatenated in the log message in the log viewer.

**Parent Topic:**[Configure Telecom Assurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/set-up-fault-management.md)

**Related topics**  


[MPN security log fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/nokia-mpn-security-log-fields.md)

