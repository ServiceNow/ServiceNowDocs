---
title: MID Hermes API extension
description: MID Hermes API is a MID Server extension that enables communication to Hermes via a MID Server.Configure the MID Hermes API extension to enable the MID Hermes Producer API to produce messages to Hermes via a MID Server.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using Stream Connect for Apache Kafka, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# MID Hermes API extension

MID Hermes API is a MID Server extension that enables communication to Hermes via a MID Server.

Send message payloads to a Hermes topic with MID script includes and the [MID Hermes Producer API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/MIDHermesProducerAPI.md). MID script includes push data to Hermes through a scriptable API interface, so Stream Connect isn't required. Activate the ServiceNow MID Hermes API \(com.glide.mid.hermes\_api\) plugin to use this extension.

## Extension context records

Configuration details for the MID Hermes API extension are stored in context records. A context record specifies which MID Server the extension context executes on. After the context record is created, you can also use it to:

-   View the status of the extension context.
-   Start, stop, and restart the extension context.
-   Update parameters.
-   View the allowed Hermes topics and edit or create topics.

The following image shows an example of a completed MID Hermes API Context record.

![Screenshot of a filled in MID Hermes API Context record.](../images/mid-hermes-api-context.png)

## Statistics

You can view statistics for the MID Hermes API extension by navigating to **All** &gt; **MID Server** &gt; **Extensions** &gt; **MID Hermes API Statistics** or going directly to the MID Hermes API Statistics \[sys\_mid\_hermes\_api\_metric\] table.

This table includes the following statistics.

-   Byte count: Number of bytes produced during the collection interval.
-   Collection time: Time the collection interval ended.
-   Collection interval \(seconds\): Duration of the collection interval. The default is 60 seconds.
-   Message count: Number of messages produced during the collection interval.
-   MID Hermes API Extension Context: Name of the extension context record used for producing messages.
-   MID Server: Reference to the MID Server executing the extension context.
-   Topic: Name of the Hermes topic the extension context is producing messages to.

The metrics for this table are collected in-memory per \(extension\_context, topic\) and aggregated continuously during each 60-second interval. Then they're transmitted as a single batch to ServiceNow, resulting in one database record per unique context-topic combination per interval rather than individual records for each message.

This table has a table cleaner that automatically purges old statistics records based on data retention policies, helping to prevent unbounded table growth.

## Access certificates

The mTLS Hermes access certificates contain topic ACLs. When the MID Server generates the CSR, the value in the topics\_acl field from the MID Extension Context table is set as the ACL on the CSR. The REST call to sign the CSR passes the MID Extension Context sys\_id, so the server can verify that the ACL matches the context configuration.

If the ACL in the Hermes access certificate doesn't match the ACL in the MID Extension Context record, the MID Server automatically retries the verification up to three more times. Between each attempt, the MID Server refetches the latest ACL from the instance. If the ACL still doesn’t match after the final attempt, a REST error is returned and logged.

When the MID extension context starts, the topic ACL string it provides is compared to the one that's part of the mTLS Hermes access certificate. If it's different, a new mTLS certificate with the correct ACL is generated.

If the allowed topics change, business rules automatically restart the MID extension context. When an extension is restarting, producing still works with the old configuration until the new configuration is loaded.

Certificates are valid for seven days. When a certificate is created, a five-day timer starts to re-request the access certificate before it expires.

## Configure the MID Hermes API Extension

Configure the MID Hermes API extension to enable the MID Hermes Producer API to produce messages to Hermes via a MID Server.

### Before you begin

-   Role required: kafka\_admin
-   Deploy and start a MID Server.
-   Activate the ServiceNow MID Hermes API \(com.glide.mid.hermes\_api\) plugin.

### Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Extensions** &gt; **MID Hermes API**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_nzz_fyr_c3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the MID Server extension context.

</td></tr><tr><td>

Short description

</td><td>

Description of the MID Server extension context.

</td></tr><tr><td>

Extension

</td><td>

Name of the MID Server extension for this context. This field is automatically set to **MID Hermes API Extension**.

</td></tr><tr><td>

Status

</td><td>

Current status of the extension context. This field is automatically set.

</td></tr><tr><td>

Execute on

</td><td>

Identifies where this extension context is executed. This field is automatically set to **Specific MID Server**.

</td></tr><tr><td>

MID Server

</td><td>

Name of the MID Server to execute this context.**Note:** You can't use the same MID Server to create multiple context records \(no duplicate records\).

</td></tr><tr><td>

Executing on

</td><td>

Name of the MID Server that is executing this context. This field is automatically set.

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  Select the newly created context record from the MID Hermes API Contexts \[ecc\_agent\_ext\_context\_mid\_hermes\_api\] table.

6.  Under Related Links, select **Start**.

    The extension context starts. You should see **Started** in the **Status** field.


### What to do next

Add Hermes topics by selecting **New** on the **Allowed Topics** tab. When you add a new topic, it's created and linked, so it shows up in the **Allowed Topics** tab.

**Note:** After changing the list of allowed topics, the MID Hermes API context record goes into the **Restarting** state. The new list of allowed topics is enforced after the record has returned to the **Started** state.

