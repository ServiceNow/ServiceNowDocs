---
title: Troubleshooting in Build Agent
description: Use this reference when troubleshooting build failures, empty UI pages, context limits, rate limit errors, and other common issues you may encounter when using Build Agent.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-02"
reading_time_minutes: 1
breadcrumb: [Use, Build Agent, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Troubleshooting in Build Agent

Use this reference when troubleshooting build failures, empty UI pages, context limits, rate limit errors, and other common issues you may encounter when using Build Agent.

|Issues|Description|Solution|
|------|-----------|--------|
|Build not deployed|The Build Agent only deploys the latest successful build. If your updates aren’t available after deployment, it may indicate that the build failed, even though the deployment was successful.|Check the build status and note any error messages. Paste those error messages into the chat panel and ask the Build Agent to resolve the build issues and redeploy the application.|
|Empty UI page|When working on complex UI pages, the Build Agent may occasionally display an empty page.|Open the browser console, copy the error messages, and paste them into the chat panel. Then, ask the Build Agent to fix the UI page. The Build Agent assists you in both creating and debugging your applications.|
|Context limit exceeded|If something goes wrong while creating or updating your application, you have the option to retry. The Build Agent maintains a history of your session and can resume from the point of failure. However, if your chat window exceeds the context limit, you receive a 'Context Window Exceeded' error.|Open a new chat window and describe the application you want to create once again. Although the Build Agent doesn’t retain the context from the previous chat session, it reviews the work already done and continues from where it stopped.|
|Rate limit error|Another error you might encounter is the 'Rate limit error', which happens when the LLM provider receives too many requests to handle.|Wait for a minute or two before trying again.|

**Parent Topic:**[Use Build Agent](../tasks/use-build-agent.md)

