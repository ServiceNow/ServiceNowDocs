---
title: Configure case digests
description: The case digests feature enables you to provide periodic updates and resolution information about high priority customer service cases to customers and internal stakeholders.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure case management, Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Configure case digests

The case digests feature enables you to provide periodic updates and resolution information about high priority customer service cases to customers and internal stakeholders.

## Before you begin

Role required: admin

## About this task

The case digests feature includes two types of case communication:

-   **Case action summary**: While a case is in progress, agents can send periodic case updates that describe actions taken, next steps, and other case-related information.
-   **Post case review**: When the work on a case has been completed, agents can a post a case review document that captures details about the issue, such as the root cause, mitigation plan, and preventive actions.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Guided Setup**.

2.  On the Getting Started page of the guided setup, select **Get Started**

3.  In the Case Management category, view the list of tasks to configure the feature.

<table id="table_pz1_qqv_llb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activate Case Digests

</td><td>

Activate the Case Digests \(com.sn\_csm\_case\_digest\) plugin.

</td></tr><tr><td>

Create Assignment Rules

</td><td>

Assignment rules automatically assign tasks to users and groups when the rule conditions are met. Two rules are provided with the case digests feature that assigns the post case review and case action summary records to the case agent:-   Auto- assign the CAS to case agent
-   Auto- assign the PCR to case agent
 For more information, see [Case action summary and post case review assignment rules](../reference/case-digests-assignment-rules.md).

</td></tr><tr><td>

Create Approval Workflows

</td><td>

The case digests feature includes one approval workflow that triggers the approval process for post case reviews. This workflow provides a one-step process that obtains a list of approvers from the **Approval group** and **Approval users** fields on the Post Case Review form.

</td></tr><tr><td>

Create Document Templates

</td><td>

Document templates identify, organize, and format the content from the case digest record that is included in generated documents. Two document templates are provided with the case digests feature, one for post case reviews and one for case action summaries.

</td></tr><tr><td>

Create a Case Digest Configuration

</td><td>

Case digest configurations handle different types of case review processes based on business needs.

</td></tr><tr><td>

Create Mapping for Case Types

</td><td>

Create the mapping that identifies the case type fields that are copied to post case reviews and case action summaries.

</td></tr></tbody>
</table>4.  To perform a task, select **Configure**.

    This button opens the page in your instance where the configuration is completed.


**Related topics**  


[Customer Service case digests](../concept/customer-service-case-digests.md)

