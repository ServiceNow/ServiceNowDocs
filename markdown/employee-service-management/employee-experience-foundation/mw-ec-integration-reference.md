---
title: Moveworks for Employee Center reference
description: The reference topics for the application provide additional information about the Moveworks for Employee Center settings, observations, and troubleshooting.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Moveworks for Employee Center, Admin configurations, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Moveworks for Employee Center reference

The reference topics for the application provide additional information about the Moveworks for Employee Center settings, observations, and troubleshooting.

## Certificate validation fails

When certificate validation returns errors during the setup process, verify the following configuration:

-   The correct keystore password is entered \(case-sensitive\).
-   JKS file isn’t corrupted, if necessary, request a fresh file, see [Upload Java KeyStore certificate](../task/mw-upload-jks-cert.md).
-   Password is entered in both certificate record and JWT provider settings.
-   Contact support if issues persist after verification.

## Moveworks chat isn’t visible

When the Moveworks chat assistant isn't visible on Employee Center or appears non-functional, you can check the following.

-   Confirm that the Moveworks plugin is installed and enabled from the ServiceNow Store.
-   Navigate to **System Applications** &gt; **Applications** and confirm the status column displays **Active** for the plugin.
-   Verify that the JKS is valid and JWT keys are configured with the correct password.
-   Check that the Moveworks website setup page is saved with a valid bot ID as explained in [Configure bot ID and AI assistant](../task/mw-setup-botid.md).
-   When all the settings look correct, validate their portal-side configuration and ingestion status.

## Enable or disable virtual agent on employee center

The Moveworks for Employee Center chat replaces the classic virtual agent. However, you can initiate and maintain an agent chat of your choice in the following way.

1.  Navigate to **All** &gt; **Service Portal** &gt; **Agent Chat**
2.  Update the **ESC Chat** value to **True** on the Service Portal Agent Chat Configurations `sp_agent_chat_config` table.

## Chat responses aren't relevant

Verify the following configuration:

-   Ensure content ingestion is complete in Moveworks platform.
-   Verify knowledge articles are published.
-   Verify knowledge articles aren't restricted by ACLs.
-   Check that requested services are available in your service catalog.

**Note:** Moveworks for Employee Center is available on both Employee Center and Employee Center Pro.

**Related topics**  


[Getting started with Moveworks for Employee Center](../concept/moveworks-ec-getting-started.md)

[Install Moveworks for Employee Center app from store](../task/mw-install-app.md)

[Upload Java KeyStore certificate](../task/mw-upload-jks-cert.md)

[Configure bot ID and AI assistant](../task/mw-setup-botid.md)

[Use Moveworks on employee portal](../concept/mw-employee-chat-ui.md)

