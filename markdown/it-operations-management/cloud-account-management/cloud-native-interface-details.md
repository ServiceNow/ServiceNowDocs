---
title: Cloud native interface configuration account fields
description: Cloud native interface configuration account form and related list field descriptions.
locale: en-US
release: yokohama
product: Cloud Account Management
classification: cloud-account-management
topic_type: reference
last_updated: "2024-09-04"
reading_time_minutes: 1
breadcrumb: [Cloud Account Management reference, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud native interface configuration account fields

Cloud native interface configuration account form and related list field descriptions.

<table id="table_ul3_hgy_w1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provision mode

</td><td>

Name of the provision mode. Here it should be Cloud native interface.

</td></tr><tr><td>

Cloud provider

</td><td>

Name of the cloud provider platform. Currently supports AWS and Azure platforms.

</td></tr><tr><td>

Cloud organization

</td><td>

The cloud organization where the subscription account is to be created.

</td></tr><tr><td>

Name

</td><td>

A name to identify the configuration.

</td></tr><tr><td>

Root email \(AWS\)

</td><td>

Cloud Account Management uses an email address to generate the root email ID for newly created account.

 For example, if your root email ID is myawsaccount@example.com, the Cloud Account Management application appends a request ID to generate myawsaccount-CWSAREQ0000001@example.com.

 **Note:** To create a root email, see [Set up and verify root email in AWS](../task/aws-setup.md).

</td></tr><tr><td>

Cloud credential alias

</td><td>

Alias created to access all the Cloud APIs. The entries are populated from the CMDB records.**Note:** Only Cloud Account Management admin can configure the cloud credential alias. To configure the cloud credential alias, see [Set up AWS API configuration information in ServiceNow](../concept/configure-aws-api-key-in-servicenow.md).

</td></tr><tr><td>

Description

</td><td>

Information that can be recorded in work notes.

</td></tr></tbody>
</table>To return to the procedure, see [Create a cloud native interface account configuration](../task/create-cloud-native-interface-config.md).

**Parent Topic:**[Cloud Account Management reference](cam-reference.md)

