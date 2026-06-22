---
title: Domain separation and Integration Hub
description: Domain separation is supported for Integration Hub. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/domain-separation-integrationhub.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Integration Hub, Workflow Data Fabric]
---

# Domain separation and Integration Hub

Domain separation is supported for Integration Hub. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard\*

The support level is Standard but has some exceptions or special conditions.

-   Includes all aspects of **Basic** level support.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must be able to configure minimum viable product \(MVP\) business logic and data parameters. This configuration is done per tenant, as expected for the specific application.

Sample use case: An Admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/servicenow-ai-platform-security/domain-separated-apps.md).

## Overview

In general, IntegrationHub inherits the domain separation features of Workflow Studio. As each spoke \(application\) can have its own domain separation relationship, there is no one specific support level to associate with IntegrationHub. To learn more, see [Domain separation and Flow Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/workflow-studio/flow-designer-domain-separation.md).

**Parent Topic:**[Integration Hub reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/integration-hub-reference.md)

**Related topics**  


[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/servicenow-ai-platform-security/domain-sep-landing-page.md)

