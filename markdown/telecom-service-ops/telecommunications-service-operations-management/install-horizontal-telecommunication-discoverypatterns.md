---
title: Install Horizontal Discovery and set up Discovery Patterns
description: Install Horizontal Discovery patterns understanding the dependencies and requirements.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Install Horizontal Discovery and set up Discovery Patterns

Install Horizontal Discovery patterns understanding the dependencies and requirements.

## Before you begin

Role required: admin

Ensure you have a subscription to TSOM.

## About this task

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Dependencies and Requirements:

-   Telecom Visibility Core \(sn\_tsom\_core\)
-   Discovery Core plugin \(com.snc.discovery.core\), which is automatically installed by Discovery.
-   ITOM Discovery License plugin \(com.snc.itom.discovery.license\). You must activate this plugin.
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=australia&pubname=australia-it-operations-management&ft:locale=en-US).

Pattern execution logic: By default, when a TSOM pattern is run, it executes both the TSOM-specific and the corresponding ITOM pattern \(e.g., Telco Router runs Router\). This ensures shared ITOM libraries are reused when needed. To override this behavior:

-   Use the system property sn\_tsom\_patterns.itom\_pattern\_enabled.
-   Setting this property to false ensures only the TSOM-specific pattern is executed.

## Procedure

1.  Install the Horizontal Discovery application.

    See [Discovery setup](https://www.servicenow.com/docs/access?context=discovery-setup&version=australia&pubname=australia-it-operations-management&ft:locale=en-US), as it is foundational for running Telecommunications Discovery Patterns.

2.  Obtain and install Telecommunications Discovery Patterns:

    1.  Install the Telecommunications Discovery Patterns \(sn\_tsom\_patterns\) from the ServiceNow® Store.

3.  Set up a MID Server and synchronization Patterns:

    1.  Synchronization the installed patterns with the appropriate MID Servers to confirm they’re ready for use:

        1.  Navigate to **Discovery** &gt; **MID Servers**.
        2.  Select **Pattern Sync to Mid**.
        **Note:** This action synchronizes both TSOM and ITOM patterns.

        For more information on how to configure a MID Server, see [Configuring MID Server](https://www.servicenow.com/docs/access?context=configure-mid-server&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

4.  Configure TSOM System Properties:

    1.  Set the system property sn\_tsom\_patterns.itom\_pattern\_enabled to define the logic for whether to use only the TSOM Pattern or a combination of ITOM and TSOM patterns.

        1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.
        2.  Select **sn\_tsom\_patterns.itom\_pattern\_enabled**.
        3.  Check that the Value is set to **true** \(default\).
        If you want TSOM to run only TSOM patterns and exclude ITOM patterns, set the Value to **false**.

        **Note:** The default setting is configured to use both TSOM and ITOM patterns.

5.  Enable the replacement of various ITOM patterns with TSOM patters on a specific MID Server:

    For example: The Telecom Router pattern replaces the Network Router pattern for a specific MID Server when **mid.telecom.discovery.patterns.enabled** is set to true for that MID Server.

    1.  Go to the **Filter Navigator** and type **ecc\_agent\_config.list**.

    2.  Select **mid.telecom.discovery.patterns.enabled** \(each MID Server has this parameter\).

    3.  Check that the Value is set to **true**.

    Repeat this configuration for each MID Server that you want to use for running TSOM patterns.


**Related topics**  


[Direct Discovery using Discovery Patterns](../concept/telecom-discovery-using-telecommunication-discovery-pattern.md)

