---
title: SCPRelay probe
description: The SCP Relay Probe copies a single file or the contents of a directory from one host to another, using the MID Server as a relay.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [List of Discovery probes, Discovery probes and sensors, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# SCPRelay probe

The SCP Relay Probe copies a single file or the contents of a directory from one host to another, using the MID Server as a relay.

The SCP Relay probe uses the same parameters as SSHCommand. The commands may be sent in or out of the context of a terminal \(tty\), and with or without sudo \(for those commands, such as lsof, that require being executed in the context of root to cough up the information we need\). When commands are sent in the context of a terminal, the path is automatically widened to include a set of default paths \(and this can be further widened with the path\_override parameter\). If the target machine is the local machine, SSH is not used; instead, a local shell is run to execute the command.

For instructions on configuring probe parameters, see [Set probe parameters](../task/t_SetProbeParameters.md).

The following parameters may be passed to the SCP Relay probe:

<table id="table_mw2_yqr_np"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Default Value

</th></tr></thead><tbody><tr><td>

debug

</td><td>

Enables debug logging.

</td><td>

false

</td></tr><tr><td>

debug\_ssh

</td><td>

Enables J2SSH debug logging **agent.log** **Note:** This log file can grow quickly and should be disabled when not needed.

</td><td>

false

</td></tr><tr><td>

timeout

</td><td>

Sets the socket connection timeout, in ms.

</td><td>

60000

</td></tr><tr><td>

path\_override

</td><td>

Overrides the default paths set before executing a command.

</td><td>

none

</td></tr><tr><td>

keyboard\_interactive

</td><td>

If true, forces the use of keyboard\_interactive SSH login mode.

</td><td>

false

</td></tr><tr><td>

must\_sudo

</td><td>

If true, forces the command to be executed through sudo.

</td><td>

false

</td></tr><tr><td>

run\_in\_terminal

</td><td>

If false, disables SSH commands from running in an SSH terminal \(this will break many commands\).

</td><td>

true

</td></tr><tr><td>

long\_runner

</td><td>

If present, indicates a long-running SSH command.

</td><td>

false

</td></tr><tr><td>

set\_path

</td><td>

If false, disables setting the path environment variable before running the command.

</td><td>

true

</td></tr><tr><td>

rm\_override

</td><td>

If present, overrides the default rm command \("/sbin/rm -f"\) with the provided value.

</td><td>

none

</td></tr><tr><td>

source

</td><td>

Source host or IP to copy from.

</td><td>

required

</td></tr><tr><td>

source\_port

</td><td>

SSH port on the source \(defaults to 22\).

</td><td>

required

</td></tr><tr><td>

from\_file

</td><td>

Name of the file to copy from the source.

</td><td>

required

</td></tr><tr><td>

target

</td><td>

Target host or IP to copy to.

</td><td>

required

</td></tr><tr><td>

target\_port

</td><td>

SSH port on the target \(defaults to 22\).

</td><td>

required

</td></tr><tr><td>

to\_file

</td><td>

Name of the file to copy to the target.

</td><td>

required

</td></tr></tbody>
</table>**Parent Topic:**[List of Discovery probes](r_ListOfDiscoveryProbes.md)

