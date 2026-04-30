---
title: About Amazon Web Services API permissions
description: Cloud Account Management interacts with Amazon Web Services to create and manage subscription accounts.
locale: en-US
release: zurich
product: Cloud Account Management
classification: cloud-account-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Amazon Web Services API permissions Cloud Workspace, Amazon Web Services API permissions CW]
breadcrumb: [Explore, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# About Amazon Web Services API permissions

Cloud Account Management interacts with Amazon Web Services to create and manage subscription accounts.

**Note:** You must establish an AWS service account for Cloud Account Management that is separate from the account for Cloud Discovery.

The following API permissions are required to start a new subscription account in AWS:

-   budgets: CreateBudgetAction
-   budgets: DescribeBudgetAction
-   budgets: ModifyBudget
-   budgets: ViewBudget
-   organizations: AttachPolicy
-   organizations: CreateAccount
-   organizations: CloseAccount
-   organizations: DescribeAccount
-   organizations: DescribePolicy
-   organizations: DescribeOrganization
-   organizations: DescribeOrganizationalUnit
-   organizations: DescribeCreateAccountStatus
-   organizations: ListRoots
-   organizations: ListAccounts
-   organizations: ListTagsForResource
-   organizations: ListAWSServiceAccessForOrganization",
-   organizations: ListAccounts
-   organizations: ListParents
-   organizations: ListOrganizationalUnitsForParent
-   organizations: MoveAccount
-   organizations: TagResource
-   iam: GetAccountSummary
-   sts: AssumeRole

**Note:**

For more details on API permissions, download the [Cloud Discovery REST API permissions spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can research and grant the user permissions required for running the discovery process.

