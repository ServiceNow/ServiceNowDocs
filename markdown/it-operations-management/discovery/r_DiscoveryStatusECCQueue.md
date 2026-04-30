---
title: The ECC queue for Discovery
description: The External Communication Channel \(ECC\) Queue is a connection point between your ServiceNow instance and other systems that integrate with it, most commonly a MID Server.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-24"
reading_time_minutes: 3
breadcrumb: [Discovery status, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# The ECC queue for Discovery

The External Communication Channel \(ECC\) Queue is a connection point between your ServiceNow instance and other systems that integrate with it, most commonly a MID Server.

## Contents of the ECC Queue

The ECC queue contains records that are created during all stages of discovery. Each record is a message from the instance to system your are targeting for discovery, classified as **output**, or a message from that system to the instance, classified as **input**.

ECC queue records provide you with a connected flow of probe and sensor activity along with the XML payload sent to or from an instance and the assets you're targeting.

## Automatic deletion of ECC queue records

As your IT Asset Discovery runs, the size of the ECC queue can grow to several gigabytes. Most of the “completed tasks” records are unnecessary, but some might be important for issue resolution.

For example, if Discovery is not properly capturing the disk drives on a particular Windows server, you can look in the ECC Queue at the data returned by the Windows - System Information probe. For this reason, you should retain ECC Queue data from Discovery for at least a month.

By default, records in the ECC Queue older than 7 days are deleted automatically. You can set the deletion schedule by updating the ECC queue \(as we will explain in the next section\) and the table rotation schedule. The table rotation names are:

-   **ecc\_queue\_event**
-   **ecc\_queue**

## Accessing the ECC queue

You can access the ECC queue from either of these locations:

-   **Discovery** &gt; **Output and Artifacts** &gt; **ECC Queue**
-   **ECC** &gt; **Queue**

The following image is an example of a record in the ECC queue. This record shows that a ConnectorProbe was instructed to run and has been processed. Note the XML payload it returned as the discovery task collected data. See [The MID Server ECC queue](https://www.servicenow.com/docs/access?context=ecc-queue-mid-server&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for a description of each field.

![An example ECC Queue](../image/ECCQueue.png "An example ECC queue record")

## ECC queue states

Input and output messages keep processing until the discovery is finished or terminated. You can monitor the ECC queue to see records populate during discovery and see the states of each record change.

ECC queue input records are processed by business rules \(BR\), but not all business rules direct these ECC queue inputs to process. As a result, some ECC queue inputs remain in a **ready** state.

The process is as follows:

1.  When new probe instructions are available for the MID Server, the system creates an **output** record with the state of **ready**.
2.  The MID Server then starts processing the probe instructions and the state changes to **processing** before it finally changes to **processed**.
3.  When a result returns to the MID Server and is ready to be sent to the instance, the system creates an **input** record with the state of **ready**.
4.  While the system processes the payload, the state changes to **processing** before it finally changes to **processed**.

    If any errors are encountered, the state changes to **error**. You can review errors as a starting point for troubleshooting a failed discovery.


## Debug processing of ECC queue records

To use a script debugger, process the payload on the same session as the debugger. Review the business rule which processes the particular ECC queue record and the actual code which processes the payload.

## Properties and parameters that affect the ECC queue

These properties are available to control aspects of the ECC queue:

<table id="table_khy_354_lz"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Save ECC queue attachments

</td><td>

The normal behavior for Discovery sensors is to delete attachments to ECC queue entries on successful sensor processing. Enabling this property overrides this behavior, and forces attachments to be preserved. This is typically done for debugging purposes.To enable this property, navigate to **Discovery Definition** &gt; **Properties**.

</td></tr></tbody>
</table>**Parent Topic:**[Discovery status](../concept/c_DiscoveryStatus.md)

**Related topics**  


[Manage ECC Queue content for a MID Server](https://www.servicenow.com/docs/access?context=ecc-queue-mid-server&version=zurich&pubname=zurich-servicenow-platform&section=manage-ecc-queue-content&ft:locale=en-US)

