---
title: Microsoft Azure Virtual Network spoke release notes
description: Version history for the Integration Hub Microsoft Azure Virtual Network spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-microsoft-azure-virtual-network.html
release: store
topic_type: reference
last_updated: "2024-11-07"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Microsoft Azure Virtual Network spoke release notes

Version history for the Integration Hub Microsoft Azure Virtual Network spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.0.0 - November 2024**
    -   New:
        -   Microsoft Azure Automation Spoke now makes use of the default alias for Microsoft Resource Management Spoke \(sn\_azure\_rm\_spoke.Microsoft\_Azure\_Resource\_Management\)
        -   New Actions with latest design pattern of complex object outputs, retry policy, connection &amp; credentials, and error evaluation making use of the new connection &amp; credential alias:
            -   Network Interface Management: Create Network Interface \(create\_network\_interface\),Delete Network Interface \(delete\_network\_interface\),Get Network Interfaces by Resource Group \(Metadata\) \(get\_network\_interfaces\_by\_resource\_group\_metadata\),Get Network Interfaces by Subscription ID \(Metadata\) \(get\_network\_interfaces\_by\_subscription\_id\_metadata\),Look up Network Interface \(look\_up\_network\_interface\),Look up Network Interfaces Stream by Resource Group \(look\_up\_network\_interfaces\_stream\_by\_resource\_group\),Look up Network Interfaces Stream by Subscription ID \(look\_up\_network\_interfaces\_stream\_by\_subscription\_id\),Update Network Interface Tags \(update\_network\_interface\_tags\)
            -   Public IP Address Management: Create Public IP Address \(create\_public\_ip\_address\),Delete Public IP Address \(delete\_public\_ip\_address\),Get Public IP Addresses by Resource Group \(Metadata\) \(get\_public\_ip\_addresses\_by\_resource\_group\_metadata\),Get Public IP Addresses by Subscription ID \(Metadata\) \(get\_public\_ip\_addresses\_by\_subscription\_id\_metadata\),Look up Public IP Address \(look\_up\_public\_ip\_address\),Look up Public IP Addresses Stream by Resource Group \(look\_up\_public\_ip\_addresses\_stream\_by\_resource\_group\),Look up Public IP Addresses Stream by Subscription ID \(look\_up\_public\_ip\_addresses\_stream\_by\_subscription\_id\),Update Public IP Address Tags \(update\_public\_ip\_address\_tags\)
            -   Subnet Management: Create Subnet \(create\_subnet\),Delete Subnet \(delete\_subnet\),Get Subnets \(Metadata\) \(get\_subnets\_metadata\),Look up Subnet \(look\_up\_subnet\),Look up Subnets Stream \(look\_up\_subnets\_stream\)
            -   Virtual Network Management: Create Virtual Network \(create\_virtual\_network\),Create Virtual Network with Subnet \(create\_virtual\_network\_with\_subnet\_v2\),Delete Virtual Network \(delete\_virtual\_network\),Get Virtual Networks by Resource Group \(Metadata\) \(get\_virtual\_networks\_by\_resource\_group\_metadata\),Get Virtual Networks by Subscription ID \(Metadata\) \(get\_virtual\_networks\_by\_subscription\_id\_metadata\),Look up Virtual Network \(look\_up\_virtual\_network\),Look up Virtual Network Usage Status Stream \(look\_up\_virtual\_network\_usage\_status\_stream\),Look up Virtual Networks Stream by Resource Group \(look\_up\_virtual\_networks\_stream\_by\_resource\_group\),Look up Virtual Networks Stream by Subscription ID \(look\_up\_virtual\_networks\_stream\_by\_subscription\_id\),Update Virtual Network Tags \(update\_virtual\_network\_tags\)
    -   Removed:
    -   -   Deprecated old credential alias Azure\_Virtual\_Network \(sn\_azure\_vn\_spoke.Azure\_Virtual\_Network\)
-   Deprecated actions that make use of old credential alias:
    -   Network Interface Management: Create Network Interface \(Deprecated\) \(create\_nic\),Delete Network Interface \(Deprecated\) \(delete\_nic\),Get Network Interface Information \(Deprecated\) \(get\_nic\),Set Network Interface Tags \(Deprecated\) \(update\_tags\_nic\),List Network Interface Names by ResourceGroup \(Deprecated\) \(list\_network\_interface\_names\_by\_resourcegroup\),Look Up Network Interfaces By Resource Group \(Deprecated\) \(list\_nic\_by\_resource\_group\),Look Up Network Interfaces By Subscription ID \(Deprecated\) \(list\_by\_subscriptionid\),Set Network Interface Tags \(Deprecated\) \(update\_tags\_nic\)
    -   Public IP Address Management: Create Public IP Address \(Deprecated\) \(create\_ip\_address\),Delete Public IP Address \(Deprecated\) \(delete\_ip\_address\),Get Public IP Address Information \(Deprecated\) \(get\_ip\_address\),List Public IP Names by ResourceGroup \(Deprecated\) \(list\_public\_ip\_names\_by\_resourcegroup\),Look Up Public IPs By Resource Group \(Deprecated\) \(list\_by\_resourcegroup\),Look Up Public IPs By Subscription ID \(Deprecated\) \(list\_by\_subscription\_id\),Set Public IP Tags \(Deprecated\) \(update\_tags\_ip\_address\)
    -   Subnet Management: Create Subnet \(Deprecated\) \(create\_subnets\),Delete Subnet \(Deprecated\) \(delete\_subnets\),Get Subnet Information \(Deprecated\) \(get\_subnets\),List of Subnet Names \(Deprecated\) \(list\_of\_subnet\_names\),Look Up Subnets \(Deprecated\) \(list\_of\_subnets\)
    -   Virtual Network Management: Create Virtual Network \(Deprecated\) \(create\),Create Virtual Network With Subnet \(Deprecated\) \(create\_virtual\_network\_with\_subnet\),Delete Virtual Network \(Deprecated\) \(delete\),Get Virtual Network Information \(Deprecated\) \(get\),Get Virtual Network Usage Status \(Deprecated\) \(list\_usage\_status\),List Network Names by ResourceGroup \(Deprecated\) \(list\_network\_names\_by\_resourcegroup\),Look Up Virtual Networks By Resource Group \(Deprecated\) \(list\_by\_resource\),Look Up Virtual Networks By Subscription ID \(Deprecated\) \(list\_by\_subscription\),Set Virtual Network Tags \(Deprecated\) \(update\_tags\)
-   **Version 1.0.5 - September 2022**

    Fixed: Improve installation performance of spoke.

-   **Version 1.0.4 - July 2020**

    Patch release of the Microsoft Azure Virtual Machine spoke for IntegrationHub. This version adds KMF modules for additional security of password2 fields and Rome compatibility.

-   **Version 1.0.2 - June 2020**

    Provides actions to automate the management of virtual networks, subnets, network interfaces, and public IP addresses in Azure.


