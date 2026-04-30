---
title: Amazon Kinesis discovery
description: The ServiceNow Discovery application uses the Amazon Kinesis discovery pattern to find Kinesis services available on Amazon Web Services \(AWS\).
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Amazon Kinesis discovery

The ServiceNow® Discovery application uses the Amazon Kinesis discovery pattern to find Kinesis services available on Amazon Web Services \(AWS\).

Kinesis is a managed, scalable, AWS cloud-based service that allows real-time processing of streaming large amount of data per second. AWS Kinesis contains four types of services:

-   Kinesis Video Streams - capture, process, and store video streams for analytics and machine learning.
-   Kinesis Data Streams - a fully-managed streaming data service.
-   Kinesis Data Firehose - load data streams into AWS data stores.
-   Kinesis Data Analytics- process and analyze streaming data.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   Install the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   Verify the following plugin versions:
    -   Discovery and Service Mapping Patterns 1.0.93 or later \(sn\_itom\_pattern\)
    -   CMDB CI Class Models version 1.40.0 or later \(sn\_cmdb\_ci\_class\)

## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

**Note:** You can test the AWS REST APIs using Postman API platform. For more information, see the [How to test AWS REST API using POSTMAN \[KB0782183\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0782183) article in the Now Support Knowledge Base.

## Data collected by Discovery during horizontal discovery

The discovered data includes the following fields in the Cloud Database \[cmdb\_ci\_aws\_kinesis\] table.

<table id="table_pw1_srb_b5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID

</td><td>

Stream resource name.

</td></tr><tr><td>

Name

</td><td>

The name of the stream.

-   Kinesis Data - cmdb\_ci\_aws\_kinesis\_data
-   Kinesis Video - cmdb\_ci\_aws\_kinesis\_video
-   Kinesis Firehose - cmdb\_ci\_aws\_kinesis\_firehose
-   Kinesis Data Analytics - cmdb\_ci\_aws\_kinesis\_data\_analytics

</td></tr><tr><td>

Status

</td><td>

The status of the stream.

</td></tr></tbody>
</table>## Configuration item \(CI\) relationships

|CI|Relationship|CI|
|---|------------|---|
|AWS Kinesis Data|Hosted on::Hosts|AWS Datacenter|
|AWS Kinesis Video|Hosted on::Hosts|AWS Datacenter|
|AWS Kinesis Firehose|Hosted on::Hosts|AWS Datacenter|
|AWS Kinesis Data Analytics|Hosted on::Hosts|AWS Datacenter|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

