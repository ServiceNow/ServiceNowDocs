---
title: Exporting hierarchy of models and templates
description: Learn how to export equipment models, inventory templates, and all their related and referred records from one ServiceNow instance to another to support development-to-production migration of network inventory data.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Explore, Telecommunications Network Inventory]
---

# Exporting hierarchy of models and templates

Learn how to export equipment models, inventory templates, and all their related and referred records from one ServiceNow instance to another to support development-to-production migration of network inventory data.

## Exporting hierarchy of models and templates

The Export Hierarchy feature lets you export network equipment models, inventory templates, and their related records from one ServiceNow instance, in a format suited to your purpose. Use this feature to promote validated configurations from a lower environment to production, share model catalogs with partners or stakeholders, or extract specific records for analysis.

|Your scenario|Use this method|
|-------------|---------------|
|You need the relationships between records preserved as a single package. JSON can be used for moving models, templates, and their complete reference data between ServiceNow instances while preserving system ID continuity. JSON imports handle the full set of inventory model types: equipment, holder, card, interface, facility, topology, cable, strand, and connection models along with their referenced manufacturers, products, classifications, and other supporting data.|Exporting hierarchy via JSON|
|You need to export specific related records of a model or template in a chosen format: for example, exporting equipment data as CSV for analysis, as PDF for a stakeholder review, or as XML for selective re-import.|Exporting hierarchy via XML \(or other selected format\)|

Both methods are launched from the Export Hierarchy action on a model or template record. The method you use depends on whether you select Export Hierarchy directly from a record's context menu \(JSON method\) or use the related-records list \(XML or other-format method\).

|Role|Action performed on "Export Hierarchy" initiation|
|----|-------------------------------------------------|
|sn\_ni\_core.inventory\_admin|Generates a JSON file packaging the hierarchy|
|sn\_ni\_core.telco\_inventory\_catalog\_manager|Generates a JSON file packaging the hierarchy|
|sn\_ni\_core.inventory\_template\_manager|Generates a JSON file packaging the hierarchy|
|Platform admin \(no TNI roles\)|Shows the related-records list is export as XML. Multiple records are exported as one single XML.|

**Related topics**  


[Exporting hierarchy process via JSON](exporting-hierarchy-process-via-json.md)

[Exporting hierarchy via XML](exporting-hierarchy-process-via-xml.md)

