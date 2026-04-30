---
title: Domain separation and External Content Connectors
description: If any conkeyrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file.In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conkeyref at the end that describes domain separation.Domain separation is unsupported for External Content Connectors. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-02-03"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Explore, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Domain separation and External Content Connectors

Domain separation is unsupported for External Content Connectors. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: No support

-   The domain field may exist on data tables but there is no business logic to manage the data.
-   This level is not considered domain-separated.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Overview of domain separation in External Content Connectors

The External Content Connectors ServiceNow® Store application allows you to make content from external source system documents searchable in AI Search applications. External content connectors do not support domain separation.

**Note:** The External Content Connectors application includes an External Content Connectors Service Account user that's assigned to the global domain by default. If your instance has domain separation configured, assigning this user to another domain can prevent user permission crawls from correctly mapping permissions to users in your instance. To correct this behavior, reassign the External Content Connectors Service Account user to the global domain. For details on this procedure, see [Reassign the External Content Connectors Service Account user to the global domain](../task/reassign-ext-cont-connectors-svc-acct-usr-global-domain.md).

**Parent Topic:**[Exploring External Content Connectors](exploring-ext-cont-connectors.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

