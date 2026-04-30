---
title: Test patterns for discovering AWS API Gateway and AWS Lambda
description: Run the horizontal and top-down discovery using Amazon AWS API Gateway \[cmdb\_ci\_cloud\_gateway\] and Amazon AWS Lambda \[cmdb\_ci\_cloud\_function\] patterns. Verify that the result is as expected.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Amazon API Gateways, Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Test patterns for discovering AWS API Gateway and AWS Lambda

Run the horizontal and top-down discovery using Amazon AWS API Gateway \[cmdb\_ci\_cloud\_gateway\] and Amazon AWS Lambda \[cmdb\_ci\_cloud\_function\] patterns. Verify that the result is as expected.

## Before you begin

Make sure that your deployment complies with all the prerequisites for [Amazon API Gateway discovery with Patterns](../concept/aws-api-gateway-discovery.md) and [AWS Lambda discovery with Patterns](../concept/aws-lambda-discovery.md).

Role required: admin

## Procedure

1.  Create an application service using the following properties for its entry point.

<table id="table_mbs_ckb_1db"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CI type

</td><td>

HTTPS

</td></tr><tr><td>

URL

</td><td>

The URL for invoking the API Gateway. Typically, the API GW has the following format:

 https://\{restapi\_id\}.execute-api.\{region\}.amazonaws.com/\{stage\_name\}/

 For example, https://k40o0l3af6.execute-api.us-east-1.amazonaws.com/prod/.

 For information about the URL format, see [https://docs.aws.amazon.com/apigateway/latest/developerguide/how-to-call-api.html](https://docs.aws.amazon.com/apigateway/latest/developerguide/how-to-call-api.html).

 **Note:** The default stage\_name parameter is **prod**.

</td></tr></tbody>
</table>2.  Click **Discover**.

    Service Mapping runs the top-down discovery using the Amazon AWS API Gateway \[cmdb\_ci\_cloud\_gateway\] pattern.

    After Service Mapping completes identifying the API Gateway configuration item \(CI\), it runs the **Connection to APIs** connection section and discovers connection to the AWS Lambda. It then runs the Amazon AWS Lambda \[cmdb\_ci\_cloud\_function\] pattern and identifies the AWS Lambda CI.

3.  After Service Mapping finishes to discover this application service, verify that it discovered and identified AWS components correctly.

    Check that the following actions happen:

    -   Service Mapping correctly resolves the URL, finds all IP addresses behind it and creates an entry point for each IP address.

        ![Verifying the result of top-down discovery](../image/testingAPIGWandLambda.png)

    -   Service Mapping identifies the AWS API Gateway and creates an application cluster for IP address.

    -   The **Properties** pane shows the properties for the AWS API Gateway: Cloud Gateway \[cmdb\_ci\_cloud\_gateway\].
    -   Service Mapping discovers the AWS Lambda connected to the application cluster for API Gateway.
    -   Service Mapping discovers the databases connected to AWS Lambda.

**Parent Topic:**[Amazon API Gateway discovery with Patterns](../concept/aws-api-gateway-discovery.md)

