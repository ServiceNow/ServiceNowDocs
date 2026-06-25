---
title: Configure the contract request form header for your workspace
description: As an administrator, configure the header of the contract request form for your workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-configure-header.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Contract request header, BU configuration]
breadcrumb: [Configure CM Pro for your workspace, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Configure the contract request form header for your workspace

As an administrator, configure the header of the contract request form for your workspace.

## Before you begin

Role required: admin

## About this task

The form header contains a primary field and secondary fields. You can add your workspace to the base system form header tables to specify the fields that appear in a contract request header for your workspace.

\[Omitted image "cmpro-cntrct-form-head.png"\] Alt text: Contract request form header displaying the configured fields

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Configuration Settings** &gt; **UX Form Header**.

2.  In the **Table** column, select the UX Form Header tables related to the contract form.

    |Contract request form fields|Table|
    |----------------------------|-----|
    |**Short description, Priority, Contract state, Parent record, Contract status, and Signature type.**|sn\_cm\_core\_contract\_request|
    |**Participant name**|sn\_cm\_core\_signer\_task|
    |**Name of the document, requester of the contract request, latest version of the document, storage details and the folder where the document is stored**|sn\_cm\_core\_document and select it.|

3.  Select the **UX Header Configurations** tab.

4.  Select **Edit**.

5.  Select your workspace from the Available list and move it to the Selected list.

6.  Select **Save**.

7.  Select **Update**.


**Parent Topic:**[Add and configure contract request functionality into your workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-uptake-steps.md)

**Related topics**  


[Configure non-task tables for contract templates]()

[Add a workspace action button for initiating a contract request]()

[Add Contract requests tab to the contract request record]()

[Add amendment tabs to contract repository record]()

[Add Contract documents tab to the contract repository record]()

[Copy fields from parent request to contract request]()

[Group contract documents by contract type in a contract request]()

[Add access to obligation management from contract repository records]()

[Assign a role for configuring template mappings]()

[Enable contract request fields in condition builders]()

[Configuring the Playbook tab on contract repository records]()

