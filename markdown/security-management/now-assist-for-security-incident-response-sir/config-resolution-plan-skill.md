---
title: Configure the Security incident resolution plan skill
description: Add your existing runbooks to the resolution plan generation skill. The runbooks provide additional context to the resolution plan generation skill.
locale: en-US
release: australia
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Skill configuration, configure resolution plan skill]
breadcrumb: [Configure a skill, Configure, Now Assist for Security Incident Response, Security Operations]
---

# Configure the Security incident resolution plan skill

Add your existing runbooks to the resolution plan generation skill. The runbooks provide additional context to the resolution plan generation skill.

## Before you begin

Role required: sn\_si.admin

## About this task

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

2.  In **Technology**, select **Security Operations**.

    The Now Assist skills for Security Operations page displays the list of available skills.

3.  In the Security Incident resolution plan tile, select ![More actions icon.](../../security-incident-response/image/cj-sir-flow-more-icon.png)

4.  Select **Edit**.

5.  Select **Add AI Runbooks**.

6.  In the **Additional Runbook Context** page, select **Add**.

7.  In **Condition**, enter a condition when the skill must reference the runbook.

    For example, set the condition as `If category is Phishing and affected user VIP status is true`.

8.  In **Choose KB Reference**, select a knowledge base article runbook.

9.  In **Order**, set an order of importance.

    You can set **Order** to any positive integer, a lower value indicating a higher priority.

10. Select **Save and continue**.


