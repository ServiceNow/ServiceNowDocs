---
title: IT Issues pre-built topics for ITSM Virtual Agent
description: IT Issues topic conversations are designed to automate common IT-related issues, such as email setup, VPN connectivity, and conference room problems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/itsm-virtual-agent/itsm-va-it-issues-generic.html
release: australia
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using ITSM Virtual Agent pre-built topics, ITSM Virtual Agent, IT Service Management]
---

# IT Issues pre-built topics for ITSM Virtual Agent

IT Issues topic conversations are designed to automate common IT-related issues, such as email setup, VPN connectivity, and conference room problems.

## Collaboration Applications

Users can use Virtual Agent to troubleshoot common issues with collaboration software, such as Cisco Webex, Zoom, and Microsoft Teams. This topic uses topic blocks that can be customized for your environment. If the user isn't satisfied with the static help content for the issue they're facing, they can perform an AI search or Contextual search. The type of search is dictated by the system property **sn\_itsm\_va.fallback\_search\_option**.​

This topic uses the following [topic blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/itsm-virtual-agent/itsm-va-topic-blocks.md):

-   Contextual Search
-   Create Incident
-   Troubleshoot Cisco Webex
-   Troubleshoot Microsoft Teams
-   Troubleshoot Zoom

\[Omitted image "TroubleshootMSTeams.jpg"\] Alt text: Collaboration Application topic.

## Email Issues

Users can request help with email problems, such as issues sending and receiving email or problems with the email client.

\[Omitted image "EmailIssues.png"\] Alt text: Email Issues topic.

## Email Setup

Users can request help with email access or setting up an email account accessible by computer or phone. Users can also request help with configuring email or setting up web mail.

\[Omitted image "EmailSetup.png"\] Alt text: Email Setup topic.

## Guest WiFi Access

Guests to your company can obtain WiFi access.

\[Omitted image "GuestWiFiAccess.png"\] Alt text: Guest WiFi Access topic.

## Hardware Issues

Users can troubleshoot specific hardware issues.

This topic uses the following [topic blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/itsm-virtual-agent/itsm-va-topic-blocks.md):

-   Contextual Search
-   Create Incident

## Local Admin Access

Users can request and gain admin rights and permission to install or access software and other admin-related items within your system.

Virtual Agent grants admin access and removes the access for all users on the device after the designated time period \(except users listed in DEFAULT\_ADMIN\_USERS\).

When the user requests help with admin access, Virtual Agent asks the user to select the device they would like admin privileges for.

Requirements:

-   [Agent Client Collector spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/acc-spoke.md) \(com.sn.acc.spoke\)
-   Applies to macOS users only

    If the user selects another operating system, Virtual Agent provides relevant KB articles.


\[Omitted image "LocalAdminAccess.png"\] Alt text: Local Admin Access topic.

To set up and use the Local Admin Access topic, refer to [Set up the Local Admin Access topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/itsm-virtual-agent/setup-admin-access.md).

## Meeting Room Issues

Users can request help with meeting room issues, such as conferencing problems, sound issues, display, connectivity, sharing, and more.

This topic uses the following [topic blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/itsm-virtual-agent/itsm-va-topic-blocks.md):

-   Contextual Search
-   Create Incident

\[Omitted image "MeetingRoomIssues.png"\] Alt text: Meeting Room Issues topic.

## Printer Issues

Users can request help with issues associated with a printer, such as no ink, printer not working, or connectivity problems. This topic can be used with [Issue Auto Resolution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/itsm-virtual-agent/itsm-va-auto-resolution.md).

This topic uses the following [topic blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/itsm-virtual-agent/itsm-va-topic-blocks.md):

-   Contextual Search
-   Create Incident

\[Omitted image "PrinterIssues.png"\] Alt text: Printer Issues topic.

## Repository Access

Users can request and gain access to a data repository manually, or choose from preloaded available repositories.

This topic uses the Create Incident [topic block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/itsm-virtual-agent/itsm-va-topic-blocks.md).

\[Omitted image "RepositoryAccess.png"\] Alt text: Repository Access topic.

## RSA Token

Users can request an RSA token or report a problem with an RSA token. Users can also request help with the setup of an RSA token.

This topic uses the following [topic blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/itsm-virtual-agent/itsm-va-topic-blocks.md):

-   Contextual Search
-   Create Incident

\[Omitted image "RSAToken.png"\] Alt text: RSA Token topic.

## Troubleshoot Slow Computer

Users can request help associated with a slow computer, such as low RAM.

This topic uses the following [topic blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/itsm-virtual-agent/itsm-va-topic-blocks.md):

-   Contextual Search
-   Create Incident

\[Omitted image "TroubleshootSlowComputer.png"\] Alt text: Troubleshoot Slow Computer topic.

## VPN Connectivity

Users can request help with connecting to VPN or setting up VPN to access business systems from remote locations.

This topic uses the following [topic blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/itsm-virtual-agent/itsm-va-topic-blocks.md):

-   Contextual Search
-   Create Incident

\[Omitted image "VPNConnectivity.png"\] Alt text: VPN Connectivity topic.

**Parent Topic:**[Using ITSM Virtual Agent pre-built topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/itsm-virtual-agent/using-itsm-va.md)

