---
title: Integrate SIR with third-party communication channels
description: The SIR Conference Call integration with third-party communication channels such as Microsoft Teams, Zoom, and Cisco Webex, enables you to manage and initiate a call directly from a security incident.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Incident Response conference call integration, Configure, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Integrate SIR with third-party communication channels

The SIR Conference Call integration with third-party communication channels such as Microsoft Teams, Zoom, and Cisco Webex, enables you to manage and initiate a call directly from a security incident.

## Key features

-   Start and end conference calls directly from any security incident.
-   Add or remove participants in a conference call.
-   Track and report meeting details such as meeting duration and attendees for further analysis.

## Prerequisites

Verify you’ve installed the following Integration Hub plugins on your ServiceNow instance.

-   Notify plugin \(com.snc.notify\). For more information, see Configuring Notify
-   Notify UI Components for Configurable Workspaces
-   For integrating Microsoft Teams as a communication channel:
    -   Microsoft Teams Communications spoke plugin \(sn\_msteams\_com\_spk\).
    -   Azure Active Directory User Mapping plugin \(sn\_now\_azure\).
-   For integrating Zoom as a communication channel:
    -   Zoom Spoke \(sn\_zoom\_spoke\)
    -   Notify Zoom \(sn\_notify\_zoom\)
-   For integrating Cisco Webex as a communication channel:
    -   Notify Cisco Webex Connector \(sn\_notify\_webex\)
    -   Cisco Webex Teams Spoke \(sn\_cisco\_teams\_spk\)

For more information, see Request Integration Hub.

## Configuration

Perform the following configuration for the communication channels you want use:

-   To configure the Conference Call Cisco Webex integration using the Notify communication channel, see Configure Notify Cisco Webex Connector.

-   To configure the Conference Call Zoom integration using the Notify communication channel, see Configure Notify Zoom connector in Notify.

-   To configure the Conference Call Microsoft Teams integration using the pre-configured app, see Integrate Notify connector pre-published app with Microsoft Teams.

-   To configure the Conference Call Microsoft Teams integration using the self-configured app, see Integrating Notify connector self-configured app with Microsoft Teams.


**Parent Topic:**[Security Incident Response conference call integration](../concept/sir-conf-call-capability.md)

