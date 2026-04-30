---
title: Retail case overview
description: The Retail case table stores information about your retail case types and provides the base for retail case creation. This table extends the Customer Service Management case table. All fields utilized through Customer Service Management case remain intact.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Exploring Retail, Retail]
---

# Retail case overview

The Retail case table stores information about your retail case types and provides the base for retail case creation. This table extends the Customer Service Management case table. All fields utilized through Customer Service Management case remain intact.

An abstract case \(or abstract case type\) refers to a base configuration of a case that is not meant to be used directly but is instead designed to be extended by specialized case types.

The abstract Retail case will include only the shared logic such as common fields, Business rules, flows, UI policies, and access controls \(ACLs\). Each specific case type will then extend this base and focus solely on its unique logic. This approach enables cleaner architecture, easier scaling, and tailored user experiences for different case types.

The retail case type introduced within retail builds on existing Customer Service Management case functionality to provide users with retail-specific fields. For more information on these changes, see the [Impact analysis and guidance: Retail case table updates \[KB2216547\]](https://support.servicenow.com/nav_to.do?uri=%2Fkb_knowledge.do%3Fsys_id%3Da312916e978aa650f03d739c1253af88%26sysparm_view%3D%26sysparm_domain%3Dnull%26sysparm_domain_scope%3Dnull) article in the Now Support Knowledge Base.

You can extend your own case types. For information on using retail case types, see [Manage customer complaints](rahi-retail-manage-customer-complaints.md) and [Manage store inquiries](rahi-retail-manage-store-inquiries.md).

For retail case table attributes, see [Retail organization data model tables](rahi-retail-operations-data-model-tables.md). For unified data model of cases and tasks, see [Retail unified case and task data model](rahi-retail-retail-unified-cas-task-data-model.md).

**Parent Topic:**[Exploring Retail](rahi-retail-operations-explore.md)

