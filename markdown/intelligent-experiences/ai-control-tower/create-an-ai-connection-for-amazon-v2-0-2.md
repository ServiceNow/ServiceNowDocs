---
title: Create an AI connection for Amazon \(v2.0.2\)
description: Create an AI connection for Amazon in AI Control Tower using the AI Service Graph Connector for Amazon \(version 2.0.2\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/create-an-ai-connection-for-amazon-v2-0-2.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-07-05"
reading_time_minutes: 5
breadcrumb: [AWS, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# Create an AI connection for Amazon \(v2.0.2\)

Create an AI connection for Amazon in AI Control Tower using the AI Service Graph Connector for Amazon \(version 2.0.2\).

## AWS Prerequisites

The AWS connector requires a read-only IAM user and a read-only role deployed across the accounts you want to discover. Download the CloudFormation templates from the playbook and deploy them using the AWS CloudFormation console — as a stack \(single account\) or a Stackset \(multiple accounts across the Organization\).

Before proceeding, confirm you have:

AWS Account- Active AWS account with access to the services you want to connect to.

Choose your Deployment Scenario

Determine how your ServiceNow IAM user will b setup in AWS:

1.  Scenario 1- Management Account: The ServiceNow IAM user is created directly in the AWS Org/Management account.
2.  Scenario 2- Delegated Member Account: The ServiceNow IAM user is created in a dedicated member account, with a cross-account role in the Management account for Organizational-level access.
3.  Standalone Mode: Available in both scenarios. Use this to test discovery against a single AWS account before rolling out to the full organization.

Templates required per scenario

<table id="table_xcn_hfy_yjc"><tbody><tr><td>

Template

</td><td>

Deployed as

</td><td>

Scenario 1

</td><td>

Scenario 2

</td></tr><tr><td>

ServiceNowAictUser.yml

</td><td>

Stack

</td><td>

✔ \(Management account\)

</td><td>

✔ \(Designated Member account\)

</td></tr><tr><td>

SgcAictReadOnlyAccessRole.yml

</td><td>

StackSet

</td><td>

✔ \(all member accounts\)

</td><td>

✔ \(all member accounts\)

</td></tr><tr><td>

SgcAictReadOnlyOrgAccessRole.yml

</td><td>

Stack

</td><td>

—

</td><td>

✔ \(Management account\)

</td></tr></tbody>
</table>CloudFormation Templates

Deploy the following AWS CloudFormation templates based on your chosen scenario:

-   ServiceNowAictUser.yml- Required in all scenarios. Deploy in the account where the ServiceNow IAM user will reside:
    -   Management account for Scenario 1
    -   Designated account for Scenario 2
-   SgcAictReadOnlyAccessRole.yml- Required in all scenarios. Deploy across all member accounts via StackSet for Organization-wide discovery, or in a single target account for Standalone Mode.
-   SgcAictReadOnlyOrgAccessRole.yml- Required only for Scenario 2. Deploy in the Org/Management account to grant the Designated account cross-account Organization read access.
-   Sign in to [https://console.aws.amazon.com](https://console.aws.amazon.com) with your Management account.

    Extract the ZIP so the template files are available on your local machine.


Required IAM permissions

The IAM roles created by the templates earlier grant read-only access to the following services:

-   Amazon Bedrock
-   Amazon SageMaker
-   Amazon CloudWatch Logs
-   Amazon Bedrock AgentCore
-   AWS Organizations
-   Amazon EC2

Pre-Deployment Checklist

Before deploying any templates, confirm the following:

You have AWS CloudFormation Stack and StackSet deployment permissions in the relevant accounts.

Target member accounts have Amazon Bedrock, SageMaker, and/or AgentCore enabled- accounts without these services will return 403 errors during discovery.

If using Standalone Mode, confirm the target account ID where SgAictReadOnlyAccessRole.yml will be deployed.

If using StackSet deployment, confirm that Automatic Deployment is enabled so newly created accounts are covered automatically.

The default role name across all templates is SgAictReadOnlyAccessRole. If your organization requires a different naming convention, update it consistently across all templates and in the ServiceNow connector configuration before deployment.

Download the CloudFormation templates

Navigate to Prerequisites section in the connector playbook.

Select Download basic scripts to download CloudFormation templates.

-   ServiceNowAictUser.yml — Creates the ServiceNow IAM user.
-   SgcAictReadOnlyAccessRole.yml — creates the read-only role in member accounts.
-   SgcAictReadOnlyOrgAccessRole.yml — creates the Org-access role in the Management account \(Scenario 2 only\).

Log in to Amazon console with your Management account and extract the zip so the template files are available on your local machine.

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **Al Control Tower** &gt; **Configurations** &gt; **AI connections**.

2.  Select **AWS** from the available connectors and then select **Create connection**.

3.  Review setup instructions page displays.

    **Note:** Verify to follow all the prerequisite steps.

4.  Select Download basic scripts.

    **Note:** Download the basic scripts and select the check box.

5.  Select **Continue**.

    Setup page appears.

6.  Select Source systems.

7.  Choose the AWS services that you want to integrate with ServiceNow.

    -   Amazon Bedrock
    -   Amazon SageMaker
    -   Amazon Bedrock AgentCore
8.  Select **Submit**.

9.  Enter the details on Configure Amazon Bedrock:

    1.  Enter the **Connection Name**.

    2.  Enter the **Access Key ID**.

    3.  Enter the **Secret Access Key**.

    4.  Enter the **AWS Regions**

    5.  Enter the **Management Account ID**.

    6.  Enter the **Standalone Account ID**.

    7.  Enter the **STS Assume Role**.

    8.  Select **Create and test connection**.

        A banner appears displaying Connection verified.

    9.  Select **Continue**.

10. Configure Amazon Bedrock import schedule:

    1.  Open a parent schedule import.

    2.  Select the Active check box.

    3.  Select Run according to your preference.

    4.  To run frequency by demand, select **Execute now**.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    5.  Select **Continue**.

11. Enter the details on Configure Amazon CloudWatch logs:

    1.  Enter the **Connection Name**.

    2.  Enter the **Secret Key**.

    3.  Enter the **Management Account ID**.

    4.  Enter the **STS Assume Role**.

    5.  Enter the **Access Key**.

    6.  Enter the **AWS Regions**.

    7.  Enter the **Standalone Account ID**.

    8.  Enter the **Log Group Names**.

    9.  Select **Create and test connection**.

        A banner appears displaying Connection verified.

    10. Select **Continue**.

12. Configure Amazon CloudWatch logs import schedules:

    1.  Open a parent schedule import.

    2.  Select the Active check box.

    3.  Select Run according to your preference.

    4.  To run frequency by demand, select **Execute Now**.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    5.  Select **Continue**.

13. Enter the details on Configure Amazon SageMaker:

    1.  Enter the **Connection Name**.

    2.  Enter the **Access Key ID**.

    3.  Enter the **Secret Access Key**.

    4.  Enter the **AWS Regions**.

    5.  Enter the **Management Account ID**.

    6.  Enter the**STS Assume Role**.

    7.  Select **Create and test connection**.

        A banner appears displaying Connection verified.

    8.  Select **Continue**.

14. Configure Amazon Sagemaker import schedule:

    1.  Open a parent schedule import.

    2.  Select the Active check box.

    3.  Select Run according to your preference.

    4.  To run frequency by demand, select **Execute Now**.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    5.  Select **Continue**.

15. Enter the details on Configure Amazon Bedrock AgentCore:

    1.  Enter the **Connection Name**.

    2.  Enter the **Secret Key**.

    3.  Enter the **Management Account ID**.

    4.  Enter the **STS Assume Role**.

    5.  Enter the **Access Key**.

    6.  Enter the **AWS Regions**.

    7.  Enter the **Standalone Account ID**.

    8.  Enter the **Log Group Names**.

    9.  Select **Create and test connection**.

        A banner appears displaying Connection verified.

    10. Select **Continue**.

16. Configure Amazon Bedrock AgentCore import schedule:

    1.  Open a parent schedule import.

    2.  Select the Active check box.

    3.  Select Run according to your preference.

    4.  To run frequency by demand, select **Execute Now**.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    5.  Select **Continue**.


## Result

Select **View all connections** to review the connection details. The created connection appears in the Installed connections list.

