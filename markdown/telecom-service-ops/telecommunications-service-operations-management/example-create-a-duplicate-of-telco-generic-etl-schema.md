---
title: Example - Duplicate the Telco Generic ETL Schema
description: This example walks you through how to duplicate the Telco Generic Schema ETL to set up a customized Service Graph Connector \(SGC\) ETL for your telecom integration. Use this procedure when you want to create a baseline ETL in your connector’s application scope based on the standardized Telco Generic Schema, ensuring schema alignment, consistency, and faster deployment.
locale: en-US
release: zurich
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Duplicate Telecom Discovery Builder, Configure Telecom Discovery Builder, Set up Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Example - Duplicate the Telco Generic ETL Schema

This example walks you through how to duplicate the Telco Generic Schema ETL to set up a customized Service Graph Connector \(SGC\) ETL for your telecom integration. Use this procedure when you want to create a baseline ETL in your connector’s application scope based on the standardized Telco Generic Schema, ensuring schema alignment, consistency, and faster deployment.

## Scenario

You are deploying a new Service Graph Connector and need to duplicate the Telco Generic Schema ETL into your connector’s application scope.

Create a temporary data source, duplicate the ETL, and configure it to work with your connector’s device payloads.

## Steps to duplicate the Telco Generic Schema ETL

1.  Switch to the connector’s application scope where you want to duplicate the ETL \(e.g., Nokia NSP Connector\).
2.  Create the data source:
    -   Navigate to System Import Sets &gt; Administration &gt; Data Sources.
    -   Locate the Generic Schema Multi-Source Data Source provided by the TSOM Core application.
    -   Copy this data source into your connector’s application scope.
    -   Test the copied data source by running Test Load 20 Records to create a sample import set.
3.  Open the Duplicate ETL Transform Map Dialog: In ETL Studio, select Duplicate ETL to start the duplication process.
4.  In the **Duplicate from** list, choose Telco Generic Schema.
5.  Select **Add new…** and enter a name for the duplicated ETL.
6.  Select importSet as the discovery source for your duplicated ETL.
7.  Enter a new name for the duplicated transform map.
8.  Specify the newly created temporary data source that you copied from the Generic Schema Multi Source.
9.  Optionally, enable **Auto-pull a new import set** to automatically load new records after duplication.
10. Click **Create Duplicate** to complete the duplication.
11. Update **Basic Details**:
    -   After duplication, open the newly created ETL.
    -   In step 1: specify **Basic Details**, replace the temporary data source with your connector’s production data source.
12. Save the ETL Configuration: click **Save** to finalize your changes.
13. Run the **Data Source**: From Import Schedules, run your connector’s data source to ingest real device data.

Result: The system creates a new ETL based on the Telco Generic Schema settings and processes the payloads from your specified connector data source. The imported data is transformed into Configuration Items \(CIs\) and inserted into the ServiceNow CMDB with the expected relationships and structures.

