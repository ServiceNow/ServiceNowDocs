---
title: Integration with Continual Improvement Management
description: Integrating with the ServiceNow Continual Improvement Management application enables you to create a request once you have identified an improvement opportunity.Launch Process Mining from the CIM workbench to analyze the existing process and find new opportunities for improvement.Understand how you can create or track an improvement request.
locale: en-US
release: yokohama
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integrating Process Mining, Activating Process Mining, Process Mining, Platform Analytics]
---

# Integration with Continual Improvement Management

Integrating with the ServiceNow® Continual Improvement Management application enables you to create a request once you have identified an improvement opportunity.

Integration with the ServiceNow® Continual Improvement Management \(CIM\) application enables you to request and view process improvement-related initiatives and add tasks to existing initiatives.

The Process Mining plugin \(com.sn\_po\) provides an integration between the Process Mining and Continual Improvement Management applications. Continual Improvement Management integrates with activation of the CIM \(com.sn\_cim\) plugin.

From Process Mining: When you create an improvement initiative from Process Mining, a reference to the project is added to the continual improvement record.

From Continual Improvement Management: Launch the Process Mining Analyst Workbench from CIM.

## Roles

Integration with Continual Improvement Management doesn’t add any additional roles to the Process Mining roles. To enable Continual Improvement Management features, you must add the agent\_workspace\_user role to the users who need this capability.

**Parent Topic:**[Integrating Process Mining](integrating-process-mining.md)

**Related topics**  


[Example of Continual Improvement Management using Process Mining](integrate-with-continuous-i.md#)

[Continual Improvement Management](https://www.servicenow.com/docs/access?context=cim-landing-page&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)

[Request Continual Improvement Management](https://www.servicenow.com/docs/access?context=request-cim&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)

## Launch Process Mining from CIM

Launch Process Mining from the CIM workbench to analyze the existing process and find new opportunities for improvement.

### Before you begin

Role required: improvement\_manager

Activate the Continual Improvement Management plugin \(com.sn\_cim\) and the Process Mining plugin \(com.sn\_po\).

### Procedure

1.  Navigate to the **Process Mining** workbench in any one of the following ways.

<table id="choicetable_ywf_lnh_nlb"><thead><tr><th align="left" id="d89920e224">

From where

</th><th align="left" id="d89920e227">

Steps

</th></tr></thead><tbody><tr><td id="d89920e233">

**Continual Improvement Workbench**

</td><td>

1.  Navigate to **Continual Improvement** &gt; **Workbench**.
2.  On the **Continual Improvement Workbench** page header, select **Go to****Process Mining**.
3.  Analyze the existing project or create a new Process Mining project definition for assessment.

**Note:** For more information, refer to [Create a project or template using Project Builder](../task/define-workflow-model.md).

</td></tr><tr><td id="d89920e284">

**Improvement Initiative**

</td><td>

1.  Navigate to **Continual Improvement** &gt; **All**.
2.  Open a record.
3.  Select the **Go to Process Mining** related links.


</td></tr></tbody>
</table>
## Example of Continual Improvement Management using Process Mining

Understand how you can create or track an improvement request.

As an improvement manager, you use your Continual Improvement Management Workbench dashboard daily to view operational work and initiatives in progress. You have an open initiative to optimize the incident process and reduce mean time to resolve \(MTTR\).

From the initiative form, you select **Go to Process Mining**. The action navigates you to a generated project in the Process Mining Analyst Workbench showing cases that were closed in the last three months.

Make Continual Improvement part of your routine through integration with Process Mining

