---
title: Security Case Management
description: Security Case Management provides a means for security analysts who are engaged in threat hunting to gather information on suspicious activity in their environment. Case-related records, such as security incidents, observables, CIs, and affected users can be added to cases to accommodate broad and specific analysis.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Security Case Management

Security Case Management provides a means for security analysts who are engaged in threat hunting to gather information on suspicious activity in their environment. Case-related records, such as security incidents, observables, CIs, and affected users can be added to cases to accommodate broad and specific analysis.

With the ability to easily pivot through the records and related information, analysts can assess whether they are facing a targeted campaign, advanced persistent threat, and so forth.

Security cases can be created from various sources on your instance, including Security Case Management, Security Incident Response, and Threat Intelligence. You can also create cases from configuration items and affected users in the Configuration Items \[cmdb.ci\] and Users \[sys.user\] tables, respectively. After cases have been created, each of these sources can be also used to add valuable analysis resources to existing cases.

Each security case consists of three main sections, a header section, a section with additional case details, and a case artifacts section containing a collection of records that aid in building an argument for identifying and dealing with particular threats.

## Case header

![Case header](../image/case-header.png "Case header section")

The case header provides basic information used to identify and classify the security case. The case number uses the SECC prefix.

## Additional case details

![Additional case details](../image/case-addtl-details.png "Additional Case Details section")

The **Additional Case Details** section provides information specific to the analysis that has already been performed on the case, including its current state, and work notes and activities recorded for the case.

## Case artifacts

![Case artifacts](../image/case-dossier.png "Case Artifacts section")

The **Case Artifacts** section provides a series of tabs of information contained in the security case.

You can perform searches within the contents of each tab. You can also exclude specific records you have already evaluated as being safe or which are of no value in your investigation. The excluded records are not deleted, but are hidden from view. If needed, you can view excluded records and add them back.

Within each tab, you can click the Additional Details icon to show related information for the selected record. For example, if you click the **Configuration Items** tab to view the Configuration Items Explorer, and click Additional Details for a specific CI, you can view incidents, vulnerable items, and annotations associated with that CI.

![Related data on CIs](../image/related-data-cis.png "Case Artifacts—related detail")

You can also select a record and click the **Annotate** button for a case-related artifact to add annotations to the record. Annotations are simply notes that each analyst can make on a particular artifact.

![Annotations](../image/annotations.png "Security Annotations")

Other tools the analyst can use for examining cases include:

-   [Run a sightings search on observables in a case](../task/run-local-sighted-srch.md)
-   [Search for security artifacts](../task/search-for-artifacts.md)

