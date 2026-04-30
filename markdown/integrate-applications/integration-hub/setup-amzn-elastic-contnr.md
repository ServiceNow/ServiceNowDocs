---
title: Set up the Amazon Elastic Container Service spoke
description: Integrate the ServiceNow instance and Amazon Elastic Container Service account by using the AWS credentials to authenticate ServiceNow requests.Create a credential record for the Amazon Elastic Container Service account. The Amazon Elastic Container Service spoke connection and credential alias uses these credentials to authorize actions.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Amazon Elastic Container Service Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Amazon Elastic Container Service spoke

Integrate the ServiceNow instance and Amazon Elastic Container Service account by using the AWS credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Amazon Elastic Container Service spoke.
-   Role required: admin

## Create a credential record for the Amazon Elastic Container Service spoke

Create a credential record for the Amazon Elastic Container Service account. The Amazon Elastic Container Service spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays this message: `What type of Credentials would you like to create?`

3.  Select **AWS Credentials**.

4.  On the form, fill these values.

<table id="table_cj5_pjb_2nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, `Amazon ECS Cred`.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the credential record.

</td></tr><tr><td>

Access Key ID

</td><td>

Access Key ID of the user with full access to Amazon Elastic Container Service.

</td></tr><tr><td>

Secret Access Key

</td><td>

Secret Access Key of the user with full access to Amazon Elastic Container Service.

</td></tr><tr><td>

Authentication Algorithm

</td><td>

Custom authentication algorithm for outbound signing requests. Select **AmazonECSAuthAlgo**.**Note:** Users are cautioned against directly modifying the default authentication algorithm.

</td></tr><tr><td>

Credential alias

</td><td>

Credential alias associated with the spoke.

</td></tr></tbody>
</table>5.  Click **Submit**.


