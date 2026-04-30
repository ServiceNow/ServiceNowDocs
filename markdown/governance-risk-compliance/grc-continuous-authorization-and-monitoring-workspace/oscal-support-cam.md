---
title: Export in OSCAL format
description: Continuous Authorization and Monitoring supports the Open Security Controls Assessment Language \(OSCAL\) used by the National Institute of Standards and Technology \(NIST\) that provides control-related information in standardized machine-readable formats. CAM supports Catalog, Profile, System Security Plan \(SSP\), and Plan of Action and Milestones \(POA&amp;M\) models.
locale: en-US
release: zurich
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CAM OSCAL, CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Export in OSCAL format

Continuous Authorization and Monitoring supports the Open Security Controls Assessment Language \(OSCAL\) used by the National Institute of Standards and Technology \(NIST\) that provides control-related information in standardized machine-readable formats. CAM supports Catalog, Profile, System Security Plan \(SSP\), and Plan of Action and Milestones \(POA&amp;M\) models.

## Source tables to fetch data for the models

The following table identifies which CAM tables provide data for each Open Security Controls Assessment Language \(OSCAL\) JSON property during export operations.

|Source table|JSON property|
|------------|-------------|
|Catalog|
|Control objective|controls|
|Control Objective to Control objective requirement|statements parts|
|Test template to Assessment procedure|assessment objective parts|
|Control Objective|guidance|
|Test Template|Assessment-method \(Examine\)|
|Test Template|Assessment-method \(Interview\)|
|Profile|
|Baseline Control|Include-controls|
|Baseline Control|Exclude-controls|
|SSP|
|Authorization boundary|components|
|Authorization package|leveraged-authorization|
|Authorization boundary|security-impact-level|
|Control requirement|statements|
|Authorization boundary|by-components|
|Information type|Information-types|

For step-by-step instructions on exporting each OSCAL model, see the following topics:

-   **[Export OSCAL catalog](../task/export-catalog-cam-ws.md)**  
Export selected control objectives from Continuous Authorization and Monitoring to Open Security Controls Assessment Language \(OSCAL\) JSON format for external system integration or catalog backup.
-   **[Export OSCAL files from authorization package](export-oscal-files-from-authorization-package.md)**  
Export Open Security Controls Assessment Language \(OSCAL\) formatted System Security Plan \(SSP\) and Plan of Action and Milestones \(POA&amp;M\) files from authorization packages for regulatory reporting and inter-agency data exchange.
-   **[Export OSCAL POA&amp;M from list view](../task/export-individual-oscal-poa-m.md)**  
Export selected Plans of Action and Milestones \(POA&amp;M\) records from the CAM list to an Open Security Controls Assessment Language \(OSCAL\) format.

**Parent Topic:**[CAM OSCAL](oscal-cam-ws.md)

**Related topics**  


[Export OSCAL catalog](../task/export-catalog-cam-ws.md)

[Export OSCAL files from authorization package](export-oscal-files-from-authorization-package.md)

[Export OSCAL POA&amp;M from list view](../task/export-individual-oscal-poa-m.md)

