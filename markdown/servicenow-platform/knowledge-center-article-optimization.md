---
title: Knowledge Center Article Optimization
description: Article Optimization is an automated system that improves the quality and health of knowledge articles by providing actionable feedback to authors and managers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/knowledge-center-article-optimization.html
release: zurich
topic_type: concept
last_updated: "2026-07-20"
reading_time_minutes: 1
breadcrumb: [Exploring Knowledge Center, Knowledge Center, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Knowledge Center Article Optimization

Article Optimization is an automated system that improves the quality and health of knowledge articles by providing actionable feedback to authors and managers.

The Article Optimization tool scans your knowledge articles and provides instant, actionable feedback. It helps you quickly address issues, resulting in high-quality content that is more accessible and discoverable. By streamlining improvements, the tool helps confirm that your articles meet accessibility and searchability standards, saving time and improving the user experience.

**Note:** Your administrator or manager can configure the Article Optimization features to enable and customize a range of operations. For more information, see [Configuring custom script based Article Optimization scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown).

The Article Optimization tool performs the following operations:

-   Scheduled jobs run various scans on articles, such as checking for proper heading tags, missing image alt attributes \(for accessibility\), and title relevance \(for search engine optimization\).
-   Findings from these scans are presented as cards in the user interface, offering suggestions like adding alt text or updating titles.
-   Both script-based and AI-powered scans are supported. AI scans include suggestions for improvement.
-   Authors can fix, ignore, or review findings directly from the UI. Some fixes \(changing heading tags, and so on\) can be batch-applied.
-   Managers can see aggregated findings on the home page, such as number of flagged articles and types of issues. Authors can see findings at the individual article level.
-   Use the article length scan, a script-based, non-AI scan, to evaluate articles against two length-based criteria: minimum length for search engine optimization, and maximum length for AI search. Articles with fewer than 300 words are flagged for search engine optimization and don't appear in search results. Articles exceeding 10,000 words are flagged for AI search indexation and don't appear in AI-powered search results.
-   The Reading Ease scan flags readability issues in articles. Review and resolve the findings to improve articles that score below the threshold.

