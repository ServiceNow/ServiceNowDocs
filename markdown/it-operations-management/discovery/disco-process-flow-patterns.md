---
title: Horizontal discovery process flow with patterns
description: Horizontal discovery with patterns has four phases, just as horizontal discovery with probes does. However, for the last two phases, Discovery triggers operations from a pattern, rather than additional sets of probes.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Horizontal discovery process flow with patterns

Horizontal discovery with patterns has four phases, just as horizontal discovery with probes does. However, for the last two phases, Discovery triggers operations from a pattern, rather than additional sets of probes.

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

## The Identification and Exploration phases

Patterns unify the Identification and Exploration phases of discovery.

1.  Discovery determines which classifier to use based on the class of the CI and the criteria specified in all CI classifier records. The classifier specifies the [Horizontal Pattern probe](../reference/r-HorizontalPatternProbe.md), which in turn specifies which pattern to launch. The Horizontal pattern probe also contains a sensor which does the actual work of updating the CMDB.

    **Note:** Patterns need applicative credentials to find applications running on host machines. Make sure you have applicative credentials configured along with the credentials required to access the host machine itself.

2.  The operations in the pattern specify the actions that Discovery needs to take for both the identification and exploration phases. Discovery knows which [identification rules](https://www.servicenow.com/docs/access?context=c_IdentificationRules&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) to use based on the CI type in the pattern, and Discovery makes inserts or updates to the CMDB based on these rules. Only the Horizontal Discovery Sensor is used. Other probes and sensors are not used.

**Parent Topic:**[Exploring Discovery](c_GetStartedWithDiscovery.md)

**Related topics**  


[Horizontal discovery process flow with probes and sensors](c_DiscoProcessFlows.md)

