---
title: Administration module
description: Use the Administration module to manage third-party providers and the configuration of entity classes.
locale: en-US
release: yokohama
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Administration module

Use the Administration module to manage third-party providers and the configuration of entity classes.

Regulatory Intelligence providers deliver regulatory alerts that include a variety of regulatory changes. Each regulatory alert record contains the taxonomy section for the regulatory taxonomy associated with the alert. This taxonomy helps in classifying and categorizing the alert. The internal taxonomy design contains the following five elements:

-   Regulatory Body
-   Sector
-   Theme
-   Content Type
-   Jurisdiction

When setting up the Regulatory Change Management application, you have to map the external taxonomy to your own internal taxonomy for standardization. The design elements are created and mapped from the provider’s external taxonomy during the setup process.

After you set up the internal taxonomy, the next step is to update the provider configuration record with the name and description of the providers. To maintain a generic provider configuration, a provider record is used. Providers can send the data via multiple combinations, such as via a single file or as an API. To learn more, see [Map the taxonomy](../task/manage-taxonomy.md).

You can use the Administration module to configure various records. You can do the following:

-   Update provider configuration record to define and receive the data from the providers.
-   Configure the entity classes that may be impacted due to the regulatory changes.

