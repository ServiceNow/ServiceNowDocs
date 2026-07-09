---
title: Enable signatory roles
description: Activate a system property to display the Role field when configuring internal signatory rules and when adding signatories to a contract request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-enable-signatory-roles.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-06-24"
reading_time_minutes: 2
keywords: [signatory role, system property, enable signatory roles]
breadcrumb: [Configure additional features in CM Pro, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Enable signatory roles

Activate a system property to display the **Role** field when configuring internal signatory rules and when adding signatories to a contract request.

## Before you begin

Docusign starting with version 4.4.3 must be configured Docusign as your electronic signature provider. For more information, see [Set up Docusign eSignature spoke using authorization code grant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/setup-docusign-authorization-code.md).

Role required: admin

## About this task

**Note:** This property applies only to contracts using the Docusign electronic signature provider. Signatory roles are not available for Adobe Acrobat Sign integrations.

## Procedure

1.  In the filter navigator, enter `sys_properties.list`.

2.  In the **Name** column, search for the **sn\_cm\_core.enable\_docusign\_signature\_roles** property.

3.  Select the property.

4.  Update the **Value** field to `true`.

5.  Select **Update**.


## Result

The **Role** field is displayed when configuring internal signatory rules and the **Signatory Role** field is displayed when adding signatories in Employee Center and in Contract Workspace. For more information about signatory roles, see [Signatory roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-signatory-roles.md).

**Parent Topic:**[Configure additional features in Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-additional-feature.md)

**Related topics**  


[Configuring Contract Workspace]()

[Configure signature pause duration when modifying signatories]()

[Auto-populate the start date and end date for contract requests]()

[Activate a system property to generate a certificate of completion]()

[Enable users to view email details in activity stream]()

[Enable keyword search for contract templates]()

[Configuring contract summarization for Contract Management Pro]()

[Configure conditions to send reminder notifications for expiring contracts]()

[Copy fields from parent request to amendment request]()

[Manage notifications in Contract Management Pro]()

