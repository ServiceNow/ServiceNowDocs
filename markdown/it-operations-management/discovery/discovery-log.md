---
title: Discovery log details
description: Discovery logs contain information on the horizontal discovery process based on probes and patterns.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Discovery reference, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery log details

Discovery logs contain information on the horizontal discovery process based on probes and patterns.

## Discovery log related list

The Discovery Log related list contains information about the horizontal discovery based on probes.

The Discovery Log provides the following information:

<table id="table_itd_wfl_rx"><thead><tr><th>

Field

</th><th>

Input value

</th></tr></thead><tbody><tr><td>

Created

</td><td>

Timestamp of the Discovery activity. Each timestamp defines the approximate time of the activity. Several Discovery events may occur in random order within a second.

</td></tr><tr><td>

Level

</td><td>

Classifies the activity into one of the following levels for general sorting:-   Error
-   Information
-   Warning

</td></tr><tr><td>

Short Message

</td><td>

Informative message detailing the outcome of the activity or the Discovery progress. Look here for the result of a classify probe or for authentication failure.

</td></tr><tr><td>

ECC queue input

</td><td>

The related input record from the ECC queue for this discovery. You can also view these records from the **ECC Queue** related list.

</td></tr><tr><td>

CI

</td><td>

Names a device for which a matching CI was found in the CMDB. Select the link to view the CI record for the device.

</td></tr><tr><td>

Source

</td><td>

Names the particular activity, such as the Shazzam probe or a UNIX classify probe.

</td></tr><tr><td>

Device

</td><td>

Lists the IP address of the CI discovered. All devices identified by IP address appear in the log, even if they refused all invitations to communicate. Any port activity from a device places it into the log, even if all subsequent efforts to identify it fail. Select the IP address of the device to view the events associated with discovering that device.

</td></tr></tbody>
</table>## Horizontal Discovery Log

The Horizontal Discovery Log window contains information on pattern-based horizontal discovery.

|Discovery Log Item|Description|
|------------------|-----------|
|Pre Pattern Execution|The actions that were run before the pattern was launched.|
|Selecting Pattern for Execution|The pattern that was run for discovery.|
|\{Identification Section name\}|Displays the results of the operations in the pattern. Expand the name to see each operation.|
|Pre Payload Processing Scripts|The results of scripts that were run before the payload was received.|
|Payload Processing|Details about the payload and how it was processed. Find errors that might have been encountered during various activities, such as the running of identification rules, updates to the CMDB, and so on.|
|Post Payload Processing Scripts|The results of scripts that were run after the payload was received.|

**Parent Topic:**[Discovery reference](discovery-references.md)

