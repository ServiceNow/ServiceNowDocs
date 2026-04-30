---
title: Tables installed with Governance, Risk, and Compliance
description: Tables are added with activation of GRC plugin.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [GRC reference, Common GRC features, Governance, Risk, and Compliance]
---

# Tables installed with Governance, Risk, and Compliance

Tables are added with activation of GRC plugin.

<table id="table_akh_kqq_nwb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Control objective to object staging table \[sn\_grc\_pci\_control\_objective\_object\_staging\]

</td><td>

Stores the staged data of control objective and configuration test mappings.

</td></tr><tr><td>

Control objective mapping import configuration \[sn\_grc\_pci\_control\_objective\_mapping\_import\_configuration\]

</td><td>

Stores the metadata of the configuration information required to ship the records from the staging table to the target table.

</td></tr><tr><td>

Control objective mapping import additional fields configuration \[sn\_grc\_pci\_control\_objective\_mapping\_import\_additional\_fields\_configuration\]

</td><td>

Stores the metadata of key-value pairs pertaining to any additional columns on the target m2m table.

</td></tr><tr><td>

Content Reference to Authority Documentsn\_grc\_m2m\_cont\_ref\_auth\_doc

</td><td>

Many-to-many relationship table that stores the mapped data between the content references and authority documents.

</td></tr><tr><td>

Content Reference to Citation\[sn\_grc\_m2m\_cont\_ref\_citation\]

</td><td>

Many-to-many relationship table that stores the mapped data between the content references and citation.

</td></tr><tr><td>

Content Reference to Control Objective\[sn\_grc\_m2m\_cont\_ref\_ps\]

</td><td>

Many-to-many relationship table that stores the mapped data between the content references and control objectives.

</td></tr><tr><td>

Functional domain \[sn\_grc\_functional\_domain\]

</td><td>

Stores the metadata of the list of functional domains.

</td></tr><tr><td>

Functional domain configuration \[sn\_grc\_functional\_domain\_configuration\]

</td><td>

Stores the configuration information of all audit and compliance objects that are classified as IT related.

</td></tr><tr><td>

Functional domain configuration m2m relationship registry \[sn\_grc\_functional\_domain\_config\_m2m\_relationship\_registry\]

</td><td>

Stores the m2m mapping of the relationship registries that determine the parent table, child table, and the relationship between the two.

</td></tr><tr><td>

GRC functional domain user action \[sn\_grc\_functional\_domain\_user\_action\]

</td><td>

Stores the manually triggered user actions of adding and removing of objects as IT related.

</td></tr><tr><td>

Issue to Content \[sn\_grc\_m2m\_issue\_content\]

</td><td>

Many-to-many relationship table that is used to manage relationships between issue and control objective.

</td></tr><tr><td>

Issue to Document \[sn\_grc\_m2m\_issue\_document\]

</td><td>

Many-to-many relationship table that is used to manage relationships between issue and policy table and between issue and authority document.

</td></tr><tr><td>

Issue to Engagement \[sn\_grc\_m2m\_issue\_engagement\]

</td><td>

Many-to-many relationship table that is used to manage relationships between issue and engagement.

</td></tr><tr><td>

Issue to Item \[sn\_grc\_m2m\_issue\_item\]

</td><td>

Many-to-many relationship table that is used to manage relationships between issue and control.

</td></tr><tr><td>

Item to entity \[sn\_grc\_m2m\_item\_entity\]

</td><td>

Many-to-many relationship table that stores associated reliant entities with common controls.

</td></tr><tr><td>

Item to entity type \[sn\_grc\_m2m\_item\_entity\_type\]

</td><td>

Stores entity type ID record for entity type association.

</td></tr><tr><td>

Indicator \[sn\_grc\_indicator\]

</td><td>

Stores details of indicators.

</td></tr><tr><td>

Supporting Data \[sn\_grc\_indicator\_supporting\_data\]

</td><td>

Stores the supporting data collected after the indicator job run \(GRC indicator nightly run\).

</td></tr><tr><td>

Indicator Supporting Data Statistics \[sn\_grc\_indicator\_supporting\_data\_statistics\]

</td><td>

Stores statistics of indicators for collecting supporting data, which is leveraged by the supporting data collection job.

</td></tr></tbody>
</table>**Parent Topic:**[Governance, Risk, and Compliance reference](../concept/grc-reference.md)

