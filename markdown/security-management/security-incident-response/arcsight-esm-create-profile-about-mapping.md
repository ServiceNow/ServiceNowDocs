---
title: Mapping correlation event fields for the ArcSight ESM event ingestion integration
description: After you identify the specific correlation event rule from the list, the next step is to map correlation event fields to the fields in the security incident form.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Use, Set up instance, ArcSight ESM Event Ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Mapping correlation event fields for the ArcSight ESM event ingestion integration

After you identify the specific correlation event rule from the list, the next step is to map correlation event fields to the fields in the security incident form.

## Overview of mapping correlation event fields

For the mapping step, you can ingest sample correlation events for the selected correlation rule. During this mapping phase, you can ensure all relevant correlation event field data is mapped to the appropriate place on the SIR incident form and then visualize the SIR incident in the preview section.

The following figure shows the default mapping configuration that is provided for creating the correlation event profile. You can customize the fields that populate the security incident.

![ArcSight ESM: Create Profile: Default Map](../image/sir-arcsight-esm-profile-default-map.png)

When you click **Retrieve Events**, the correlation event field names and the corresponding values are populated on the left side of the form. These are the ArcSight ESM correlation event fields that are available to map to the security incident fields.

You may prefer to review a few sample correlation events on your console to ingest for the field mapping configuration step. This step is labeled Mapping on the progress bar. If this page is not displayed, click **Mapping** on the progress bar. You can ingest up to five sample correlation events from the ArcSight ESM Manager for the selected correlation rule to assist with the field mapping process. There are options to either ingest the five most recent correlation events for the selected Correlation Event or ingest up to five specific correlation events based on the event IDs.

Below is a summary of the steps required to map correlation events:

-   Field Mapping: Edit the mapping configuration by dragging correlation event fields from the left side and dropping them on the SIR incident mapping section on the right. The mapping on the right associates the incoming correlation event field with an outgoing security incident field.
-   Mapping Experience: Customize the mapping grid by adding or removing fields using the + icon at the bottom of the SIR incident field mapping section. Track overlooked or previously mapped fields with the color coding that is provided \(mapped fields are greyed out, blue fields are unmapped\).
-   Incident Generation Conditions: Once the mapping section is complete, you can define filter conditions so that you can filter which correlation events should create security incidents versus correlation events that should be filtered out, for example, low priority correlation events. This is done in the Incident Generation Conditions section located below the Correlation Event Sample Ingestion section.
-   Event Aggregation Criteria: Define additional event aggregation criteria that aggregates an incoming correlation event to an existing SIR security incident instead of creating similar, potentially duplicate incidents. Using field matching value criteria for each profile, this additional aggregation capability can reduce the number of active, overlapping security incidents by placing all related security notable event data on a single security incident.
-   Format Field Translation: In certain cases, event field values in the ArcSight ESM correlation event may not translate directly to the fields on the SIR security incident. For these values, you can use a script editor to format field values on the security incident during the mapping step. Use the script editor if you want to format values that are similar, but not identical.

    For example, with the script editor, a category value of Malware Alert and Virus Infection may have different field values for the source category but both values can be translated to a common Malicious Code Activity in the Category field on the SIR security incident using the Format Field Translation functionality.


The next step is to ingest sample correlation events and map values to the SIR security incident fields.

