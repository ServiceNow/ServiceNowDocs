---
title: Domain separation and Cloud Services Catalog
description: Domain separation is supported in Cloud Services Catalog. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CSC references, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Domain separation and Cloud Services Catalog

Domain separation is supported in Cloud Services Catalog. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Recommendations for domain separation in Cloud Services Catalog

Domain separation recommendations in Cloud Services Catalog:

-   **CSC Guided setup**

    CSC Guided Setup should be executed solely by the system administrator within the global domain. It is important to note that the local domain is not the suited environment for this task.

-   **Terraform Opensource in global domain**

    All the catalogs and config providers are installed in the global domain with the installation of Cloud Services Catalog plugin. Hence, the Out Of Box catalogs will also work only if, you create the Terraform Opensource\(TFO\) configuration and credentials in the global domain and not in a specific domain. This also enables the Managed Service Provider \(MSP\) users to use single TFO server for multiple domains.

-   **Service providers credentials**

    Service providers' \(AWS, Microsoft Azure and Google Cloud Platform credentials should be domain specific. However, Azure DevOps\) and Ansible config installables should be in global domain for provisioning.

-   **MID Server in global domain**

    Set the MID server in the global domain as TFO and related config management is also set in the global context. This enables accurate global discovery.

    MSP users can set global MID servers and also use domain specific MID for different service providers for Day 1.


## Next steps

For more information on how domain separation works in Cloud Provisioning and Governance, visit [Domain separation and Cloud Provisioning and Governance](../../cloud-management-v2/concept/domain-separation-cloud-management.md).

**Parent Topic:**[CSC references](../reference/csc-reference.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=australia&pubname=australia-platform-security&ft:locale=en-US)

