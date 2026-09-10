---
title: Zero Copy Connector for ERP AI semantic field mapping
description: Semantic field mapping uses AI to rank target fields in the platform data model by how closely their meaning matches a selected source field.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-semantic-mapping.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-08-06"
reading_time_minutes: 1
keywords: [erp, match, field, map]
breadcrumb: [Model management, Using, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Zero Copy Connector for ERP AI semantic field mapping

Semantic field mapping uses AI to rank target fields in the platform data model by how closely their meaning matches a selected source field.

When you configure a Zero Copy Connector for ERP \(Enterprise Resource Planning\) platform data model, you map fields from an external system to fields in the corresponding Glide table. This mapping can involve hundreds of fields on each side. Semantic field mapping uses AI to identify the most relevant target field for each source field you select, reducing the manual effort required to complete the mapping.

## Semantic field mapping process

When you select a source field in the inputs or outputs configuration of a platform model operation entity, the platform evaluates all target fields in the Glide table. It then ranks them by semantic relevance to the selected source field. The ranked list of candidates is displayed automatically so you can review and confirm the mapping.

\[Omitted image "erp-semantic\_mapping1.jpg"\] Alt text: Specify inputs page with a field label selected and mapped value options listed.

\[Omitted image "erp-semantic\_mapping2.jpg"\] Alt text: Specify outputs page with a field label selected and mapped value options listed.

The ranking is based on semantic similarity — the meaning of the field relative to the source field — rather than alphabetical order or exact name matching. Fields with different names can rank highly if their semantic meaning is closely related. The ranking considers all source fields and all target fields together, then orders the target fields for a one-to-one mapping that maximizes the similarity between sources and targets.

Semantic field mapping can consider field name, field type, and field description when evaluating candidates.

## Scope and applicability

The automatic semantic field mapping is available when the source table has an associated platform table.

## Confidence scores and ranking

Each candidate target field is assigned a confidence score that reflects how closely its semantic meaning matches the selected source field. You can review the ranking before confirming the mapping.

**Important:** AI-generated field mapping suggestions may not be accurate in all cases. Review the ranked candidates and confirm the appropriate target field before saving the connector model.

