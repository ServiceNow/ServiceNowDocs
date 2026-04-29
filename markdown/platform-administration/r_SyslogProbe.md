---
title: Syslog probe
description: The ServiceNow Syslog probe uses the MID Server to deliver log messages from a ServiceNow instance to another machine, such as a dedicated log server, using the syslog protocol over an IP network.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Supported integration interfaces, Integration options, Integration with third-party applications and data sources, Integrations, Configure core features, Administer the ServiceNow AI Platform]
---

# Syslog probe

The ServiceNow Syslog probe uses the MID Server to deliver log messages from a ServiceNow instance to another machine, such as a dedicated log server, using the syslog protocol over an IP network.

## How the Syslog probe works

The syslog probe is launched by a ServiceNow [Script includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=australia&pubname=australia-api-reference&ft:locale=en-US) \(called Syslog\) that can be invoked from a [Business rules](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=australia&pubname=australia-api-reference&ft:locale=en-US), event, or Orchestration activity and is launched by a MID Server. A syslog server or any server that can receive messages using the syslog protocol must be installed on the recipient \(target\) machine. Typically, a dedicated log server in the network is configured to receive all internal syslog messages. Some products that accept syslog messages are:

-   ArcSight
-   Splunk
-   LogLogic
-   syslog-ng

## Example

The Acme Corporation wants to send a log message from their ServiceNow instance to an ArcSight syslog server inside their corporate firewall each time a user login fails. The system administrator uses the login.failed event to trigger a business rule that invokes the Syslog Script Include each time a login fails. Acme's MID Server checks the ECC Queue for work and picks up the syslog probe, which contains the log entry. The MID Server then sends the log message to the ArcSight server, which gathers log messages from all the machine in the internal network.

![Syslog probe diagram](../image/SyslogProbeDiagram.png "Syslog probe diagram")

## Code sample

The following code sample, included in an event or a business rule, directly calls the Syslog Script Include and sends a syslog message to a designated syslog server:

```
var sl = new Syslog('FQDN of your syslog server', 'mid.server.Eclipse', 16);
sl.log('This is a sample log message', 6);
```

This code does the following:

-   Sends the log message to facility **16**
-   Sets the priority to **6** \(informational\)
-   Sends the message to your syslog server
-   Launches the probe via the MID Server named "Eclipse"

**Parent Topic:**[Supported integration interfaces](r_SupportedIntegrationInterfaces.md)

