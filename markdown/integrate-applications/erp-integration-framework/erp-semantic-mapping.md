---
title: Zero Copy Connector for ERP semantic mapping
description: Semantic field mapping uses AI to match source fields from an external system to target fields in the platform data model, ranked by semantic similarity rather than name or alphabetical order.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-semantic-mapping.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-04-27"
reading_time_minutes: 1
keywords: [erp, match, field, map]
breadcrumb: [Reference, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Zero Copy Connector for ERP semantic mapping

Semantic field mapping uses AI to match source fields from an external system to target fields in the platform data model, ranked by semantic similarity rather than name or alphabetical order.

When you configure a Zero Copy Connector for ERP \(Enterprise Resource Planning\) platform data model, you map fields from an external system to fields in the corresponding Glide table. This mapping can involve hundreds of fields on each side. Semantic field mapping uses AI to identify the most relevant target field for each source field you select, reducing the manual effort required to complete the mapping.

## Semantic field mapping process

When you select a source field in the inputs or outputs configuration of a platform model operation entity, the platform evaluates all candidate target fields in the Glide table and ranks them by semantic relevance to the selected source field. The ranked list of candidates is displayed automatically so you can review and confirm the mapping.

\[Omitted image "erp-semantic\_mapping1.jpg"\] Alt text: Specify inputs page with a field label selected and mapped value options listed.

\[Omitted image "erp-semantic\_mapping2.jpg"\] Alt text: Specify outputs page with a field label selected and mapped value options listed.

The ranking is based on semantic similarity — the meaning of the field relative to the source field — rather than alphabetical order or exact name matching. Fields with different names can rank highly if their semantic meaning is closely related. The ranking takes into consideration all source fields and all target fields. Then it ranks the target fields considering a 1:1 mapping with the source fields, maximizing the similarity between sources and targets.

Semantic field mapping can consider field type and description in addition to field name when evaluating candidates.

## Scope and applicability

The automatic semantic field mapping is available when the source table has an associated platform table.

## Confidence scores and ranking

Each candidate target field is assigned a confidence score that reflects how closely its semantic meaning matches the selected source field. You can review the ranking before confirming the mapping.

**Important:** AI-generated field mapping suggestions may not be accurate in all cases. Review the ranked candidates and confirm the appropriate target field before saving the connector model.

**Parent Topic:**[Zero Copy Connector for ERP reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-integration-reference.md)

