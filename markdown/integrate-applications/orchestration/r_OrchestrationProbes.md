---
title: Probes used by Orchestration
description: Certain probes, controlled by MID Servers, perform Orchestration tasks on remote computers, such as restarting a server or creating virtual machines from templates.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Deprecated Orchestration activities, Activate Orchestration, Classic Orchestration, Workflow Data Fabric]
---

# Probes used by Orchestration

Certain probes, controlled by MID Servers, perform Orchestration tasks on remote computers, such as restarting a server or creating virtual machines from templates.

## How Orchestration probes work

When a Workflow executes an Orchestration activity, that activity launches a probe, which writes an output record to the ECC Queue. The MID Server selected for the activity checks the ECC Queue for assignments, and then executes the appropriate probe to do the work on the target machine. The information about the activity \(machine restarted, files copied, etc.\) that is returned from the target machine by the probe is written to the ECC Queue as an input record. This information is then sent from the ECC Queue to a sensor that is built into the Workflow activity. The Workflow is updated, and the next activity is executed.

**Note:** The probe parameters are set by the activities that launch the probe.

![How Orchestration uses probes](../image/RunbookProbesDiagram.png "How Orchestration uses probes")

## Probe List

The base system includes the following Orchestration probes \(**Orchestration** &gt; **Definition** &gt; **Probes**\).

<table id="table_ljp_vzb_sp"><thead><tr><th>

Probe Name

</th><th>

ECC Queue Topic

</th><th>

ECC Queue Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Command

</td><td>

Command

</td><td>

 

</td><td>

A probe that runs a local command on the MID server.

</td></tr><tr><td>

DNS Name Resolver

</td><td>

DNSNameResolver

</td><td>

 

</td><td>

A probe that resolves a fully qualified domain name \(FQDN\) into an IP address. The probe executes MID Server queries in parallel. It utilizes DNS lookup by the MID Server host OS to make use of the OS maintained DNS cache. It also leverages the hosts file on the OS.

</td></tr><tr><td>

SCPCommand

</td><td>

SCPCommand

</td><td>

 

</td><td>

A probe that copies files securely from one machine to another. The copy function is performed using the MID Server as a tunnel.

</td></tr><tr><td>

Shazzam

</td><td>

Shazzam

</td><td>

 

</td><td>

A probe that identifies active devices.

</td></tr><tr><td>

SNMPProbe

</td><td>

SNMP

</td><td>

SNMP Query

</td><td>

This is a generic SNMP probe.

</td></tr><tr><td>

SOAPProbe

</td><td>

SOAPProbe

</td><td>

 

</td><td>

A probe that sends a SOAP request to target machine.

</td></tr><tr><td>

SSHCommand

</td><td>

SSHCommand

</td><td>

 

</td><td>

A probe that executes shell scripts from a command line after logging in to a target machine via SSH.

</td></tr><tr><td>

SSHCommandLong

</td><td>

SSHCommandLong

</td><td>

 

</td><td>

A probe that executes long running shell scripts from a command line after logging in to a target machine via SSH.

</td></tr><tr><td>

VMWare

</td><td>

VMWareProbe

</td><td>

 

</td><td>

A generic VMware probe that executes the MID Server script include in the ECC queue name that is set by a VMware Orchestration activity. This probe can run any MID Server script include.

</td></tr><tr><td>

Windows - PowerShell

</td><td>

PowerShell

</td><td>

Windows - PowerShell

</td><td>

A probe that runs a Windows PowerShell script on the MID Server. The PowerShell script is provided as the value of a parameter with name ending in **.ps1**. Two variables are available to the script: -   *$computer*: The computer pointed to as the source for this probe
-   *$cred*: A PowerShell credential, using a user name and password from the Credentials table, that logs into *$computer* successfully.

</td></tr></tbody>
</table>**Parent Topic:**[Deprecated Orchestration activities](../../../administer/orchestration-activities/reference/r_OrchestrationBasicActivities.md)

