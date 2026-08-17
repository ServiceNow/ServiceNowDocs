---
title: AI Service Graph Connector for Amazon
description: The AI Service Graph Connector for Amazon enables you to discover and import AI assets from your AWS environment into ServiceNow AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/aws\_0.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower \(legacy\), Enable AI experiences]
---

# AI Service Graph Connector for Amazon

The AI Service Graph Connector for Amazon enables you to discover and import AI assets from your AWS environment into ServiceNow AI Control Tower.

The connector integrates with your AWS account \(Amazon Bedrock, Amazon SageMaker, Amazon CloudWatch, and Amazon Bedrock AgentCore\) to catalog AI systems, agents, models,prompts, and tools. Usage data is automatically collected and populated into the AI Control Tower value dashboard, providing comprehensive visibility and governance of your AI operations.

## Download apps from the Store

Visit the  ServiceNow store website to download the [AI Service Graph Connector for Amazon](https://store.servicenow.com/store/app/74d7378e47a73a50cbbce551336d4356) application.

## Supported ServiceNow versions

This connector is supported on the following ServiceNow releases:

|Release|Status|
|-------|------|
|Australia|Supported|
|Zurich|Supported|
|Yokohama|Supported|

## User Roles

You must have one of the following roles assigned.

|Required Roles|
|--------------|
|sn\_ai\_disc.discovery\_admin|
|sn\_cmdb\_int\_util.sgc\_admin|

## ServiceNow Prerequisites

Complete the following setup steps once when configuring the connector for the first time.

**Note:** Updating data source access and clear cache is a prerequisite that needs to be completed only once, when setting up a new instance for the first time.

Update Data Source Access

The connector requires write permissions to the Data Source table to create data sources.

To enable data source creation:

1.  Select **Global** from the application picker.
2.  Navigate to **Application Access**.
3.  Select the **Can create**, **Can update**, and **Can delete** check boxes.
4.  Select **Update**.
5.  Switch to the connector application scope.

Clear the cached data for the Data Source and Tables.

To clear the cache:

1.  Navigate to **System Definition** &gt; **Background Scripts**.
2.  Enter the following script in the **Run Script** text box:

    ```
    GlideTableManager.invalidateTable('sys_data_source');
    GlideCacheManager.flushTable('sys_data_source');
    GlideTableManager.invalidateTable('sys_db_object');
    GlideCacheManager.flushTable('sys_db_object');
    
    ```

3.  Select **Run Script**.

    **Note:** The script might take several minutes to complete. After completion, switch to the connector application scope.


## AWS Prerequisites

**AWS prerequisites for version 1.1.0**

Complete the following steps in your Azure environment before creating an Azure Foundry connection. Configure OAuth Credentials:

The connector uses OAuth to authenticate with Azure APIs. To obtain credentials, register an application in Microsoft Entra ID. For full instructions, see, [https://learn.microsoft.com/en-us/rest/api/azure/\#register-your-client-application-with-azure-ad](https://learn.microsoft.com/en-us/rest/api/azure/#register-your-client-application-with-azure-ad)

The Azure client application requires the following roles:

-   Reader role at the subscription or resource group level to discover resources.
-   Foundry User role in the Azure AI Foundry resources.

**Note:** Starting from March 2026, ServiceNow supports the new Azure AI Foundry alongside the original Foundry. The New Foundry treats each agent version as a distinct entity.

**AWS prerequisites for version 2.0.2**

The AWS connector requires a read-only IAM user and a read-only role deployed across the accounts you want to discover. Download the CloudFormation templates from the playbook and deploy them using the AWS CloudFormation console as a Stack \(single account\) or a StackSet \(multiple accounts across the Organization\).

Before proceeding, confirm you have:

AWS Account- Active AWS account with access to the services you want to connect to.

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

Perform the AWS prerequisites:

**1. Choose your deployment scenario**

Determine how your ServiceNow IAM user will be setup in AWS:

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
</table>**2. Download the CloudFormation templates**

Deploy the following AWS CloudFormation templates based on your selected scenario:

1.  Navigate to the connector playbook, open the **Prerequisites** section.
2.  Select **Download basic scripts**. This downloads a ZIP file containing the following CloudFormation templates:
    1.  ServiceNowAictUser.yml- Required in all scenarios. Deploy in the account where the ServiceNow IAM user will reside:
        -   Management account for Scenario 1
        -   Designated account for Scenario 2
    2.  SgcAictReadOnlyAccessRole.yml- Required in all scenarios. Deploy across all member accounts via StackSet for Organization-wide discovery, or in a single target account for Standalone Mode.
    3.  SgcAictReadOnlyOrgAccessRole.yml- Required only for Scenario 2. Deploy in the Org/Management account to grant the Designated account cross-account Organization read access.
3.  Sign in to [https://console.aws.amazon.com](https://console.aws.amazon.com) using your Management account.
4.  Extract the ZIP so the template files are available on your local machine.

**3. Enable trusted access for StackSets**

Service-managed StackSets require trusted access between AWS Organizations and CloudFormation. This is a one-time setup in the Management account.

1.  Sign in to the Management account.
2.  Search for CloudFormation in the left navigation pane and select **StackSets**.
3.  If trusted access is not enabled, a banner prompts you to enable it. Select **Enable trusted access**.

    **CLI Alternative:**

    ```
    aws organizations enable-aws-service-access\
    --service-principal member.org.stacksets.cloudformation.amazonaws.com
    ```


**Note:** For more information, see the AWS documentation on [enabling trusted access with AWS Organizations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-orgs-activate-trusted-access.html).

**4. Deploy the ServiceNow IAM user \(Stack\)**

The ServiceNowAictUser.yml template creates the ServiceNow IAM user with the required read-only permissions. Deploy it as a Stack in the account where the user should reside — the Management account for Scenario 1, or the Designated Member account for Scenario 2.

1.  Sign in to the account where the user will be created.
2.  Search for CloudFormation and select **Create stack** With new resources \(standard\).
3.  Under Specify template:
    1.  Prepare template: Choose an existing template.
    2.  Template source: Upload a template file.
    3.  Select **Choose file** and upload ServiceNowAictUser.yml and select **Next**.
4.  Under **Specify stack details**:
    1.  Stack name: aict-servicenow-user.
    2.  Parameters:
        -   UserAccountType: ManagementAccount \(Scenario 1\) or DesignatedMemberAccount \(Scenario 2\)
        -   SNUserName: servicenow-aict-user
        -   MbrActRoleName: Leave the default value \(SgcAictReadOnlyAccessRole\).
    3.  Select **Next**.
5.  Under **Configure stack options**, leave the default values and select **Next**.
6.  On the **Review and create** page, scroll to the bottom and select **I acknowledge that AWS CloudFormation might create IAM resources** check box.
7.  Select **Submit**. The stack status shows CREATE\_IN\_PROGRESS, then CREATE\_COMPLETE.
8.  Open the stack, select the **Outputs** tab, and note the **ServiceNowUserARN** value.

**Note:** The IAM resources created are strictly read-only and scoped to AI Discovery APIs \(Bedrock, SageMaker, AgentCore, and CloudWatch Logs\).

**5. Deploy the Org-access role \(Scenario 2 only, Stack\)**

**Note:** This step applies only to Scenario 2 \(user in a Designated Member account\). Skip it for Scenario 1.

The SgcAictReadOnlyOrgAccessRole.yml template creates a read-only role in the Management account, scoped to Organization, Account, and Region APIs. The ServiceNow user assumes this role to enumerate the Organization.

1.  Sign in to the **Management account**.
2.  Search for CloudFormation, then select **Create stack** with new resources \(standard\).
3.  Under **Specify template**:
    1.  Prepare template: Choose an existing template.
    2.  Template source: Upload a template file.
    3.  Select **Choose file** and upload SgcAictReadOnlyOrgAccessRole.yml.
    4.  Select **Next**.
4.  Under **Specify stack details**:
    1.  Stack name: aict-org-readonly-role
    2.  Parameters:
        -   DesignatedAccountId: the 12-digit account ID where the ServiceNow user was created \(Prerequisite 4\).
        -   ServiceNowUserName: servicenow-aict-user
    3.  Select**Next**.
5.  Under **Configure stack options**, leave the default values and select **Next**.
6.  On the**Review and create** page, scroll to the bottom and select the check box **I acknowledge that AWS CloudFormation might create IAM resources**.
7.  Select **Submit** and wait for CREATE\_COMPLETE.

**Note:** This template is not needed for Scenario 1, because the user created in the Management account already has Organization permissions inline.

**6. Deploy the member-account role \(StackSet\)**

The SgcAictReadOnlyAccessRole.yml template creates the SgcAictReadOnlyAccessRole read-only role that the ServiceNow user assumes to make API calls in each member account. Deploy it as a StackSet from the Management account across all member accounts.

1.  Sign in to the **Management account**.
2.  Search for CloudFormation in the left navigation pane, select &gt; **StackSets** &gt; **Create StackSet**.
3.  Under **Permissions**, select **Service-managed permissions**.
4.  Under **Specify template**:
    1.  Prepare template: Choose an existing template.
    2.  Template source: Upload a template file.
    3.  Select **Choose file** and upload SgcAictReadOnlyAccessRole.yml.
    4.  Select **Next**.
5.  Under **Specify StackSet** details:
    1.  StackSet name: aict-member-readonly-role
    2.  Parameters:
        -   ServiceNowUserAccountId: the 12-digit account ID where the ServiceNow user was created \(Management account for Scenario 1, Designated Member account for Scenario 2\).
        -   ServiceNowUserName: servicenow-aict-user
        -   RoleName: leave default \(SgcAictReadOnlyAccessRole\)
    3.  Select **Next**.
6.  Under **Configure StackSet** options, leave the default values and select **Next**.
7.  Under **Set deployment** options:
    1.  Add stacks to stack set: Deploy new stacks
    2.  Deployment targets — select one of the following:
        -   Deploy to organization — Deploys to all accounts in the Organization
        -   Deploy to organizational units \(OUs\) — Select **Add an OU** and paste the target OU ID\(s\).
        -   For a subset of accounts within an OU, set **Account filter type** to **Intersection** and provide the specific account numbers.
    3.  Automatic deployment: Enabled — accounts added to the Organization or OU in the future automatically receive the role.
    4.  Account removal behavior: Delete stacks.
    5.  Specify regions: Add the region\(s\) matching your connector configuration \(for example, us-east-1\).
    6.  Select **Next**.
8.  On the **Review page**, select the **I acknowledge that AWS CloudFormation might create IAM resources** check box, then select **Submit**.
9.  On the **Operations** tab, monitor the StackSet operation until the status shows SUCCEEDED.

**Note:**

IAM is a global service. Although a region must be specified for the StackSet, the role created by this template is global and identical regardless of region. For more information, see the AWS documentation on [creating StackSets with service-managed permissions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-orgs-associate-stackset-with-org.html).

Standalone Mode: To validate against a single account before deploying org-wide, deploy SgcAictReadOnlyAccessRole.yml as a regular Stack \(following the Prerequisite 4\) in that one account. After validation, deploy the StackSet across all accounts.

**7. Generate the access key**

The connector requires an Access Key ID and Secret Access Key from the IAM user created in the Prerequisite 4 \(Deploy the ServiceNow IAM user \(Stack\) steps\).

1.  Sign in to the account where the ServiceNow user was created.
2.  Search for IAM, then select Users&gt; select servicenow-aict-user.

3.  Select the **Security credentials tab**, then select **Create access key**.
4.  Select **Application running outside AWS**, then select **Next**.

5.  \(Optional\) Add a description tag, then select **Create access key**.
6.  Save the credentials:

    1.  Access Key ID: AKIA...
    2.  Secret Access Key: wJal...
    The Secret Access Key is only shown only once. Download the .csv file or save the value immediately.

    **CLI Alternative:**

    ```
    aws iam create-access-key --user-name servicenow-aict-user
    ```


**Note:** An IAM user can have a maximum of two access keys. If two access keys already exist, delete one before creating a new one.

**8. Setup CloudWatch Log Group and CloudTrail**

The connector queries CloudWatch Logs to retrieve Bedrock invocation counts per agent. CloudTrail captures the Bedrock data events and delivers them to the log group. Complete this step in each member account from which you want usage data.

This step is optional- complete it only if you want agent invocation counts. Asset discovery works without it.

1.  Create the CloudWatch Log Group.
2.  Search CloudWatch → Logs → Log groups → Create log group

    1.  Log group name: /aws/bedrock/aict-invocations
    2.  Retention: 90 days \(recommended\).
    3.  Select **Create**.
    **CLI Alternative**

    ```
    # Create
    aws logs create-log-group --log-group-name /aws/bedrock/aict-invocations
     
    # Verify
    aws logs describe-log-groups --log-group-name-prefix /aws/bedrock/aict-invocations
    
    ```

    **Note:** If a log group already exists for this purpose, use its name in the connector configuration.

3.  Create an IAM Role for CloudTrail to CloudWatch Logs delivery

    CloudTrail requires permission to write events into the log group. Create a role that allows.

4.  IAM → Roles → Create role
    1.  Trusted entity type: AWS service
    2.  Service: CloudTrail
    3.  Select **Next**.
5.  Attach the following inline policy:

    ```
    {
      "Version": "2012-10-17",
      "Statement": [
        {
          "Effect": "Allow",
          "Action": [
            "logs:CreateLogStream",
            "logs:PutLogEvents"
          ],
          "Resource": "arn:aws:logs:*:*:log-group:/aws/bedrock/aict-invocations:*"
        }
      ]
    }
    
    ```

6.  Role name: CloudTrailToCloudWatchLogsRole → Create role
7.  Copy the Role ARN — required in Step 10, when configuring CloudWatch Logs delivery in the trail.
8.  Create the CloudTrail. Search CloudTrail &gt; Trails &gt; Create trail
9.  Trail settings:
    1.  Trail name: servicenow-aict-bedrock-trail
    2.  Storage location: Create a new S3 bucket or use existing.
    3.  S3 bucket name: servicenow-aict-cloudtrail-logs-&lt;account-id&gt;
10. CloudWatch Logs — Enable:
    1.  Log group: /aws/bedrock/aict-invocations
    2.  IAM role: CloudTrailToCloudWatchLogsRole \(from Step 7\)
11. Select **Next** → Events
    1.  Event type: Data events
    2.  Uncheck Management events
12. Configure data event selectors — add each of the following:

    |**Data event source**|**Event type**|
    |---------------------|--------------|
    |Bedrock Agent Alias|AWS::Bedrock::AgentAlias|
    |Bedrock Async Invoke|AWS::Bedrock::AsyncInvoke|
    |Bedrock Inline Agent|AWS::Bedrock::InvokeInlineAgent|
    |Bedrock Knowledge Base|AWS::Bedrock::KnowledgeBase|
    |Bedrock Model|AWS::Bedrock::Model|
    |Bedrock Session|AWS::Bedrock::Session|
    |Bedrock Flow Alias|AWS::Bedrock::FlowAlias|

13. Select **Next** &gt; Review &gt; Create trail

**CLI Alternative:**

```
# Create trail
aws cloudtrail create-trail \\
  --name servicenow-aict-bedrock-trail \\
  --s3-bucket-name servicenow-aict-cloudtrail-logs-<account-id> \\
  --cloud-watch-logs-log-group-arn arn:aws:logs:<region>:<account-id>:log-group:/aws/bedrock/aict-invocations \\
  --cloud-watch-logs-role-arn arn:aws:iam::<account-id>:role/CloudTrailToCloudWatchLogsRole
 
# Enable logging
aws cloudtrail start-logging --name servicenow-aict-bedrock-trail
 
# Verify trail is active
aws cloudtrail get-trail-status --name servicenow-aict-bedrock-trail

```

**Note:**

Repeat this step in each member account from which you want usage data. Note the log group name — enter it in the Log Group Names field of the connector configuration.

Bedrock data events are only logged when agents are invoked. If no invocations have occurred, the log group exists but is empty. Invocation counts populate after the first discovery run.

**9. Verify Services**

1.  Bedrock:
    1.  Search "Bedrock" → Bedrock console loads
    2.  CLI \(example\): aws bedrock list-foundation-models --region us-east-1
2.  SageMaker:
    1.  Search "SageMaker" → SageMaker console loads
    2.  CLI \(example\): aws sagemaker list-models --region us-east-1
3.  CloudWatch Logs:
    1.  Search "CloudWatch" → CloudWatch → Logs → Log groups
    2.  CLI \(example\): aws logs describe-log-groups --region us-east-1

## AWS Prerequisite troubleshooting

|**Error**|**Solution**|
|---------|------------|
|Access Denied \(creating stack/StackSet\)|Ensure your session has CloudFormation, IAM, and Organizations permissions in the relevant account.|
|Stack fails with "requires capabilities: \[CAPABILITY\_NAMED\_IAM\]"|On the Review page, select the check box acknowledging that CloudFormation may create IAM resources.|
|StackSet operation FAILED|Open the StackSet → Operations tab → view the failed stack instance. Common causes: SCP restrictions, name conflicts from a prior failed run.|
|Trusted access not enabled|Enable trusted access between AWS Organizations and CloudFormation StackSets in the Management account \(Prerequisite 3\).|
|StackSet has no deployment targets|Verify you selected Deploy to organization or provided a valid OU ID.|
|Service unavailable in region|Use us-east-1; not all regions have all services.|
|Can't see Secret Access Key|Delete the key and create a new one.|
|Log group already exists|Use the existing group; skip Prerequisite 8 or reuse the name.|
|Explicit deny in service control policy|An SCP is blocking the action on that account. Contact the Organization administrator.|

**AWS prerequisites for version 2.1.2**

To setup AWS instructions, see the [Automating AICT AWS Connector Setup Using the CloudShell Deployment Script \[KB3138431\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB3138431) article in the Now Support Knowledge BaseKB3138431

## Data Mapping

The following table lists the data sources, the staging tables, and the target tables  CMDB CI classes and non-CMDB  classes where data is stored for a  AWS  project.

<table id="table_jc1_m2r_l3c"><tbody><tr><td>

Data Source

</td><td>

Staging Table

</td><td>

Target Table

</td></tr><tr><td>

SGawsBedrockAIAssetDSUtilSNC

</td><td>

sn\_ai\_disc\_aws\_sgc\_bedrock\_ai\_asset

</td><td>

sn\_ai\_disc\_aws\_sgc\_bedrock\_ai\_system \(routes to other staging tables\)

</td></tr><tr><td>

SGawsBedrockAISystemDSUtilSNC

</td><td>

sn\_ai\_disc\_aws\_sgc\_bedrock\_ai\_system

</td><td>

alm\_ai\_system\_digital\_asset

</td></tr><tr><td>

SGawsBedrockAIModelDSUtilSNC

</td><td>

sn\_ai\_disc\_aws\_sgc\_bedrock\_ai\_model

</td><td>

alm\_ai\_model\_digital\_asset

</td></tr><tr><td>

SGawsBedrockAIToolDSUtilSNC

</td><td>

sn\_ai\_disc\_aws\_sgc\_bedrock\_ai\_tool

</td><td>

sn\_ent\_ai\_tool

</td></tr><tr><td>

SGawsBedrockAIPromptDSUtilSNC

</td><td>

sn\_ai\_disc\_aws\_sgc\_bedrock\_ai\_prompt

</td><td>

alm\_ai\_prompt\_digital\_asset

</td></tr><tr><td>

SGawsBedrockAISbcompM2mDSUtilSNC

</td><td>

sn\_ai\_disc\_aws\_sgc\_bedrock\_sbcomp\_m2m

</td><td>

sn\_ent\_ai\_system\_subcomponent\_m2m

</td></tr><tr><td>

SGawsBedrockAIUsageDSUtilSNC

</td><td>

sn\_ai\_disc\_aws\_sgc\_bedrock\_ai\_usage

</td><td>

sn\_ai\_disc\_ai\_usage

</td></tr><tr><td>

SGAgentCoreDataSourceUtil \(importAgentRuntimesByID\)

</td><td>

sn\_ai\_disc\_aws\_sgc\_agentcore\_ai\_system

</td><td>

alm\_ai\_system\_digital\_asset

</td></tr><tr><td>

SGAgentCoreDataSourceUtil \(importCodeInterpretersByID, importBrowsersByID, importTargetsByID\)

</td><td>

sn\_ai\_disc\_aws\_sgc\_agentcore\_ai\_tool

</td><td>

sn\_ent\_ai\_tool

</td></tr><tr><td>

SGAgentCoreDataSourceUtil \(getAWSAgentCoreUsage\)

</td><td>

sn\_ai\_disc\_aws\_sgc\_agentcore\_ai\_usage

</td><td>

sn\_ai\_disc\_ai\_usage

</td></tr><tr><td>

SGSageMakerAIModelDSUtilSNC

</td><td>

sn\_ai\_disc\_aws\_sgc\_sg\_awssagemaker\_model

</td><td>

alm\_ai\_model\_digital\_asset

</td></tr><tr><td>

SGSageMakerModelCardDSUtilSNC

</td><td>

sn\_ai\_disc\_aws\_sgc\_sg\_awssagemaker\_model

</td><td>

alm\_ai\_model\_digital\_asset

</td></tr></tbody>
</table>