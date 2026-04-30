---
title: Configure an Amazon Signature based Custom Algorithm
description: Generate the Amazon Signature based data needed to authenticate to a web service by running script.
locale: en-US
release: xanadu
product: Connections and Credentials
classification: connections-and-credentials
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Authentication Algorithms, Connections and Credentials, Access Management]
---

# Configure an Amazon Signature based Custom Algorithm

Generate the Amazon Signature based data needed to authenticate to a web service by running script.

## Before you begin

-   JavaScript knowledge
-   REST knowledge
-   Target web service API knowledge
-   Connection, credential, and alias knowledge
-   Role required: Developer

## About this task

Use a connection and credential alias and Amazon Signature Version 4 based algorithm for authentication.

## Procedure

1.  Navigate to **All** &gt; **Credentials &amp; Connections** &gt; **Authentication Algorithms**, and click **New**.

2.  On the form, fill in the fields.

    The database selection in the **Format** field determines which fields are available.

<table id="table_dls_tpv_sx"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of this algorithm.

</td></tr><tr><td>

Algorithm

</td><td>

Outbound request type. Select **Amazon Signature Version 4**.

</td></tr><tr><td>

Description

</td><td>

Description of what your algorithm does.

</td></tr><tr><td>

Application

</td><td>

Scope that your application runs in.

</td></tr><tr><td>

Instance Authentication Script

</td><td>

Script that you select from the Script Includes table. In case of **Amazon Signature Version 4** algorithm, choose **RequestAuthAWSV4Signer**. The scripts available are as follows:-   RequestAuthAWSV4Signer
-   RequestAuthInternal
-   RequestAuthSampleCustomSigner
-   RequestAuthTwitterSigner
 **Note:** To know more about the script click the information icon next to the field. The details of the script such as Name, API Name, Application, Accessible from, Script, and so on is displayed.

</td></tr><tr><td>

MID Authentication Script

</td><td>

Script that you select from the MID Server Script Includes \[Discovery view\] table. The scripts available are as follows:-   RequestAuthAWSV4Signer
-   RequestAuthInternal
-   RequestAuthSampleCustomSigner
-   RequestAuthTwitterSigner


</td></tr></tbody>
</table>    ![Auth Algorithm](../image/amazon-singature-based-custom-algorithm.png)

3.  Click **Update**.

4.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

5.  Click **New**.

6.  Create AWS Credentials with Authentication Algorithm.

    In this case **AWS Auth alg**.

7.  Specify the following:

    -   Name
    -   Active
    -   Access Key ID
    -   Secret Access Key
    -   Credential alias
    -   Authentication Algorithm
    ![AWS Credentials](../image/amazon-credentials.png)

8.  Click **Update**.


## Result

Based on the selected scripts and authentication algorithm, the configured credentials \(**Access Key ID** and **Secret Access Key**\) or user's credentials \(**Access Key ID**, **Secret Access Key**, and **Session Token**\) generates a Amazon V4 signature that is sent as outbound request from ServiceNow to the provider \(in this case AWS\).

## REST step with AWS

**Note:** Amazon V4 signature based authentication can also be used from Script background.

Action: Get AWS Regions

Input REST step with AWS as follows:

-   **Credentials Alias**: The alias that is created for AWS.
-   **Base URL**: Base URL details from AWS.
-   **HTTPS Method**: In this case it is GET method.
-   **Query Parameters**: **Action** as **DescribeRegions**.

![GET AWS Region](../image/aws-regions-get.png)

You can test the action, the associated regions are displayed. The response body is as follows:

![Code Snippet sample](../image/response-body-aws.png)

Amazon V4 is defined with standard set of algorithm that supports authentication mechanism. This algorithm when used adds the signature as authorization header for authentication \(HTTP request\) using REST step.

