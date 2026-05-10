---
title: Migrate the Verizon eBonding Integration to a Production System
description: This topic outlines the tasks required for moving the Verizon eBonding integration from a Dev/Test environment to a Production environment.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow provided integrations, Integration options, Integration with third-party applications and data sources, Integrations, Configure core features, Administer the ServiceNow AI Platform]
---

# Migrate the Verizon eBonding Integration to a Production System

This topic outlines the tasks required for moving the Verizon eBonding integration from a Dev/Test environment to a Production environment.

This process requires coordination with your assigned Verizon implementation manager.

## General Tasks

The following work can be performed any time:

-   Obtain a production SOAP password from Verizon. Your Verizon SOAP user ID is the same as that used against the Verizon test broker.
-   Create an integration user for Verizon in the ServiceNow Production instance. Use the same user name and password that was created for the development instance, so that the communication between Verizon and ServiceNow is properly authenticated.

## Migrating to a Production Environment

Perform these tasks in order.

-   Task 1: Request the Verizon eBonding plugin for the production instance. When the plugin is installed, the only immediate user interface change is an additional **Category** field named **VZ eBonding**. All of the triggers for the integration are dependent on the category being set to **VZ eBonding**. Enabling the plugin on the production instance should not affect your users. If you wish to take additional precautions, disable the **VZ eBonding** category from the list when the plugin is activated for the instance.
-   Task 2: Set up the Verizon certificate and keystore. Copy these directly over from the Dev instance or regenerate them so that you have separate versions for the Dev and Production instances.
-   Task 3: Configure the integration properties to work with the Production Verizon eBonding system. This is userID, password, and other properties provided by your Verizon representative.
-   Task 4: Change all the Verizon eBroker SOAP Message functions to use Verizon's production SOAP Endpoint. In most cases, the endpoint URL will be: https://pubwebsvc.vzbi.com:443/Trouble\_Management\_v3r0. Verify this URL with the Verizon implementation specialist.
    -   In the **SOAP Message Functions** related list, click each function, clear the **Lock** check box, and enter the production endpoint.
    -   Configure the **SOAP Message Functions** related list and add the **SOAP endpoint** column. In the **SOAP Message Functions** list view, unlock and update the endpoint for all records by [Edit multiple records in a list using the list editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/t_EditMultRecUsingListEditor.md).
-   Task 5: Apply any customizations. If customizations to the integration on the Dev system were captured in an update set, apply that update set to the Production system.
-   Task 6: Provide Verizon with the production SOAP Endpoint. The SOAP endpoint should look something like this: https://yourproductioninstance.service-now.com/ETMSPublish.do?WSDL.
-   Task 7: Coordinate a Production turn up with your Verizon representative to do basic testing.

    **Warning:** Do not create test tickets against the production system without working with the Verizon team. Any tickets created are treated as real tickets.


**Parent Topic:**[ServiceNow provided integrations](../../vendor-specific-integrations/reference/r_ServiceNowProvidedintegrations.md)

