---
title: Use Autonomous Engineer to implement an application
description: Use Autonomous Engineer \(powered by Build Agent\) to generate a plan from your requirements and build all work items in parallel, without creating each artifact individually. When implementing a ServiceNow product or application, Autonomous Engineer uses agent packs to give background agents product-specific domain knowledge.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/use-autonomous-engineer.html
release: brazil
topic_type: task
last_updated: "2026-09-08"
reading_time_minutes: 5
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, Autonomous Engineer, agent packs, Build Agent, implementation plan, work items, parallel execution, agile user stories, ATF tests, update set, ServiceNow Studio, plan dashboard, MCP server, application development, requirements interview, ServiceNow products]
audience: programmer
breadcrumb: [Use, Autonomous Engineer, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Use Autonomous Engineer to implement an application

Use Autonomous Engineer \(powered by Build Agent\) to generate a plan from your requirements and build all work items in parallel, without creating each artifact individually. When implementing a ServiceNow product or application, Autonomous Engineer uses agent packs to give background agents product-specific domain knowledge.

## Before you begin

**Note:** You must install the Autonomous Engineer app from the ServiceNow Store. Check your entitlements to see whether you can use Autonomous Engineer.

Role required: admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow Studio**.

2.  In the chat panel, open the mode selector and select **Autonomous Engineer**.

    \[Omitted image "ba-sns-select-plan-mode.png"\] Alt text: Autonomous Engineer option selected from the Build Agent mode drop-down.

    **Note:** Select **Autonomous Engineer** specifically to access the planning and parallel execution workflow described in this topic.

3.  Provide your requirements using one of the following methods.

    |Method|Steps|
    |------|-----|
    |Describe your requirements in plain language|Enter a description of what you plan to implement in the chat panel. Include as much detail as available. See [Example prompts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/build-agent-example-prompts.md) for some ideas.|
    |Upload a file of requirements|Attach a file, such as a CSV of user stories, to the chat panel.|

4.  Answer any interview questions that Autonomous Engineer asks to clarify your requirements.

    \[Omitted image "ba-sns-spec-questions.png"\] Alt text: Guided question asking what the app should manage, with four selectable data model options.

    Autonomous Engineer processes your requirements and searches your instance to identify existing artifacts such as tables, roles, fields, and catalog items. If anything is ambiguous or incomplete, Autonomous Engineer asks follow-up questions. For each question, select an answer option or type a response. Autonomous Engineer then generates a brief from which to draft a plan.

5.  Tell Autonomous Engineer whether you approve of the brief or want to make any changes.

    Review and update the acceptance criteria and test criteria for each work item as needed.

    Accurate acceptance criteria and test criteria improve execution quality and help Autonomous Engineer build and validate each work item correctly.

    Autonomous Engineer generates a plan with work items, and approves the work items. Work items are structured in an Agile user story format and include acceptance criteria and test criteria. They are grouped into logical sections and sequenced using a dependency graph so that each work item executes only after any items it depends on are complete.

6.  Select the plan in the chat panel to review its contents and work items in a new window.

    \[Omitted image "ba-spec-plan-generated.png"\] Alt text: Autonomous Engineer chat alongside an Employee Onboarding plan in Ready to execute status, with Review, Execute, and Finalize stages displayed.

7.  Select the **Show work items** button to review the work items in the plan.

    \[Omitted image "ba-spec-work-items.png"\] Alt text: Employee Onboarding plan with work items grouped into Application and Roles Foundation, Access Controls, and Data Model categories. For details, refer to the work items list in the surrounding text.

8.  Review each work item.

9.  Edit the content in the work item directly.

    You can edit work items using the chat panel.

    1.  Select a work item to open it.

    2.  Select the more options icon \[Omitted image "ba-spec-more-icon.png"\] Alt text:.

    3.  Select **Open record**.

        The record for the work item opens in a new browser tab.

    4.  Make any changes to the work item record and select **Update.**

    \[Omitted image "ba-spec-open-record.png"\] Alt text: Work item record in Waiting status, with the Open record button highlighted in the header area.

10. Complete any required manual steps, if the plan includes them, before you run the plan.

    Work items that depend on an incomplete manual step may fail.

11. Select the **Execute plan** button on the **Plan** tab to approve the plan and start execution.

    The **Plan** tab view becomes a dashboard where you can track the plan progress. Autonomous Engineer generates a background agent for each work item and builds all work items in parallel.

    The dashboard displays the status of each work item as it progresses. For a description of each status, see [Autonomous Engineer plan and work item states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown).

12. Monitor progress and respond to items that require your attention.

    The plan dashboard shows a count of work items by status. If a work item reaches a blocked or error state, it appears in the dashboard and a notification appears in the chat panel.

    To see more detail on a work item, open it from the dashboard or ask Autonomous Engineer in the chat panel. To retry a blocked work item after reviewing or editing it, ask Autonomous Engineer to retry that item. If you must undo changes for a specific work item, ask Autonomous Engineer to roll back that item.

    \[Omitted image "ae-work-items-dash.png"\] Alt text: Dashboard showing work item execution progress and status counts. For details, refer to the surrounding description.

13. When a work item reaches the Needs validation status, open it to verify the results and mark it complete.

    A work item in Needs validation status shows a validation section with Test Agent \(ATF\) test results and a list of the artifacts that were created. If you used an agent pack, the tests are product-specific.

    If the results look correct, select **Mark as complete**. To make changes, edit the work item content and ask Autonomous Engineer to retry.


## Result

When all work items are complete, Autonomous Engineer generates an update set for the plan. Export the update set and deploy it to your UAT or production environment.

For information on deploying update sets, see [Update sets and Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ba-update-sets.md).

**Parent Topic:**[Using Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ae-using-autonomous-engineer.md)

