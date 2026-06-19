---
title: Activate OData services and assign a system alias
description: Activate the OData services and assign a system alias to support OAuth 2.0 authentication for integration with the Software Asset Management application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/activate-odata-services-sap.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-05-12"
reading_time_minutes: 1
keywords: [OData services, SAP system alias, ICF node, OAuth SAP, post-transport configuration]
breadcrumb: [Set up SAP integration to establish a connection with SAP, Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Activate OData services and assign a system alias

Activate the OData services and assign a system alias to support OAuth 2.0 authentication for integration with the Software Asset Management application.

## Before you begin

The SAP transport must be imported into the target system before performing this configuration.

SAP Role required: SAP Basis administrator

## About this task

Activate the OData services and assign the system alias to activate and configure the OData services with OAuth support.

## Procedure

1.  Open transaction code **/n/IWFND/MAINT\_SERVICE** in your SAP system.

2.  Select the **Find** icon \[Omitted image "search-icon.png"\] to search for the OData services.

3.  Search for and activate each of the following services.

    -   `/NOW/ODATA_VALIDATE_REFRESH_SRV`
    -   `/NOW/ODATA_PULL_DATA_SRV`
4.  For each service, select the **ICF Node** list and activate the ICF node.

    \[Omitted image "sap-odata-icf.png"\] Alt text: Activate and maintain services page on SAP portal

5.  If prompted to assign a package, select **Local Object**.

    \[Omitted image "sap-odata-local.png"\] Alt text: Package selection for OData services

6.  For each service, select **Add System Aliases** &gt; **New Entries**.

7.  In the **SAP System Alias** column, enter `LOCAL`.

    \[Omitted image "sap-odata-alias.png"\] Alt text: Add System Alias option for OData services

8.  Select the **Default System** check box.

9.  Select **Save**.

    If prompted for a customizing request, select **Create** and enter a suitable description. Select **Save** again to save the entries.

    \[Omitted image "sap-odata-create-request.png"\] Alt text: Prompt for customizing request

    \[Omitted image "sap-odata-request.png"\] Alt text: Create request page with the highlighted save option


## Result

The OData services are active and the LOCAL system alias is assigned as the default system for both services.

## What to do next

Create a system user for OAuth authentication. For details, see [Create a system user for OAuth authentication in SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/create-system-user-oauth-sap.md).

