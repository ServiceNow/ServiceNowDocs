---
title: Yokohama Patch 6 Hotfix 2
description: The Yokohama Patch 6 Hotfix 2 release contains fixes to these problems.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-08-14"
reading_time_minutes: 7
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 6 Hotfix 2

The Yokohama Patch 6 Hotfix 2 release contains fixes to these problems.

-   **Build information:**

    Build date: 08-20-2025\_0809

    Build tag: glide-yokohama-12-18-2024\_\_patch6-hotfix2-08-08-2025


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

## Fixed problem

<table id="all-other-fixes"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1917146

</td><td>

Restricted caller access \(RCAs\) for Case look up Assistant

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1928914

</td><td>

There's a RCA issue for email reply recommendation

</td><td>

The sparkle icon is missing because this RCA isn't in an allowed state.

</td><td>

 

</td></tr><tr><td>

Glide Server APIs

 PRB1921133

</td><td>

Users can't query guest voice agents due to a lack of impersonation ability in a scoped app

</td><td>

The AI Voice agent application makes a call to a platform API to retrieve guest or public voice agents. These are agents that return basic public data such as company hours, location, etc. These agents have an ACL for a guest user. However, the integration user can't impersonate a guest since the app isn't in a global scope.

</td><td>

Call into the Voice Agent app.

 Notice in the orchestrator that the public agents aren't queried correctly.

</td></tr><tr><td>

Next Experience User Menu

 PRB1926920

 [KB2442915](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2442915)

</td><td>

On instances with AI Agents, some users can't be found on the impersonation list

</td><td>

Currently, users with the **Identity type** field set to **AI Agent** are filtered out, but they must also be filtered by 'is empty'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

OneExtend

 PRB1920515

</td><td>

LLM usage domain separation application properties aren't installed by default

</td><td>

 

</td><td>

1.  Install the latest OneExtend app.
2.  Add the domain separation plugin.
3.  Verify the sys\_application \_property table.
4.  Look for domain.llm. usage.entitled.

 Notice that the property is missing, even though it's part of the repository.

</td></tr><tr><td>

OneExtend

 PRB1920527

</td><td>

Elaborate or shortened responses load on form skills when the ACL is set to Now Assist Context Menu \(NACM\) skills

</td><td>

This issue was found in Washington DC. Responses that have been elaborated or shortened appear even though they are restricted to a particular role in the NACM ACL table. The NACM skill in the skill configuration table also becomes 'inactive' by default.

</td><td>

1.  Log in to a Washington DC instance.
2.  Ensure Gen AI is setup.
3.  Activate the Resolution Notes generation skill.
4.  Navigate to the ACL table.
5.  Add a role to the NACM ACL, such as workspace\_admin.
6.  Impersonate an ITIL user.
7.  Select the text on close\_notes.
8.  Elaborate or shorten the text on close\_notes.

 Observe that elaborate and shortened responses are loading even when it's restricted to only the workspace\_admin role, and the NACM skill in the skill configuration table is 'inactive' by default.

</td></tr><tr><td>

OneExtend

 PRB1923618

</td><td>

Heap OutOfMemory error and node restart in an ITSM use case for Agentic AI Benchmark

</td><td>

This issue may be caused by the Agentic AI workload transaction allocating heap memory of over 1G.

</td><td>

1.  Run ITSM Benchmark.
2.  Test the load with 500 users on Now Assist and 150 users on the Agentic AI workload.

</td></tr><tr><td>

OneExtend

 PRB1923685

</td><td>

When executing a couple of Zoom Agents, an IllegalAccess error is thrown

</td><td>

The same issue is observed for the 'Create Meeting' Agent.

</td><td>

1.  Log in to an instance.
2.  Navigate to Virtual Agent UI.
3.  Provide the prompt, 'Please create a user &lt;user's name&gt; having an email ID as &lt;user email address&gt;. The user should be a basic user only.'

 Expected behavior: A user should be created in Zoom.

 Actual behavior: The message appears, '\{'message':'Invalid inputs for tools execution: JavaException: java.lang. SecurityException: Illegal access to package\_private script include function AIAFdihDataTypeConstants: caller not in scope sn\_aia'\}'.

</td></tr><tr><td>

OneExtend

 PRB1928470

</td><td>

Abnormal GAIC async submission duration

</td><td>

When the user calls certain code with an async request, the response time should be around 0-200 ms. However, the reponse time can be as high as five seconds because the Builder Entity cache frequently gets reclaimed.

</td><td>

1.  Enable logging sn\_ais\_assist. AISearchNA4S GeniusResultLogger .level=INFO.
2.  Run NAVA QnA flow.
3.  Look at the splunk log pattern 'AISearchNA4S GeniusResultLogger response received! duration'.

 Observe that the submission time can reach two to five seconds.

</td></tr><tr><td>

Software Asset Management

 PRB1913658

 [KB2290496](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2290496)

</td><td>

On an upgrade to Yokohama, new entitlements may get created from entitlement import errors

</td><td>

Users may observe the issue as duplicate entitlements found after an upgrade to Yokohama, or, after an upgrade to Yokohama, a number of entitlements were added that were created by 'system'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UI Field Administration

 PRB1875982

</td><td>

Now Assist Context Menu \(NACM\) isn't rendered on a few form fields on an INC form

</td><td>

After creating and activating a new skill on an **Incident form** field, the NACM isn't rendered for some fields.

</td><td>

1.  Log in to a Washington DC instance.
2.  Ensure Gen AI is set up.
3.  Navigate to **Now Assist Admin \(NAA\)** &gt; **NACM experiences**.
4.  Create a new skill configuration on the **Incident form** field.
5.  Add **Record form** fields such as **Subcategory**, **Short description**, and **Service**.
6.  Activate the skill.
7.  Open an INC record.

 Observe that the NACM sparkle isn't rendered on the form for the fields **Subcategory** and **Short description**.

</td></tr><tr><td>

UX Framework

 PRB1925967

</td><td>

Engagement Messenger isn't loading chats after upgrading to Yokohama Patch 6

</td><td>

The chat box in Engagement Messenger is blank, and loads no content. The errors occurs, 'SecurityError: Failed to read a named property 'uxfIntentLibrary' from 'Window'.

</td><td>

1.  Launch the Engagement Messenger.
2.  Select the chat box.
3.  Observe that the chat box is blank.
4.  Hop into a Yokohama instance.
5.  Navigate to Agentic Portal in a separate browser tab.
6.  Don't attempt to log in.
7.  Open up the dev console.
8.  Execute the script.
9.  Execute the code.
10. Select the chat bubble that appears after the code finishes executing.

 Expected behavior: The chat loads with content.

 Actual behavior: The chat load is blank and a security error appears in console.

</td></tr><tr><td>

Virtual Agent

 PRB1890524

</td><td>

Increase in heap utilization due to expression cache for search

</td><td>

This issue occurs from a script include expression cache from platform.

</td><td>

1.  Set up Now Assist Virtual Agent \(NAVA\) on a Yokohama instance.
2.  Perform search actions from the chat window.
3.  Notice that the expression cache is filled due to this.

 Notice that the load of 25 users on a single node for one hour for the search action performed occupies more than 500MB.

</td></tr><tr><td>

Virtual Agent

 PRB1925496

</td><td>

SQL does a table scan on the sys\_cs\_session \_binding table for auxiliary subscripting, causing high SQL time

</td><td>

Auxiliary is the only subscription timing out, and the SQL processing time is more than 500ms.

</td><td>

Launch Now Assist Virtual Agent \(NAVA\).

 Notice the processing time for the subscription when launching the chat client.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1925994

</td><td>

Engagement Messenger isn't loading chats after upgrading to Yokohama Patch 6

</td><td>

The chat box in Engagement Messenger is blank, and loads no content. The errors occurs, 'SecurityError: Failed to read a named property 'uxfIntentLibrary' from 'Window'

</td><td>

1.  Launch the Engagement Messenger.
2.  Select the chat box.
3.  Observe that the chat box is blank.
4.  Hop into a Yokohama instance.
5.  Navigate to Agentic Portal in a separate browser tab.
6.  Don't attempt to log in.
7.  Open up the dev console.
8.  Execute the script.
9.  Execute the code.
10. Select the chat bubble that appears after the code finishes executing.

 Expected behavior: The chat loads with content.

 Actual behavior: The chat load is blank and a security error appears in console.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 6 Hotfix 1](yokohama-patch-6-hf-1.md)
-   [Yokohama Patch 5](yokohama-patch-5.md)
-   [Yokohama Patch 4](yokohama-patch-4.md)
-   [Yokohama Patch 3](yokohama-patch-3.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

