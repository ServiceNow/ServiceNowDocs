---
title: Using Investigative Case Management Evidence Management
description: Investigative Case Management Evidence Management guides investigators through the process of logging and managing all physical and digital evidence associated with a case, ensuring it's consistently classified, accessed, and associated with relevant investigative records.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Using Investigative Case Management, Solutions, Use, Public Sector Digital Services \(PSDS\)]
---

# Using Investigative Case Management Evidence Management

Investigative Case Management Evidence Management guides investigators through the process of logging and managing all physical and digital evidence associated with a case, ensuring it's consistently classified, accessed, and associated with relevant investigative records.

![Evidence Management evidence details view](../image/psds-icm-evidence-details-view.png)

The Evidence Management feature provides a structured, searchable record system for managing evidence across all investigative contexts, whether the evidence is a physical item stored in a law enforcement evidence locker, or a digital file hosted on a cloud platform. With thorough metadata, customizable access controls, and auto-linkage to cases, people, locations, events, and other entities, investigators can track and integrate evidence into case data. For civilian and internal investigative units, Evidence Management offers a comprehensive method for documenting evidence custody, keeping related records, and maintaining audit compliance.

With Evidence Management, investigators and supervisors can:

-   Upload or log new evidence \(physical or digital, such as documents, images, web-hosted files, or physical items\) and view a list of evidence records per case
-   Map evidence to the investigation and assign it to a subject, event, location entity
-   Link evidence to a person, location, event, vehicle, property, or organization
-   Capture and store key metadata, such as evidence type, evidence source, the date it was received, and associated notes
-   Track the movement, transfer, and status changes of evidence records with timestamps and responsible personnel for each action with the digital chain of custody feature.
-   Track custody or handler information for a piece of evidence in a dedicated chain-of-custody record with audit logging, capturing when and by who something was opened and viewed

Investigators can access Evidence Management directly from the Investigative Case Management workspace through the dedicated **Evidence** tab. The Evidence table in Investigative Case Management is a structured data model for managing all physical and digital evidence, so data can be consistently classified, accessed, and associated with relevant investigative records. Within the **Evidence** tab, you can create an evidence record for a piece of evidence, create a chain of custody log to track its movement, and link evidence records to existing entities within the case. Evidence can be linked to the following entities:

-   Persons \(subjects, victims, witnesses\)
-   Locations \(scene of crime, office, storage\)
-   Events \(arrest, tip-off, scene visit\)
-   Vehicles \(suspect or involved vehicles\)
-   Property \(items discovered or stolen\)
-   Organizations \(gangs, schools, employers\)

For information on how to link evidence to entities, see [Associate and link evidence to entities](../task/psds-using-icm-associate-evidence-entities.md).

## Evidence Tabs

![evidence tabs view](../image/psds_icm_evidence_tabs.png)

In Evidence Management, an investigator can view details about the evidence through the evidence record page. The evidence record page has the following tabs:

-   **Details**

    View high-level details about the evidence record, such as evidence notes, and how the evidence is related to the case.

-   **Cases**

    View the cases that are linked to the evidence record. An investigator can link multiple cases to one evidence record.

-   **Chain of Custody**

    Track the movement, transfer, and status changes of evidence records with timestamps and responsible personnel for each action with the digital chain of custody feature.

-   **Persons**

    The **Persons** tab allows investigators to link one or more person entity records to the record of a specific evidence item. Here, investigators can associate a single evidence item with a person, such as a Subject, Witness, Victim, or Other. If a piece of evidence is collected in relation to a specific person, add this person under the **Persons** tab in the Evidence Record. A single evidence item may be associated with one or multiple entities, and can also be associated with one or multiple cases.

-   **Locations**

    The Locations tab allows investigators to add or link locations to a specific piece of evidence.

-   **Events**

    The Events tab allows investigators to link either incident or investigation event records to an evidence record. If a piece of evidence is collected in relation to a specific event, that event can be added under the Events tab in the Evidence Record.

-   **Properties**

    The Property tab allows users to add or link property items to a specific piece of evidence. Users are able to add new properties, view existing ones linked with the case in a related tab or list, and edit them. If a piece of evidence is collected in relation to a specific property, that property can be added under the Properties tab in the Evidence Record. The vehicle index and firearm index tables are an extension of the property index table.

-   **Vehicles**

    The Vehicles tab allows an investigator to link one or more vehicle entity records to an evidence record. Each vehicle record profile stores critical identifiable information about a vehicle, and allows it to be associated with a specific piece of evidence. For example, if a piece of evidence was recovered from, or collected in relation to a specific vehicle, an entity record may be created for this vehicle, and it can then be linked to the Evidence record. The vehicle index and firearm index tables are an extension of the property index table.

-   **Firearms**

    The Firearms tab allows users to link one or more firearm entity records to an evidence record. Each firearm profile stores critical identifiers, traits, and historical data. The vehicle index and firearm index tables are an extension of the property index table.

-   **Organizations**

    The Organization tab allows users to create and manage records of organizations that are related to the case. Users are able to add new organizations, view existing ones in a related tab or list, and edit details as they become available. If a piece of evidence is collected in relation to a specific organization, that organization should be added under the **Organizations** tab in the Evidence Record.


## Chain of Custody Log

![Investigative Case Management Evidence Management Chain of Custody Log View](../image/psds-evid-management-coc-view.png)

Track the movement, transfer, and status changes of evidence records with a dedicated digital Chain of Custody \(CoC\) log tab, featuring audit logging, timestamps, and information about responsible personnel for each action. Investigators can create entries of custody events, and include information such as the sender, receiver, timestamp, and purpose, which can be especially useful for internal investigations \(e.g., OIGs, compliance offices, HR\) and offices with multiple investigative departments working with a single set of evidence. A document upload or signature capture within the custody record can also be configured by an admin.

In the Investigative Case Management application, a Chain of Custody record answers:

-   The action\(s\) taken on the evidence
-   When this action took place, and by whom
-   Where the evidence had been collected from, and from whom
-   The method of transfer from one location and person to another
-   Where it physically and/or digitally resides

The following example shows the view for an investigator who wants to view the log for a piece of evidence.![Evidence Management CoC Log](../image/icmcocview.png)

For information on how to create a chain of custody log in Evidence Management, see [Create a chain of custody log for an evidence record in an investigative case](../task/psds-using-icm-create-chain-of-custody-log.md).

