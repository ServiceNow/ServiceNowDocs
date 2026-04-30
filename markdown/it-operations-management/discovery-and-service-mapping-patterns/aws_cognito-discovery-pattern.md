---
title: Amazon Cognito discovery
description: The ServiceNow Discovery and Service Mapping applications use the Amazon AWS Cognito pattern to provide authentication, authorization, and user management functions for AWS customers. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Amazon Cognito discovery

The ServiceNow Discovery and Service Mapping applications use the Amazon AWS Cognito pattern to provide authentication, authorization, and user management functions for AWS customers. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

You can use this pattern on the ServiceNow AI Platform using London Patch 8, Madrid Patch 2, or later releases.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **User permissions**

    Provide user with read-only permission to run the following API:

    -   https://cognito-idp.&lt;region&gt;.amazonaws.com
    -   Method: POST
    -   Body: \{\\"MaxResults\\": 10\}
    -   Headers: X-Amz-Target:AWSCognitoIdentityProviderService.ListUserPools,Content-Type:application/x-amz-json-1.0
-   **AWS Credentials**

    On your instance, configure credentials of type **AWS Credentials** and set to **Active**.

-   **Cloud service account**

    On your instance, configure the cloud service account of type **AWS Datacenter** and set to **AWS account ID**. Use the credentials defined in the preceding **AWS Credentials**.

-   **Discovery schedule**

    Create a cloud application schedule for discovering AWS Cognito and configure the attributes. Set Discovery to **Cloud application**.

-   **Execution pattern**

    Create and define the serverless execution pattern for cloud application discovery.

    1.  Create new **Cloud Execution Patterns**.
    2.  Define **Name**.
    3.  Verify that **Active** is true.
    4.  Verify that **Domain** is global.
    5.  Choose the **AWS pattern** you want to run.
    6.  Create multiple records if you want to run more than one pattern.
-   **Discovery schedule for full AWS discovery**

    Create a discovery schedule from your **Cloud service account** created in the earlier procedure.

    1.  Click on **Discover Datacenter** and wait for it to finish.
    2.  Click **Create Discovery Schedule**.
    3.  This new schedule is created under the Discovery Schedule and runs all AWS patterns.

## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

**Note:** You can test the AWS REST APIs using Postman API platform. For more information, see the [How to test AWS REST API using POSTMAN \[KB0782183\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0782183) article in the Now Support Knowledge Base.

## Data collected by Discovery and Service Mapping during horizontal and top-down discovery

The AWS Cognito pattern collects data.

|Field|Description|
|-----|-----------|
|Main CI: cmdb\_ci\_cloud\_authentication|
|name|A descriptive name used to identify the user pool.|
|object\_id|This is equal to the account\_id and used by IRE identification rules.|
|Fqdn|Example of an ARN: arn:aws:cognito-idp:eu-west-1:751200741520:userpool/eu-west-1\_fim5E2mix|

Tags are also being collected by an extension section that runs following the pattern. The tagging API for AWS specifies the resource type Cognito.

|Field|Description|
|-----|-----------|
|cmdb\_key\_value|
|key|The actual tag key.|
|value|The tag value.|
|configuration\_item|The unique resource ID \(ARN\) that identifies the resource in the AWS console.|

## CI relationships

The AWS Cognito pattern creates the following CI relationship.

|CI|Relationship|CI|
|---|------------|---|
|Cloud authentication \[cmdb\_ci\_cloud\_authentication\]|Hosts:Hosted on|Logical datacenter \[cmdb\_ci\_logical\_datacenter\]|

## Troubleshooting

If the mapping process does not proceed as you expected, follow the following suggestions.

<table id="table_ggn_ypj_yhb"><thead><tr><th>

Symptom

</th><th>

Cause

</th><th>

Solution

</th></tr></thead><tbody><tr><td>

Discovery fails. The discovery message contains the information about an error caused by the REST timeout.

</td><td>

There are many CIs sending the REST call response in the deployment. The MID Server cannot process the REST call response without exceeding the time limit controlled by the **mid.sa.cloud.request\_timeout** parameter.

</td><td>

By default, the **mid.sa.cloud.request\_timeout** parameter is set to 30000 milliseconds. Increase the value of this parameter on the relevant MID Server and run discovery again.

**Note:** If the **Configuration Parameters** related list for the relevant MID Server does not show this parameter, you may need to add it.

</td></tr><tr><td>

Pattern Designer fails during a debug session. The Pattern Designer message contains information about an error caused by a timeout.

</td><td>

The Pattern Designer fails because of a timeout during pattern debugging \(and not during discovery\).

</td><td>

By default, the **sa.debugger.max\_timeout**parameter is set to 240 seconds.Increase the value of this parameter on the relevant MID Server.

</td></tr></tbody>
</table>**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

