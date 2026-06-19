---
title: Activate Now Assist for CSM Major Issue Management
description: Activate the AI skill, test it against your data, then activate the agentic workflow to begin AI-assisted major case detection on new cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/activate-na-csm-major-issue-management.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2026-06-02"
reading_time_minutes: 2
breadcrumb: [Configure Now Assist for CSM Major Issue Management, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Activate Now Assist for CSM Major Issue Management

Activate the AI skill, test it against your data, then activate the agentic workflow to begin AI-assisted major case detection on new cases.

## Before you begin

Role required: admin

-   The `com.sn_csm_mim_gen_ai` plugin must be installed
-   The Major Issue Management \(com.sn\_majorissue\_mgt\) application must be installed \(provides the `suggested_major_case` field and major issue management lifecycle\)

## About this task

This procedure has three stages. Complete all three before AI detection takes effect on production cases.

## Procedure

1.  Activate the **Major Cases Similarity Search** Now Assist skill.

    1.  Navigate to **Now Assist Admin** &gt; **Now Assist Skills** &gt; **Customer** &gt; **CSM** &gt; **Major Cases Similarity Search**.

    2.  Select **Activate Skill**.

    3.  Turn on the **Flow Action** display setting.

        **Important:** The flow action display must be enabled. If it is not, the skill can't be invoked from the **Major case agentic workflow** flow.

    4.  Confirm that the access roles include the defaults.

        The following roles are granted execute access on the skill by default:

        -   `sn_customerservice_agent`
        -   `sn_customerservice.consumer_agent`
        -   `sn_customerservice.consumer`
        -   `sn_customerservice.customer`
2.  Test the skill with your data before activating the workflow.

    1.  In the **Now Assist for CSM Major Issue Management** scope, navigate to **Now Assist Skill Kit** &gt; **Home** &gt; **ServiceNow skills** &gt; **Major Cases Similarity Search**.

    2.  Select **Run Test**.

    3.  Use the default test values, then verify the results returned against both the major case profile and the non-major case profile.

        Running the test against representative cases in your environment helps validate that the OOB similarity thresholds and search profiles return appropriate matches before live cases are evaluated.

3.  Activate the **Major case agentic workflow** flow.

    1.  Navigate to **Flow Designer** &gt; **Flows** and search for **Major case agentic workflow**.

    2.  Open the flow and review the default trigger.

        The default trigger is: **Case Created where Priority is 1 - Critical, or Priority is 2 - High; and Parent is empty**.

        The flow is delivered with a single action, **Search similar major case**, which calls the sub-flow that runs the AI skill and updates the case.

    3.  Edit the trigger conditions to further restrict which cases run through detection.

        You can add filter conditions such as category, account, product, or any other case field. More restrictive triggers reduce the number of AI skill executions, which lowers cost and load.

    4.  Select **Activate** on the flow.

4.  Adjust detection behavior by changing the configuration properties.

    The defaults work for most environments. To adjust thresholds, search profiles, or match fields, extend the extension point implementation.


## Result

The AI detection runs automatically on each newly created case that matches the flow's trigger conditions. The workflow either links the case to an existing major case or proposes a new major case for review. If there are no cases that match, or a major case is not required, no action is taken.

## What to do next

[Now Assist for CSM Major Issue Management Properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/na-for-csm-mim-properties.md)

