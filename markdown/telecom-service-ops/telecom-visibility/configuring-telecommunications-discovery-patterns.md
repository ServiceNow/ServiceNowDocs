---
title: Configure Telecommunications Discovery \(TSOM\) Patterns
description: This document outlines the dependencies, requirements, and installation steps necessary for setting up Telecommunications Discovery Patterns \(also known as TSOM Patterns\) in TSOM Visibility in ServiceNow.The process of obtaining and installing the Telecommunications Discovery Patterns in TSOM.In order to support the TSOM Visibility solution, we have modified the CMBD CI Class Models store application, introducing updates to the IRE Identification Rules for the following telecom CIs.
locale: en-US
release: yokohama
product: Telecom Visibility
classification: telecom-visibility
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Telecom Discovery using Telecommunications Discovery Patterns, Exploring Telecom Discovery, Telecom Discovery, TSOM Visibility, Telecommunications Service Operations Management]
---

# Configure Telecommunications Discovery \(TSOM\) Patterns

This document outlines the dependencies, requirements, and installation steps necessary for setting up Telecommunications Discovery Patterns \(also known as TSOM Patterns\) in TSOM Visibility in ServiceNow®.

## Before you begin

To use Telecommunications Discovery Patterns, you need a subscription to TSOM.

Role required: admin

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Dependencies and Requirements

-   Telecom Service Operation Core \(sn\_tsom\_core\)
-   Discovery Core plugin \(com.snc.discovery.core\), which is automatically installed by Discovery.
-   ITOM Discovery License plugin \(com.snc.itom.discovery.license\). You must activate this plugin.
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

## TSOM Visibility Installation Disclaimer

See [TSOM Visibility Installation Disclaimer](tsom-visibility.md#section_wn4_2fk_b2c) for important information and requirements related to the installation process.

**Parent Topic:**[Telecom Discovery using Telecommunications Discovery Patterns](telecom-discovery-using-telecommunication-discovery-pattern.md)

## Install Horizontal Discovery and Telecommunication Discovery Patterns

The process of obtaining and installing the Telecommunications Discovery Patterns in TSOM.

### Before you begin

Role required: admin

### Procedure

1.  Install the Horizontal Discovery application.

    See [Discovery setup](https://www.servicenow.com/docs/access?context=discovery-setup&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US), as it is foundational for running Telecommunications Discovery Patterns.

2.  Obtain and install Telecommunications Discovery Patterns:

    1.  Install the Telecommunications Discovery Patterns \(sn\_tsom\_patterns\) from the ServiceNow® Store.

3.  Set up a MID Server and synchronization Patterns:

    1.  Synchronization the installed patterns with the appropriate MID Servers to confirm they’re ready for use:

        1.  Navigate to **Discovery** &gt; **MID Servers**.
        2.  Select **Pattern Sync to Mid**.
        **Note:** This action synchronizes both TSOM and ITOM patterns.

        For more information on how to configure a MID Server, see [Configuring MID Server](https://www.servicenow.com/docs/access?context=configure-mid-server&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

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


## TSOM Visibility Installation Disclaimer

In order to support the TSOM Visibility solution, we have modified the CMBD CI Class Models store application, introducing updates to the IRE Identification Rules for the following telecom CIs.

For more information about CMBD CI Class Models store application, see [CMDB CI Class Models](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/it-operations-management/store-rn-itom-cmdb-class-models.html).

-   **Interface Cards**
-   **Slots**
-   **Subslots**
-   **Network Interfaces**

TSOM Visibility requires CMDB CI Class Models Version 1.69.0 \(**sn\_cmdb\_ci\_class**\).

If you install any of the TSOM Visibility applications \(**sn\_sgc\_altiplano\_connector**, **sn\_tsom\_patterns**, or the **sn\_tsom\_core** plugin\), the CMDB CI Class Models store application is automatically updated \(or installed\) to Version 1.69.0.

**Note:** An administrator can still upgrade the CMDB CI Class Models store application to Version 1.69.0 at their discretion, regardless of whether their Yokohama instance has TSOM Visibility or even if their instance is on a pre-Yokohama release \(for example, Washington DC or Xanadu\).

**IMPORTANT!** If an administrator deploys CMDB CI Class Models Version 1.69.0—whether or not TSOM Visibility is installed—any customized IRE identification rules applied to one or more of the above-mentioned telecom CIs may be affected. These rules will require careful validation to ensure proper functionality.

