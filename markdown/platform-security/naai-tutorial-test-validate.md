---
title: Test and validate
description: Test your agent's execution and access controls, run automated evaluations, and review Guardian logs before approving the agent for production deployment.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-26"
reading_time_minutes: 2
breadcrumb: [Create and secure an AI agent in Now Assist, Agentic AI security and governance]
---

# Test and validate

Test your agent's execution and access controls, run automated evaluations, and review Guardian logs before approving the agent for production deployment.

Testing validates both that your agent performs its intended task correctly and that your security configuration works as designed. Both dimensions must pass before you deploy to production.

## Test agent execution

Use the testing playground in AI Agent Studio to run manual test executions against your agent using sample utterances. Verify that the agent completes its intended task, uses the correct tools, and handles edge cases and failure scenarios appropriately.

-   To test an AI agent execution, see [Manually test the execution of an AI agent](https://www.servicenow.com/docs/access?context=test-ai-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).
-   To test an agentic workflow execution, see [Manually test the execution of an agentic workflow](https://www.servicenow.com/docs/access?context=test-aia-use-case&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Test access controls

Verify that your ACL configuration works correctly by running access tests as different users. Confirm that users who should have access can invoke the agent, and users who should not have access cannot.

-   To test user access to an AI agent, see [Test user access to an AI agent](https://www.servicenow.com/docs/access?context=test-aia-access&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).
-   To test user access to an agentic workflow, see [Test user access to an agentic workflow](https://www.servicenow.com/docs/access?context=test-aw-access&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

If access test results are unexpected, review your ACL configuration. See [Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for details on how ACLs interact across the agent, workflow, and tool layers.

## Run automated evaluations

Automated evaluations test your agent against a dataset of expected inputs and outputs, providing consistent, repeatable quality measurements. Run evaluations after manual testing is complete to establish a performance baseline before go-live. For details on this process, see [Execute an agentic evaluation run](https://www.servicenow.com/docs/access?context=execute-aia-eval&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Important:** The user running an automated evaluation must pass the ACLs of the agent and all agents in the agentic workflow. If the user does not have the required roles, the evaluation will report an access failure rather than an agent execution failure.

## Review Guardian logs from testing

Export and review Now Assist Guardian logs from your test runs before going live. The logs show you what content Guardian detected during testing, which helps you decide whether your current blocking configuration is appropriate for production use. See .

If you see unexpected detections in the logs, adjust your Guardian configuration before proceeding. Common causes include overly broad sensitive topic filters or test utterances that trigger offensiveness detection.

## Go-live validation gate

Do not proceed to [Go live and monitor](naai-tutorial-go-live-monitor.md) until all of the following are true:

-   Agent execution tests pass for your defined use case scenarios.
-   Access control tests confirm that only intended users can invoke the agent.
-   Automated evaluations meet your defined success criteria threshold.
-   Guardian logs from testing have been reviewed and configuration is confirmed appropriate for production.

## Next step

When all validation gate criteria are met, proceed to [Go live and monitor](naai-tutorial-go-live-monitor.md).

**Parent Topic:**[Create and secure an AI agent in Now Assist](naai-tutorial-overview.md)

