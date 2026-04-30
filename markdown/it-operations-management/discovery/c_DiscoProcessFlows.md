---
title: Horizontal discovery process flow with probes and sensors
description: The horizontal discovery process passes through the four phases of discovery using probes, which gather information on the target machine, and then sensors, which help Discovery determine what to do with that information.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Horizontal discovery process flow with probes and sensors

The horizontal discovery process passes through the four phases of discovery using probes, which gather information on the target machine, and then sensors, which help Discovery determine what to do with that information.

## Kicking off Discovery

A user triggers horizontal discovery by configuring a discovery schedule or by launching an on-demand discovery with Discover now or Quick Discovery. The schedule specifies one or more IP addresses or range of IP addresses.

## Scanning phase

1.  Discovery first takes the Shazzam probe \(and then [port probes](../reference/r_PortProbes.md)\) and places it in a request in the External Communication Channel \(ECC\) queue.
2.  The MID Server checks the ECC queue, retrieves the discovery request, and runs the probes against the host and discovers open ports.
3.  The port probes scan common ports using several protocols, such as WMI, HTTP, SSH, and SNMP.
4.  If one or more ports respond, the Shazzam probe sends information about the port back to the ECC queue through the MID Server.
5.  Discovery checks the ECC queue to find out which ports responded, which identifies the type of machine. For example, if Shazzam detects that the machine is listening on port 22, Discovery treats the machine as a UNIX or Linux machine.

## Classification phase

1.  The Discovery application determines which classification probe to send to the newly discovered device by using information in the record of the port probe that successfully responded.
2.  Discovery puts the classification probe into the ECC queue.
3.  The MID Server checks the ECC queue, retrieves the discovery request, and runs the classification probe.
4.  The classification probe retrieves additional information, such as which version of the operating system is running on a machine. This information determines the class of the CI that Discovery found. There is only one classification probe per discovered device.
5.  The classification probe sends information back to the instance ECC queue through the MID Server.

## The Identification phase

1.  Discovery determines which classifier to use based on the class of the CI and the criteria specified in all CI classifier records. The classifier specifies which probes to use for the next two phases.
2.  Discovery puts the identification trigger probe for the CI classifier into the ECC queue. For example, a UNIX machine running HP-UX would require the HP-UX classifier, which specifies that the Multi Probe-HP-UX Identity identification trigger probe. These probes use identification rules to determine whether or not to insert or update a CI in the CMDB.

    **Note:** The trigger probe could also be the Horizontal Pattern probe, which tells Discovery to follow the operations in the specified pattern, rather than sending out additional probes. The operations in the pattern cover both the identification and exploration phases. Discovery knows which identification rules to use based on the CI type, and Discovery makes inserts or updates to the CMDB based on these rules. Probes and sensors are not used.

3.  The MID Server checks the ECC queue, retrieves the discovery request, and runs the identification trigger probe.
4.  The identification probe accumulates identification data for each device and sends that data back to the instance via the MID Server.
5.  Discovery uses sensors for the identifier probe to process the information.
6.  Discovery performs the analysis on the CMDB using [CI identifiers](c_DiscoveryIdentifiers.md). Discovery can update existing CIs in the CMDB or create new ones.

## The Exploration phase

1.  Discovery looks at the Triggers Probes related list in the classifier to find exploration probes to run.
2.  Discovery puts the exploration trigger probe into the ECC queue.
3.  The MID Server checks the ECC queue, retrieves the discovery request, and runs the exploration trigger probes.
4.  The probes send data back to the instance via the MID Server and sensors make updates to the CMDB, just as in the identification phase.

**Parent Topic:**[Exploring Discovery](c_GetStartedWithDiscovery.md)

**Related topics**  


[Horizontal discovery process flow with patterns](disco-process-flow-patterns.md)

[Discovery Admin Workspace](discovery-admin-workspace.md)

[Patterns and horizontal discovery](c-UsingPatternsForHorizontalDiscovery.md#)

