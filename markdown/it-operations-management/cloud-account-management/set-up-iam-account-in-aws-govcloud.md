---
title: Set up an Identity Access Manager in AWS GovCloud
description: Create AWS CloudFormation Identity Access Manager \(IAM\) resources for three AWS account types in the management account using the CloudFormation templates \(CFT\) to integrate ServiceNow Cloud Account management \(CAM\) with AWS GovCloud.
locale: en-US
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 7
breadcrumb: [Setting up AWS cloud, Configuring cloud providers, Configuring Cloud Account Management, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Set up an Identity Access Manager in AWS GovCloud

Create AWS CloudFormation Identity Access Manager \(IAM\) resources for three AWS account types in the management account using the CloudFormation templates \(CFT\) to integrate ServiceNow Cloud Account management \(CAM\) with AWS GovCloud.

## Before you begin

Verify that the target user account has the required AWS IAM permissions. For more information, see [About Amazon Web Services API permissions](../concept/about-aws-api-permissions.md).

**Note:** Always follow your organization's security policies when implementing IAM permissions.

Role required: AWS admin

## About this task

AWS GovCloud accounts are always linked to commercial accounts, which means IAM resources must be created across three AWS account types:

-   AWS Commercial Management Account: The standard AWS account that links to GovCloud.
-   AWS GovCloud Root Management Account: The main account in the GovCloud environment.
-   AWS GovCloud Organization Management Account: The account for managing organization resources in the GovCloud environment.

## Procedure

1.  Copy each CloudFormation template \(CFT\) code into different files with a `.yml` extension and save the files.

2.  Log in to the AWS Management console using your root user credentials.

3.  Follow the steps to execute each script in sequence.

    1.  **AWS Commercial Management Account** CFT script

        1.  Log in to the Commercial AWS console.
        2.  Access the CloudFormation console by entering `CloudFormation` in the search bar and selecting it.
        3.  On the CloudFormation console, select **Create Stack** &gt; **Choose an existing template** &gt; **Upload a template file** &gt; **Choose file** to choose a template file from your local computer.

            A stack is a collection of AWS resources that you can manage as a single unit.

        4.  Use the saved Commercial CFT script and set the `SNUserName` parameter.
        5.  Record the output parameters: `SNUserARN` and `SNUser`.
        ```
        AWSTemplateFormatVersion: '2010-09-09'
        Description: This script creates a ServiceNow user in the AWS Commercial Management Account for Cloud Account Management (CAM) integration.
        
        Metadata:
          AWS::CloudFormation::Interface:
            ParameterGroups:
              - Label:
                  default: User Credentials
                Parameters:
                  - SNUserName
            ParameterLabels:
              SNUserName:
                default: User Name in the AWS Commercial environment
        
        Parameters:
          SNUserName:
            Type: String
            Description: User name for ServiceNow Cloud Workspace application in AWS Commercial Environment
            MinLength: '6'
            MaxLength: '15'
            ConstraintDescription: The username must be between 6 and 15 characters
        
        Resources:
          # AWS Commercial Resources
          SnowCWMemberAccountAccessGroup:
            Type: 'AWS::IAM::Group'
            Properties:
              GroupName: SnowCWMemberAccountAccessGroup
            Description: IAM Group for ServiceNow Cloud Workspace users with permissions to manage AWS Organizations
        
          SnowCWAccountAccessPolicy:
            Type: 'AWS::IAM::Policy'
            Properties:
              PolicyName: SnowCWAccountAccessPolicy
              PolicyDocument:
                Version: '2012-10-17'
                Statement:
                  # Create Account Workflow Permissions
                  - Sid: ServiceNowCreateAccountAccess
                    Effect: Allow
                    Action:
                      - 'budgets:CreateBudgetAction'
                      - 'budgets:DescribeBudgetAction'
                      - 'organizations:CreateGovCloudAccount'
                      - 'organizations:DescribeCreateAccountStatus'
                      - 'organizations:MoveAccount'
                      - 'organizations:TagResource'
                      - 'organizations:ListRoots'
                    Resource: '*'
                  # Account Management Workflow Permissions
                  - Sid: ServiceNowAccountManagementAccess
                    Effect: Allow
                    Action:
                      - 'budgets:ListTagsForResource'
                      - 'budgets:ModifyBudget'
                      - 'budgets:ViewBudget'
                      - 'iam:GetAccountPasswordPolicy'
                      - 'iam:GetAccountSummary'
                      - 'iam:GetRole'
                      - 'iam:ListAccountAliases'
                      - 'organizations:AttachPolicy'
                      - 'organizations:DescribePolicy'
                      - 'organizations:DetachPolicy'
                      - 'sts:AssumeRole'
                    Resource: '*'
                  # Discovery Workflow Permissions
                  - Sid: ServiceNowDiscoveryAccess
                    Effect: Allow
                    Action:
                      - 'organizations:DescribeAccount'
                      - 'organizations:DescribeOrganization'
                      - 'organizations:DescribeOrganizationalUnit'
                      - 'organizations:ListAccounts'
                      - 'organizations:ListAWSServiceAccessForOrganization'
                      - 'organizations:ListOrganizationalUnitsForParent'
                      - 'organizations:ListParents'
                      - 'organizations:ListRoots'
                      - 'organizations:ListTagsForResource'
                    Resource: '*'
              Groups:
                - !Ref SnowCWMemberAccountAccessGroup
            Description: Policy that grants permissions required for ServiceNow CAM in the AWS Commercial environment
        
          CreateServicenowUser:
            Type: 'AWS::IAM::User'
            Properties:
              Path: /
              UserName: !Ref SNUserName
              Tags:
                - Key: Purpose
                  Value: ServiceNowCAMIntegration
            Description: IAM user for ServiceNow CAM integration with AWS Commercial environment
        
          AddSnowUserToSnowCWMemberAccountAccessGroup:
            Type: 'AWS::IAM::UserToGroupAddition'
            Properties:
              GroupName: SnowCWMemberAccountAccessGroup
              Users:
                - !Ref SNUserName
            DependsOn: CreateServicenowUser
            Description: Adds the ServiceNow user to the access group
        
        Outputs:
          SNUserARN:
            Description: ARN of ServiceNow user in AWS Commercial environment
            Value: !GetAtt CreateServicenowUser.Arn
        
          SNUser:
            Description: Username of the created ServiceNow user in AWS Commercial environment
            Value: !Ref SNUserName
        ```

    2.  **AWS GovCloud Root Management Account** CFT script

        1.  Log in to the GovCloud AWS console.
        2.  Access the CloudFormation console by entering `CloudFormation` in the search bar and selecting it.
        3.  On the CloudFormation console, select **Create Stack** &gt; **Choose an existing template** &gt; **Upload a template file** &gt; **Choose file** to choose a template file from your local computer.
        4.  Use the saved GovCloud root CFT script and set the `SNGovUserName` parameter.
        5.  Record the output parameters: `SNGovUserARN` and `SNGovUser`.
        **Note:**

        For simplicity, this template uses a wildcard \(\*\) in the Resource ARN for the SnowCWGovCloudUserPolicy, enabling the ServiceNow user to assume the role in any GovCloud account. While this works functionally, it grants more permissions than necessary.

        For production environments:

        -   Add a parameter for the organization account ID: `OrgAccountId: Type: String`
        -   Update the Resource field:

            ```
            Resource: !Sub
                  'arn:aws-us-gov:iam::${OrgAccountId}:role/ServiceNowGovCrossAccountRole'
            ```

        -   For working with multiple accounts, see [CloudFormation Parameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html) and [Using CommaDelimitedList](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html#parameters-section-structure-properties-type)
        -   Review [AWS IAM Best Practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html) for more guidance on securing IAM policies
        ```
        AWSTemplateFormatVersion: '2010-09-09'
        Description: This script creates a ServiceNow user in the AWS GovCloud Management Account for Cloud Account Management (CAM) integration.
        
        Metadata:
          AWS::CloudFormation::Interface:
            ParameterGroups:
              - Label:
                  default: User Credentials
                Parameters:
                  - SNGovUserName
            ParameterLabels:
              SNGovUserName:
                default: AWS User Name in the GovCloud environment
        
        Parameters:
          SNGovUserName:
            Type: String
            Description: User name for ServiceNow Cloud Workspace application in AWS GovCloud Environment
            MinLength: '6'
            MaxLength: '15'
            ConstraintDescription: The username must be between 6 and 15 characters
        
        Resources:
          # AWS GovCloud Resources
          SnowCWGovCloudAccessGroup:
            Type: 'AWS::IAM::Group'
            Properties:
              GroupName: SnowCWGovCloudAccessGroup
            Description: IAM Group for ServiceNow Cloud Workspace users in AWS GovCloud environment
        
          CreateGovCloudServicenowUser:
            Type: 'AWS::IAM::User'
            Properties:
              Path: /
              UserName: !Ref SNGovUserName
              Tags:
                - Key: Purpose
                  Value: ServiceNowCAMIntegration
            Description: IAM user for ServiceNow CAM integration with AWS GovCloud environment
        
          SnowCWGovCloudUserPolicy:
            Type: 'AWS::IAM::Policy'
            Properties:
              PolicyName: SnowCWGovCloudUserPolicy
              PolicyDocument:
                Version: '2012-10-17'
                Statement:
                  - Effect: Allow
                    Action: 'sts:AssumeRole'
                    Resource: 'arn:aws-us-gov:iam::*:role/ServiceNowGovCrossAccountRole'
                  - Effect: Allow
                    Action: 'sts:AssumeRole'
                    Resource: 'arn:aws-us-gov:iam::*:role/OrganizationAccountAccessRole'
              Groups:
                - !Ref SnowCWGovCloudAccessGroup
            Description: Policy that grants basic permissions and ability to assume the cross-account role
        
          AddSnowUserToSnowCWGovCloudAccessGroup:
            Type: 'AWS::IAM::UserToGroupAddition'
            Properties:
              GroupName: SnowCWGovCloudAccessGroup
              Users:
                - !Ref SNGovUserName
            DependsOn:
              - CreateGovCloudServicenowUser
              - SnowCWGovCloudAccessGroup
            Description: Adds the ServiceNow GovCloud user to the access group
        
        Outputs:
          SNGovUserARN:
            Description: ARN of ServiceNow user in AWS GovCloud environment
            Value: !GetAtt CreateGovCloudServicenowUser.Arn
        
          SNGovUser:
            Description: Username of the created ServiceNow user in AWS GovCloud environment
            Value: !Ref SNGovUserName
        ```

    3.  **AWS GovCloud Organization Management Account** CFT script

        1.  Log in to the GovCloud Organization AWS console.
        2.  Access the CloudFormation console by entering and selecting `CloudFormation` in the search bar.
        3.  On the CloudFormation console, select **Create Stack** &gt; **Choose an existing template** &gt; **Upload a template file** &gt; **Choose file** to choose a template file from your local computer.
        4.  Use the saved GovCloud Organization CFT script and set the `SNGovUserARN` parameter to the output recorded from the **AWS GovCloud Root Management Account** CFT script.
        5.  Record the output parameter: `RoleARN`.
        ```
        AWSTemplateFormatVersion: '2010-09-09'
        Description: This template creates the ServiceNowGovCrossAccountRole in the AWS Organization Management Account for ServiceNow CAM integration.
        
        Metadata:
          AWS::CloudFormation::Interface:
            ParameterGroups:
              - Label:
                  default: Role Configuration
                Parameters:
                  - SNGovUserARN
            ParameterLabels:
              SNGovUserARN:
                default: ServiceNow GovCloud User ARN
        
        Parameters:
          SNGovUserARN:
            Type: String
            Description: ARN of the ServiceNow GovCloud user that will assume this role
            AllowedPattern: '^arn:aws(-[a-z0-9-]+)?:iam::[0-9]{12}:user/.*$'
            ConstraintDescription: Must be a valid AWS IAM user ARN
        
        Resources:
          ServiceNowGovCrossAccountRole:
            Type: 'AWS::IAM::Role'
            Properties:
              RoleName: ServiceNowGovCrossAccountRole
              Description: Role used by ServiceNow CAM for cross-account operations in AWS GovCloud
              AssumeRolePolicyDocument:
                Version: '2012-10-17'
                Statement:
                  - Effect: Allow
                    Principal:
                      AWS: !Ref SNGovUserARN
                    Action: 'sts:AssumeRole'
              Policies:
                - PolicyName: ServiceNowGovCloudPolicy
                  PolicyDocument:
                    Version: '2012-10-17'
                    Statement:
                      # Create Account Workflow Permissions
                      - Sid: ServiceNowGovCreateAccountAccess
                        Effect: Allow
                        Action:
                          - 'organizations:InviteAccountToOrganization'
                          - 'organizations:ListRoots'
                          - 'organizations:MoveAccount'
                          - 'organizations:TagResource'
                        Resource: '*'
                      # Account Management Workflow Permissions
                      - Sid: ServiceNowGovAccountManagementAccess
                        Effect: Allow
                        Action:
                          - 'iam:GetAccountAuthorizationDetails'
                          - 'iam:GetAccountPasswordPolicy'
                          - 'iam:GetAccountSummary'
                          - 'iam:GetRole'
                          - 'iam:ListAccountAliases'
                          - 'organizations:AttachPolicy'
                          - 'organizations:DescribePolicy'
                          - 'organizations:DetachPolicy'
                        Resource: '*'
                      # Discovery Workflow Permissions
                      - Sid: ServiceNowGovDiscoveryAccess
                        Effect: Allow
                        Action:
                          - 'ec2:DescribeRegions'
                          - 'organizations:DescribeAccount'
                          - 'organizations:DescribeOrganization'
                          - 'organizations:DescribeOrganizationalUnit'
                          - 'organizations:ListAccounts'
                          - 'organizations:ListAWSServiceAccessForOrganization'
                          - 'organizations:ListOrganizationalUnitsForParent'
                          - 'organizations:ListParents'
                          - 'organizations:ListRoots'
                          - 'organizations:ListTagsForResource'
                        Resource: '*'
        
        Outputs:
          RoleARN:
            Description: ARN of the ServiceNowGovCrossAccountRole
            Value: !GetAtt ServiceNowGovCrossAccountRole.Arn
        ```

4.  Select **Next** to continue and validate the template.

5.  On the **Specify stack details** page, enter a name for the template in the **Stack name** field.

    A stack name:

    -   Can contain only case-sensitive alphanumeric characters and hyphens
    -   Must start with an alphabetic character
    -   Cannot be longer than 128 characters
6.  In the **User Name** field, enter a Cloud Account Management service account user name.

7.  Select **Next**.

8.  On the **Configure stack options** page, select the **I acknowledge that AWS CloudFormation might create IAM resources with custom names** check box and select **Next**.

9.  On the **Review and create** page, select **Submit** to launch your stack.

    The IAM account gets created.

10. To add security credentials for the two users created:

    1.  Select **Resources**.

    2.  Select the user name link.

    3.  In the Access Keys section, select **Create access key**.

    4.  On the **Access key best practices &amp; alternatives** page, choose the **Third-party service** option.

        You can use this access key to enable access for a third-party application or service that monitors or manages your AWS resources.

    5.  Select the **I understand the above recommendation and want to proceed to create an access key** check box and select **Next**.

    6.  Select **Create access key**.

    7.  In the **Review access keys** page, download the access key file and select **Done**.

        **Note:** Share the access key and secret key with the Terraform admin and ServiceNow AI Platform admin.


