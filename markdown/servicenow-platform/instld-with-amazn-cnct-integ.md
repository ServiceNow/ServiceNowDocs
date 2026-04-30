---
title: Components installed with Amazon Connect Integration with ServiceNow Voice
description: Several types of components are installed with installation of the Amazon Connect Integration with Voice application \(sn\_cti\_amzn\_cct\), including user roles, plugins, and operation handlers.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ServiceNow Voice reference, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Components installed with Amazon Connect Integration with ServiceNow Voice

Several types of components are installed with installation of the Amazon Connect Integration with Voice application \(sn\_cti\_amzn\_cct\), including user roles, plugins, and operation handlers.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Amazon Connect administrator\[sn\_cti\_amzn\_cct.admin\]

</td><td>

Configures the integration with the Amazon Connect instance.

</td><td>

sn\_cti\_core.admin

</td></tr></tbody>
</table>## Plugins installed

|Plugin|Description|
|------|-----------|
|ServiceNow Voice - Core \(sn\_cti\_core\)|Provides the framework that supports the integration with your third-party phone system.|
|Openframe \(com.sn\_openframe\)|Provides an interface to integrate a communication frame to place and receive calls.|

## Operation handlers installed

Operation handlers are defined in the ServiceNow instance to run a script based on the intent of the caller and provide response to the caller.

|Plugin|Description|
|------|-----------|
|$connect.kinesis.event|Receives and processes the call trace record that is created by Amazon Connect in the Amazon Kinesis stream.|
|$connect.s3.event|Receives and processes JSON events from the S3 buckets where the call recording, transcript and analysis data is created and stored. Associates this information with an interaction and Openframe call log records.|
|createPhoneLog|Creates a PhoneLog for each call transfer and links the Phone Log to the Interaction Related Record|

**Parent Topic:**[ServiceNow Voice reference](ccc-reference.md)

