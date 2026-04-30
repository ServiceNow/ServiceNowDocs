---
title: Troubleshooting Workplace Calendar Synchronization
description: This section helps administrators troubleshoot connection setup issues in Workplace Calendar Synchronization. Calendar sync integrates ServiceNow Workplace with external calendar providers — Microsoft Exchange Online and Google Calendar — to synchronize room and resource availability.
locale: en-US
release: zurich
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: concept
last_updated: "2026-03-03"
reading_time_minutes: 3
breadcrumb: [Reference, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Troubleshooting Workplace Calendar Synchronization

This section helps administrators troubleshoot connection setup issues in Workplace Calendar Synchronization. Calendar sync integrates ServiceNow Workplace with external calendar providers — Microsoft Exchange Online and Google Calendar — to synchronize room and resource availability.

Calendar sync establishes two types of connections that must both be correctly configured for the integration to function:

-   **System-to-System connection**

    A backend integration that syncs calendar data automatically using service account credentials.

-   **User-level connection**

    A per-user connection established when a user interacts with the application, required only in Personal mode.


**Note:** The troubleshooting steps in this guide apply to both Microsoft Exchange Online and Google Calendar integrations unless otherwise specified.

## System-to-System Connection

The system-to-system connection handles backend synchronization between ServiceNow and your calendar provider. Follow the steps below to diagnose and resolve configuration issues.

## Identify the Connection Alias

The connection alias determines which credentials and OAuth configuration are used for the integration. ServiceNow resolves the alias in the following order.

1.  Navigate to the Calendar Provider record for the relevant provider \(Microsoft or Google\).
2.  Check whether an Override Alias is configured on the provider record.
3.  If an Override Alias is mapped to a Connection &amp; Credential Alias, that alias is used for the integration.
4.  If no Override Alias is mapped, ServiceNow uses the default alias for the processor — for example, the default Microsoft Exchange Online alias for the `ms_graph` processor

## Validate the Connection &amp; Credential Alias

Confirm that the alias is correctly configured before checking credentials.

-   Verify that the alias is appropriate for the selected Integration Mode: Normal, Strict, or Personal.
-   Confirm all of the following are configured and active on the alias:
    -   **Connection**
    -   **Credential**
    -   **OAuth Entity Profile**
    -   **Scopes**
    -   **Application Registry**

**Note:** An incomplete alias, for example, a missing OAuth Entity Profile or Application Registry will cause token generation and API calls to fail even if the credential itself is valid.

## Verify Credential Settings

Navigate to the Credential record associated with the alias and confirm the following settings:

-   **Integration Type** must be set to **System**.
-   **Grant Type** must match the integration mode and provider as shown in the table below.

|Provider|Integration Mode|Required Grant Type|
|--------|----------------|-------------------|
|Microsoft Exchange Online|Normal|Client Credential|
|Microsoft Exchange Online|Strict or Personal|Authorization Code|
|Google Calendar|All modes \(including Normal\)|Authorization Code|

**Important:** Using a mismatched grant type is a common cause of authentication failures. For example, configuring Client Credential on an Exchange Online integration that is running in Strict mode will result in authorization errors.

## Obtain an OAuth Token \(Authorization Code Only\)

This step applies only when the grant type is Authorization Code. If the grant type is Client Credential, skip this step.

1.  Open the Credential record associated with the alias.
2.  Select **Get OAuth Token**.
3.  When prompted, authenticate using the credentials of a user who has read or write access to the room calendars in the external system.
4.  Confirm that the token is generated successfully before proceeding.

**Warning:** Using incorrect credentials when clicking **Get OAuth Token** will result in errors such as `"resource not found"`,`"subscription failed"`,or `"access denied"`. Ensure the authenticating user has the required permissions before generating the token.

## Configure Delegated User Email

The **Delegated User Email** field on the Calendar Provider record is required only in Strict or Personal integration modes.

-   If the integration mode is Strict or Personal: populate the **Delegated User Email** field on the Provider record with the email address of the delegated service account.
-   If the integration mode is Normal: leave this field empty. It is not used in Normal mode.

**Note:** A missing or incorrect Delegated User Email in Strict or Personal mode will cause calendar event lookups and room availability queries to fail.

## User-Level Connection

The user-level connection is established per user when they interact with the Workplace application. The configuration required depends on the integration mode.

-   **Normal and Strict Modes**

    No additional user-level configuration is required. System-to-system credentials handle all calendar operations.

-   **Personal Mode**

    In Personal mode, each user authenticates individually with the calendar provider. An out-of-the-box \(OOB\) alias is provided for each processor type \(Exchange Online and Google Calendar\).

    -   Locate the OOB alias for the relevant processor \(Exchange or Google\).
    -   Confirm that the alias is correctly configured for the processor type.
    -   Verify that the alias has all of the following configured and active:
        -   **Connection**
        -   **Credential**
        -   **OAuth Entity Profile**
        -   **Scopes**
        -   **Application Registry**
    -   Confirm that the **Grant Type** on the Credential record is set to Authorization Code.
    -   Confirm that the **Integration Type** on the Credential record is set to Personal.

**Important:** Do not select **Get OAuth Token** on the Personal credential record. In Personal mode, each user’s OAuth token is generated automatically via a pop-up or in-application prompt the first time they interact with the calendar feature. Manually generating the token on this credential will interfere with per-user token management.

