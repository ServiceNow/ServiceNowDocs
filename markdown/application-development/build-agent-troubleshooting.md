---
title: Common issues and solutions in Build Agent
description: Identify and resolve common issues in Build Agent. Use this reference alongside the general debugging approach to identify and fix problems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/build-agent-troubleshooting.html
release: zurich
topic_type: reference
last_updated: "2026-05-07"
reading_time_minutes: 5
keywords: [troubleshooting, build failures, empty UI pages, context limits, rate limit errors, deployment issues, debugging, error messages, Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Build Agent, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Common issues and solutions in Build Agent

Identify and resolve common issues in Build Agent. Use this reference alongside the general debugging approach to identify and fix problems.

## General debugging approach

When something goes wrong, paste the exact error message into the Build Agent chat. Build Agent can often diagnose and fix the issue directly. If not, the error message is your starting point for debugging.

If you attempt several fixes in the same conversation without progress, use a structured approach before starting a new chat.

**Tip:**

Use the following prompt to structure your debugging session:

`I'm seeing this error: [paste exact error]. This happens when: [describe scenario]. Before suggesting fixes: 1) Help me reproduce this consistently. 2) Review the debugger output and logs. 3) Check for access or configuration issues. 4) Examine if this is a known issue.`

Then test hypotheses from simplest to most complex:

-   Is this an access or role issue?
-   Is this a configuration problem?
-   Is this a naming convention mismatch?
-   Is this a logic edge case?

If structured investigation does not resolve the issue within a few attempts, start a fresh conversation with a more specific prompt.

Save any debugging information to convey if you need to contact Now Support.

## Issues and solutions

<table id="table_zgy_pfl_kgc"><thead><tr><th>

Issue

</th><th>

Resolution

</th></tr></thead><tbody><tr><td>

Now Assist panel not visible

</td><td>

-   Quick check: Required plugins are installed and your user has the right roles. The ServiceNow IDE needs the admin role plus the documented Build Agent plugins \(`sn_glider` and `sn_build_agent` for Trial; `sn_now_creator` for Paid\). In ServiceNow Studio, confirm you're on a supported release.
-   Try: Refresh the page or sign out and back in.
-   If still failing, capture: The exact error or behavior, your release, and the role list on your user.

</td></tr><tr><td>

Build Agent unresponsive

</td><td>

-   Quick check: Browser cache and the active session.
-   Try: Clear the cache, try a different browser, and check the ServiceNow status page for service announcements.
-   If still failing, capture: The request that hung, your browser version, and the ServiceNow status state.

</td></tr><tr><td>

Scope or name conflict

</td><td>

-   Quick check: Whether the scope or app name is already in use on the instance.
-   Try: Let Build Agent self-correct with a unique scope, or pick a new name and try again.
-   If still failing, capture: The conflicting scope or app name and the action that triggered it.

</td></tr><tr><td>

Stuck in error loop

</td><td>

-   Quick check: How many fixes Build Agent has attempted on the same symptom.
-   Try: Use Git checkpoints or update set rollback to revert, then start a fresh conversation that names the specific error.
-   If still failing, capture: The exact error text, recent commits, and a brief description of what you were trying to accomplish.

</td></tr><tr><td>

App not deploying

</td><td>

-   Quick check: Build output for errors before deploying. Build Agent only deploys the latest successful build. If your updates are not available after deployment, the build may have failed even though the deployment succeeded.
-   Try: In the ServiceNow IDE, run ServiceNow SDK build first, check errors, then deploy and install in sequence. In ServiceNow Studio, confirm your update set is current and complete. Paste any error messages into the chat panel and ask Build Agent to resolve the build issues and redeploy. For more information, see [Deploying what you built with Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/build-agent-deployment.md).
-   If still failing, capture: The build log, your SDK version, and your update set state.

</td></tr><tr><td>

Empty UI page

</td><td>

-   Quick check: The browser console for errors.
-   Try: Open the browser console, copy the error messages, paste them into the chat panel, and ask Build Agent to fix the UI page.
-   If still failing, capture: The full browser console output and the prompt that produced the empty page.

</td></tr><tr><td>

Context limit exceeded

</td><td>

-   Quick check: Whether you have received a `Context Window Exceeded` error. Build Agent maintains a history of your session and can resume from the point of failure, but has a context limit.
-   Try: Open a new chat window and describe the application again. Build Agent does not retain context from the previous session, but it reviews the work already done and continues from where it stopped.
-   If still failing, capture: The last prompt before the error and a summary of what had been built.

</td></tr><tr><td>

Out of prompts

</td><td>

-   Quick check: Your remaining prompt count for the current 30-day cycle.
-   Try: Wait for the cycle to reset, or upgrade to Now Assist for Creator. Plan approvals do not count against your prompt allotment; only submitted prompts do.
-   If still failing, capture: Your entitlement state and the cycle reset date.

</td></tr><tr><td>

Rate limit error

</td><td>

-   Quick check: Whether the model provider is receiving too many requests.
-   Try: Wait a minute or two before trying again.
-   If still failing, capture: The exact error message and the time it occurred.

</td></tr><tr><td>

Unsupported configuration

</td><td>

-   Quick check: Whether the requested metadata or feature is in the supported list.
-   Try: Complete that step directly on the platform, then continue with Build Agent for everything else.
-   If still failing, capture: The configuration you needed and the workaround you used.

</td></tr><tr><td>

Missing dependencies \(IDE\)

</td><td>

-   Quick check: `package.json` for the entries Build Agent referenced.
-   Try: Let Build Agent self-correct first. If that does not resolve it, add the package manually and run `npm install`.
-   If still failing, capture: The missing module name and the install error output.

</td></tr><tr><td>

Long-running prompt times out

</td><td>

-   Quick check: Your session timeout setting.
-   Try: For labs and workshops, set **glide.ui.session\_timeout** to `1440` in sys\_properties. Coordinate with the platform admin on a shared instance before changing it.
-   If still failing, capture: The session length and the prompt that timed out.

</td></tr></tbody>
</table>**Parent Topic:**[Use Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/use-build-agent.md)

