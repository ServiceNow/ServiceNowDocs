---
title: Badge Reader Integration for Walk-up Experience
description: Improve Walk-up Experience user satisfaction by using the Badge Reader Integration application at your on-site walk-up queue locations. Walk-up Experience users can scan an employee badge to check in to a queue, rather than entering credentials.
locale: en-US
release: xanadu
product: Walk-Up Experience
classification: walk-up-experience
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure, Walk-up Experience, IT Service Management]
---

# Badge Reader Integration for Walk-up Experience

Improve Walk-up Experience user satisfaction by using the Badge Reader Integration application at your on-site walk-up queue locations. Walk-up Experience users can scan an employee badge to check in to a queue, rather than entering credentials.

## Badge Reader Integration for Walk-up Experience on-site queue locations

Badge Reader Integration is a pre-built, domain-separated, base-system application. The application enables your Walk-up Experience users to simply scan an employee badge to join an on-site walk-up queue. Scanning a badge eliminates the need for users to look up a name or email to join a queue. Administrators can easily configure the badge scanning integration for use with Walk-up Experience.

By providing an enhanced, easier, and faster Walk-up Experience check-in process, the use of on-site walk-up location queues can increase and overall user satisfaction can improve. Users receive an on-screen confirmation and an audio alert after a successful check-in to a walk-up queue.

The Badge scanning integration requires activation of the Badge Reader Integration plugin \(com.snc.badge\_reader\). The plugin enables applications, such as Walk-up Experience, to integrate with badge reader hardware. Badge Reader Integration administration requires the Badge Admin role \(sn\_badge.badge\_admin\).

**Note:** Badge Reader Integration is not an authentication mechanism.

## Walk-up Experience Badge Reader Integration components

The badge reader hardware and integration client are physically located at a walk-up queue location. The Badge Reader Integration application provides a generic, reusable REST API used by the badge integration clients. Walk-up Experience uses the Badge Reader Integration application as a soft dependency.

Walk-up Experience implementers install the badge reader hardware on a new computer at each on-site walk-up queue location. The hardware replaces any existing tablets used for on-site check-in.

The following are important associated components.

|Component|Description|
|---------|-----------|
|Badge number|Employee badge number.|
|Facility code|Unique facility or site code encoded into each card that identifies the organization.|
|Human Interface Device \(HID\)|Protocol for interfacing with user interface devices via USB.|
|Physical Access Control Services \(PACS\)|Method used to protect the security of a physical environment by setting authorization and authentication rules.|
|Badge reader client|Client for the badge reader. Acceptable platforms include macOS and Linux.|
|Badge reader plugin|The Badge Reader Integration plugin \(com.snc.badge\_reader\) is at no additional cost.|

## Badge Reader Integration modules

Badge admins can access several application modules.

<table id="table_olh_thh_yjb"><thead><tr><th>

Module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Downloads

</td><td>

Badge Reader Integration client for download to your system.

</td></tr><tr><td>

Badge Readers

</td><td>

Configuration module for defining and activating your badge reader devices.

</td></tr><tr><td>

Badge Event Handlers

</td><td>

Configuration module for defining what action to take when a badge is scanned by a badge reader device.

 The script entered is the code executed when a badge is scanned.

 These records are typically delivered as part of the application-specific badge reader integrations.

</td></tr><tr><td>

User Badges

</td><td>

Configuration module for associating users with user badges.

 Configuration requires associating a sys\_user with a unique badge number and facility code.

</td></tr><tr><td>

Badge Scan Logs

</td><td>

View-only module to monitor badge reader error events.

</td></tr><tr><td>

User Badge Configuration

</td><td>

Configuration module for defining the table from where the user ID and badge ID mapping information is retrieved.

</td></tr></tbody>
</table>## Badge Reader Integration security

The Badge Reader Integration application is not an authentication mechanism. It provides a quicker, more convenient way for users to check into a walk-up queue. It is meant for use within the existing security perimeter at the facility. The application does not integrate with existing access control software at the facility.

## Badge Scanner Integration scan logs

You can view the Badge Scanner Integration scan logs and fix the errors to connect to the badge reader. For more information, see [View Badge Scanner Integration scan logs](../task/view-badge-read-integ-scan-logs.md).

-   **[Activate Badge Reader Integration](../task/activate-badge-reader-integration.md)**  
You can activate the Badge Reader Integration plugin \(com.snc.badge\_reader\) if you have the Badge sn\_badge.badge\_admin role.
-   **[Walk-up Experience Badge Reader Integration setup and configuration](walkup-badge-read-integ-config.md)**  
Badge Reader Integration set up and configuration enables your on-site Walk-up Experience users to scan a badge to quickly check into the queue.

**Parent Topic:**[Configuring Walk-up Experience](walkup-experience-configuration.md)

