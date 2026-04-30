---
title: TISC Data Processing Functional Flow
description: Threat Intelligence Security Center \(TISC\) provides a solution that automates the data collection and processing which helps reduce the burden on Threat Intel Analysts by avoiding manual steps involved.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Threat Intelligence Security Center, Security Operations]
---

# TISC Data Processing Functional Flow

Threat Intelligence Security Center \(TISC\) provides a solution that automates the data collection and processing which helps reduce the burden on Threat Intel Analysts by avoiding manual steps involved.

Threat Intelligence Security Center \(TISC\) collects intelligence using one of the following methods:

1.  Ingestion from data sources that are preconfigured and run on a schedule.
2.  Threat Intel Analysts importing data using the Import Intelligence feature.
3.  Manually creating individual records within the application.

    **Note:** The data collected in the application will be processed to normalize, de-duplicate, and aggregate the information before loading into Threat Intel library.


## Basic terminology used in Data Processing

1.  Source Tables: The Source tables contains the data related to the entities that are fetched from multiple sources, and then the records will be created by each source.
2.  Aggregated Records: The Aggregated records tables contains the data related to a specific entity by aggregating the data from all the source records of a specific entity.

## TISC Data Flow

1.  On a successful execution of import intelligence/Data Source, the records would be created in the corresponding source tables.
2.  Once data comes into source table, the data goes through Filtering logic to validate if the record should be filtered based on configured **Inbound Filtering Rules**. \(Let’s consider SourceRecord1 as a source record for our explanation\).
3.  If the record gets filtered by any of the configured Inbound Filtering Rules, the corresponding source record \(SourceRecord1\) is marked as **Filtered** and rule which filtered the record can be found in Applied Filter Rule.
4.  Let’s assume the source record \(SourceRecord1\) aggregates to AggregateRecord1.
5.  If the record is not filtered, the record is marked for de-duplication by setting processing status to Ready for De-Duplication.
6.  De-Duplication logic validates the below:
    1.  Whether incoming source record \(SourceRecord1\) is duplicate of any existing source records for AggregateRecord1.
    2.  Any of the existing source records for AggregateRecord1 is a duplicate of incoming source record \(SourceRecord1\).
7.  Every entity has specific fields and relationships based on which the source record is validated for Duplication.
8.  If incoming source record \(SourceRecord1\) is a duplicate of any existing source record of AggregateRecord1, the incoming source record \(SourceRecord1\) is marked as Duplicate.
9.  If any of the existing source record \(Existing Source Record1\) of AggregateRecord1 is identified as duplicate of incoming source record \(SourceRecord1\), then existing source record \(Existing Source Record1\) is marked as Duplicate and incoming source record \(SourceRecord1\) is marked for aggregation by setting the processing status to Ready for Aggregation.
10. As part of aggregation, fields of aggregated record AggregateRecord1 will be updated based on values from multiple source records will be aggregated as per the predefined criteria defined in the system.

![Data Processing in TISC](../image/tisc-data-processing.png)

