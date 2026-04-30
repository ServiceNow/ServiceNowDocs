---
title: Use the knowledge check box
description: As with incidents, problems often generate information that may be needed in the future. The system can automatically submit a knowledge article when a problem is closed.
locale: en-US
release: xanadu
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Knowledge articles from problems, Communicating the outcome of a problem, Problem Management, IT Service Management]
---

# Use the knowledge check box

As with incidents, problems often generate information that may be needed in the future. The system can automatically submit a knowledge article when a problem is closed.

## Before you begin

Role required: itil

## About this task

**Note:** If you have Problem Management Best Practice — Madrid — Knowledge Integration plugin \(com.snc.best\_practice.problem.madrid.knowledge\) activated, see [Create a known error article](create-known-error-from-problem.md). The topic applies to legacy Problem \(London or a prior release\) only.

You can select the **Knowledge** check box and automatically submit a knowledge article when a problem is closed.

## Procedure

1.  Select the **Knowledge** check box on the Problem form.

2.  Resolve and close the problem.

    Closing the problem triggers the business rule **Problem Create Knowledge**. By default, the business rule creates a knowledge article in the **Draft** workflow state, ready for a knowledge team member to review and publish. The problem **Short description** becomes the article **Short description**, and the problem **Work notes** become the article **Text**.

    If the knowledge submission workflow is enabled, the problem **Work notes** become a knowledge submission instead of an article. For more information, see [Knowledge workflows](https://www.servicenow.com/docs/access?context=r_KnowledgeWorkflows&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).


**Parent Topic:**[Knowledge articles from problems](../concept/c_CreateKnowledge.md)

