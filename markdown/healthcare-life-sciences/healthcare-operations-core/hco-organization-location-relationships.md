---
title: Organization and location relationships in Healthcare Operations Core
description: The tables that make up your organization and location model span two topics: how Healthcare Operations Core extends the Service Model Foundation \(SMF\) hierarchy, and how healthcare organizations and healthcare locations layer on top of it. Read both together to understand the full picture before you configure either one.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/healthcare-operations-core/hco-organization-location-relationships.html
release: australia
product: Healthcare Operations Core
classification: healthcare-operations-core
topic_type: concept
last_updated: "2026-07-14"
reading_time_minutes: 1
breadcrumb: [Configure, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Organization and location relationships in Healthcare Operations Core

The tables that make up your organization and location model span two topics: how Healthcare Operations Core extends the Service Model Foundation \(SMF\) hierarchy, and how healthcare organizations and healthcare locations layer on top of it. Read both together to understand the full picture before you configure either one.

## The big picture

Two separate chains of tables both hang off Business Organization, and it's easy to read about one without realizing how it connects to the other:

-   The Service Model Foundation \(SMF\) hierarchy establishes who's requesting and fulfilling a case: **Case** → **Requesting or Supporting service organization** → **Internal Organization or External Organization**.
-   The healthcare profile layer attaches identity and physical space to that record: **Business Organization** → \[1:1\] → **Healthcare Organization** → \[many-to-many, through the healthcare organization location association table\] → **Healthcare Location** → \[reference\] → **Common Location** \(the physical address\).

Healthcare location and healthcare organization aren't part of the SMF extension hierarchy, they're a parallel layer that connects to it only through Business Organization and the organization-location association. A case never references a healthcare organization or healthcare location directly.

Both chains are healthcare's take on the same Service Model Foundation \(SMF\) framework used across other industries. For the platform-wide picture, see [Service Model Foundation overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-industry-data-model.md).

## What to read next

Read the following topics in order to go from the data model to a configured hierarchy:

1.  [Understanding Service Model Foundation in Healthcare Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/healthcare-operations-core/understanding-service-model-foundations-hco.md)—the SMF extension hierarchy, case visibility fields, and importing location data.
2.  —a worked example applying that hierarchy to a hospital system.
3.  [Setting up healthcare locations and healthcare organizations]()—healthcare organization and healthcare location profiles, and how the two are associated.

