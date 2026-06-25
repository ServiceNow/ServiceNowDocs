---
title: Model classification
description: Use model classification to organize and categorize enterprise models and their associated assets in a structured, consistent way across the ServiceNow platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/classification-codes.html
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Enterprise Asset Management data model, Explore, Enterprise Asset Management, IT Asset Management]
---

# Model classification

Use model classification to organize and categorize enterprise models and their associated assets in a structured, consistent way across the ServiceNow platform.

## Overview of classification

Classification codes are structured identifiers assigned to enterprise models. After assigned to a model, a classification code is automatically inherited by all assets created from that model. Classification codes serve a descriptive purpose — supporting reporting, analysis, and grouping — distinct from model categories, which serve a technical purpose by binding model, asset, and CI class tables together.

|Characteristic|Model categories|Model classifications|
|--------------|----------------|---------------------|
|Purpose|Technical — bind model, asset, and CI class tables|Business — organize and classify models for reporting and management|
|Seeded out-of-the-box|Yes — 9 parent, approximately 95 child categories|No — imported or created by an administrator|
|Standard|Platform-defined|Industry standard or customer-defined|
|Drives|Discovery routing, asset-CI synchronization|Filtering, reporting, and taxonomy|

## Classification behavior

-   **Assigning classification to models**

    Classifications are assigned directly to a model record. Only classifications valid for the model's category are selectable. After assignment, the classification applies automatically to all associated assets.

-   **Model category field**

    A classification with a model category defined is only available to models within that category. A classification without a model category applies to all models.

-   **Multi-tier hierarchy**

    Classifications support a parent-child hierarchy. Parent classifications represent higher-level categories; child classifications inherit attributes including source and model category. Each child code can have only one parent. Ancestor lists are automatically generated and updated when parent relationships change.


## Classifications in reporting and dashboards

Classifications can be used as filters in:

-   Enterprise asset overview
-   Enterprise asset dashboard
-   Inventory
-   Enterprise model management
-   Enterprise asset estate

Filtering by a parent classification includes all models and assets associated with that code and all child codes. If the parent is not itself assigned to any model, results still show assets from child codes.

## Industry classification systems

The Enterprise Model Classification table is not seeded out-of-the-box. Organizations can adopt an industry-standard taxonomy or define their own custom system.

|Classification system|Description|Enterprise Asset Management \(EAM\) example|
|---------------------|-----------|-------------------------------------------|
|CSI OmniClass|Classification of construction elements|Standardized categories for air-distribution components \(ducts, diffusers, fans\)|
|CSI UniFormat|Classification of buildings by functional elements, systems, and assemblies|Groups elements such as substructure, shell, interiors, and services consistently|
|ECRI|Healthcare equipment classification|Classifies MRI machines, ventilators, and infusion pumps for conformance and patient safety|
|GICS|Global industry standard|Classifies turbines and substations in energy companies for external reporting|
|ISO 14224|Reliability and maintenance data collection|Monitors failure rates and downtime for robotic arms, conveyors, and CNC machines|
|NAICS|US, Canada, and Mexico industry classification|Maps conveyors, HVAC, or facility systems into industry codes for reporting|
|UNSPSC|Global goods and services taxonomy|Confirms pumps and compressors are consistently classified in procurement workflows|

## Examples of classification systems applied in EAM

|Level 1 code|Level 2 category|Hospital-specific examples|
|------------|----------------|--------------------------|
|A|Substructure|Foundations, basements for imaging or radiation therapy rooms|
|B|Shell|Structural frames, exterior walls, windows, and roofing|
|C|Interiors|Patient rooms, nurse stations, operating rooms, and ICU units|
|D|Services \(MEP systems\)|Specialized HVAC, medical gases, emergency power, plumbing, and fire protection|
|E|Equipment and furnishings|MRI, X-Ray, surgical tables, patient beds, and clinical furniture|
|F|Special construction|Radiation shielding, clean rooms, and isolation rooms|
|G|Building sitework|Ambulance entrances, helipads, parking lots, and landscaping|
|Z|General|General conditions, overhead, administration, and contingency|

**Parent Topic:**[Enterprise Asset Management data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/eam-data-model.md)

**Related topics**  


[Create a source for classification codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/create-class-source-eam.md)

[Import classification codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/import-class-codes-eam.md)

