---
title: Go live and monitor
description: Deploy your agent to production, activate analytics and monitoring, and establish the ongoing review cadence that keeps your agent performing securely over time.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-26"
reading_time_minutes: 2
breadcrumb: [Create and secure an AI agent in Now Assist, Agentic AI security and governance]
---

# Go live and monitor

Deploy your agent to production, activate analytics and monitoring, and establish the ongoing review cadence that keeps your agent performing securely over time.

Deploying to production is not the end of the process — it is the beginning of an ongoing monitoring and improvement cycle. Set up your monitoring before you go live so that you have a performance baseline from the first day of production operation.

## Deploy to production

Before deploying, confirm that all Phase 5 validation gate criteria have been met and that any required organizational approvals \(security review, AI governance sign-off\) have been obtained.

When deploying, verify that all roles, ACLs, user identity configurations, Guardian settings, and privacy policies from your non-production build are correctly replicated in your production instance. Access control and Guardian configuration does not transfer automatically in all deployment scenarios.

## Activate analytics and monitoring

Set up the following monitoring capabilities on the day of go-live:

-   **Now Assist Analytics**

    Monitor overall usage, performance, and adoption of your Now Assist skills and AI agents. See [Analyzing Now Assist performance](https://www.servicenow.com/docs/access?context=now-assist-analytics&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

-   **AI Agent Analytics dashboard**

    Track AI agent use, efficiency gain, time to resolution, and task closure trends specific to your deployed agents. See [AI Agent Analytics dashboard](https://www.servicenow.com/docs/access?context=ai-agent-dashboard&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

-   **Now Assist Guardian analytics**

    Monitor guardrail performance to track how often offensive content, prompt injection attempts, and sensitive subject detections occur in production. See [Now Assist Guardian analytics](https://www.servicenow.com/docs/access?context=now-assist-guardian-analytics&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).


## Establish your baseline

Record your initial production metrics against the success criteria you defined in Phase 2. Your baseline measurements during the first week of production operation give you the reference point for all future optimization decisions.

At minimum, record the following from day one:

-   Agent execution volume \(number of invocations\).
-   Task closure and deflection rate.
-   Guardian detection counts by category \(offensive, prompt injection, sensitive topics\).
-   Any access control failures surfaced in logs.

## Ongoing monitoring and review

Schedule the following recurring activities to keep your agent performing securely:

-   **Regular Guardian log review**

    Export and review Now Assist Guardian logs on a regular schedule to identify emerging patterns in detected content. See . Increasing detection rates may indicate that your agent is being targeted or that your prompts need refinement.

-   **Access control audit**

    Periodically review who holds the roles that can invoke your agents, and confirm that role masking configurations still reflect least-privilege intent as your organization's roles and team structure evolve.

-   **Performance review**

    Review your agent's performance metrics against your baseline and success criteria. Use the AI Agent Analytics dashboard and Now Assist Analytics to identify trends and determine whether prompt refinement or configuration changes are needed.


**Parent Topic:**[Create and secure an AI agent in Now Assist](naai-tutorial-overview.md)

