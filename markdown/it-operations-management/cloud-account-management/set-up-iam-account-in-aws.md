---
title: Set up an Identity Access Manager account for a ServiceNow user in AWS
description: AWSCreate an AWS CloudFormation Identity Access Manager \(IAM\) user in the management account using the CloudFormation template \(CFT\) so you can manage multiple AWS accounts with a centralized IAM user.
locale: en-US
release: zurich
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Setting up AWS cloud, Configuring cloud providers, Configure, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Set up an Identity Access Manager account for a ServiceNow user in AWS

AWSCreate an AWS CloudFormation Identity Access Manager \(IAM\) user in the management account using the CloudFormation template \(CFT\) so you can manage multiple AWS accounts with a centralized IAM user.

## Before you begin

Ensure that the target user account has the required AWS IAM permissions. For more information, see [About Amazon Web Services API permissions](about-aws-api-permissions.md).

Role required: AWS admin.

## Procedure

1.  Log in to the AWS Management console.

2.  Access the CloudFormation console by entering `CloudFormation` in the search bar and selecting it.

3.  On the CloudFormation console, select **Create Stack**.

    A stack is a collection of AWS resources that you manage as a single unit.

4.  Copy the CloudFormation template \(CFT\) code into a file with a `.yml` extension and save the file.

    ```
    AWSTemplateFormatVersion: '2010-09-09'
    Description: This script is executed in Management Account where the  ServiceNow user is created.
    
    Metadata:
      AWS::CloudFormation::Interface:
        ParameterGroups:
          - Label:
              default: User Credentials
            Parameters:
              - SNUserName
        ParameterLabels:
          SNUserName:
            default: User Name
    
    Parameters:
      SNUserName:
        Type: String
        Description: User name for CW Service Account user
        MinLength: '6'
        MaxLength: '15'
        ConstraintDescription: The username must be between 6 and 15 characters
    
    Resources:
      SnowCWMemberAccountAccessGroup:
        Type: 'AWS::IAM::Group'
        Properties:
          GroupName: SnowCWMemberAccountAccessGroup
    
      SnowCWAccountAccessPolicy:
        Type: 'AWS::IAM::Policy'
        Properties:
          PolicyName: SnowCWAccountAccessPolicy
          PolicyDocument:
            Statement:
              - Sid: ServiceNowCWUserAccess
                Effect: Allow
                Action:
                  - 'organizations:ListRoots'
                  - 'organizations:ListTagsForResource'
                  - 'organizations:DescribeAccount'
                  - 'organizations:CreateAccount'
                  - 'organizations:ListAWSServiceAccessForOrganization'
                  - 'organizations:TagResource'
                  - 'organizations:ListAccounts'
                  - 'organizations:ListRoots'
                  - 'organizations:ListTagsForResource'
                  - 'organizations:DescribeAccount'
                  - 'organizations:CreateAccount'
                  - 'organizations:ListAWSServiceAccessForOrganization'
                  - 'organizations:TagResource'
                  - 'organizations:ListAccounts'
                  - 'organizations:CloseAccount'
                  - 'organizations:DescribeOrganization'
                  - 'organizations:DescribeOrganizationalUnit'
                  - 'organizations:ListParents'
                  - 'organizations:ListOrganizationalUnitsForParent'
                  - 'organizations:MoveAccount'
                  - 'organizations:DescribeCreateAccountStatus'
                  - 'organizations:AttachPolicy'
                  - 'organizations:DescribePolicy'
                  - 'organizations:ListAccounts'
                  - 'budgets:CreateBudgetAction'
                  - 'budgets:ModifyBudget'
                  - 'budgets:ViewBudget'
                  - 'budgets:ListTagsForResource'
                  - 'iam:GetAccountSummary'
                  - 'iam:GetAccountPasswordPolicy'
                  - 'budgets:DescribeBudgetAction'
                  - 'iam:ListAccountAliases'
                  - 'sts:AssumeRole'
                  - 'iam:GetRole'
                  - 'iam:ListAccountAliases'
                  - 'iam:GetAccountPasswordPolicy'
                  - 'organizations:DetachPolicy'
                  - 'iam:GetAccountAuthorizationDetails'              
                Resource: '*'
          Groups:
            - !Ref SnowCWMemberAccountAccessGroup
    
      CreateServicenowUser:
        Type: 'AWS::IAM::User'
        Properties:
          Path: /
          UserName: !Ref SNUserName
      AddSnowUserToSnowCWMemberAccountAccessGroup:
        Type: 'AWS::IAM::UserToGroupAddition'
        Properties:
          GroupName: SnowCWMemberAccountAccessGroup
          Users:
            - !Ref SNUserName
        DependsOn: CreateServicenowUser
    
    Outputs:
      ServiceNowUserARN:
        Description: ARN of ServiceNow user
        Value: !GetAtt 
          - CreateServicenowUser
          - Arn
    
      ServiceNowUser:
        Description: ServiceNow user
        Value: !Ref SNUserName
    
    ```

5.  On the **Create Stack** page, select **Choose an existing template** &gt; **Upload a template file** &gt; **Choose file** to choose a template file from your local computer.

6.  Select **Next** to continue and to validate the template.

7.  On the **Specify stack details** page, enter a name for the template in the **Stack name** field.

    Note the following format requirements for a stack name:

    -   Can contain only case-sensitive alphanumeric characters and hyphens
    -   Must start with an alphabetic character
    -   Can't be longer than 128 characters
8.  In the **User Name** field, enter a Cloud Account Management service account user name.

9.  Select **Next**.

10. On the **Configure stack options** page, select the **I acknowledge that AWS CloudFormation might create IAM resources with custom names** check box and select **Next**.

11. On the **Review and create** page, select **Submit** to launch your stack.

    The IAM account gets created.

12. Add security credentials.

    1.  Select **Resources**.

    2.  Select the user name link.

    3.  In the Access Keys section, select **Create access key**.

    4.  On the **Access key best practices &amp; alternatives** page, choose the **Third-party service** option.

        This access key provides access for a third-party application or service that monitors or manages your AWS resources.

    5.  Select the **I understand the above recommendation and want to proceed to create an access key** check box and select **Next**.

    6.  Select **Create access key**.

    7.  On the **Review access keys** page, download the access key file and select **Done**.

        **Note:** Share the access key and secret key with the Terraform admin and ServiceNow AI Platform admin.


## What to do next

[Set up suspension of an AWS account using service control policy](../task/configure-suspension-policy.md)

