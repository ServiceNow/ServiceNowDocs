---
title: \(Legacy\) Automated testing for Virtual Agent topics that use NLU topic discovery
description: Automated testing for your Virtual Agent topic flows uses the ServiceNow Automated Test Framework product through Assistant Designer. You can create and run automated tests through the Automated Test Framework to confirm that your topic flow works after making a change.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/automated-testing-va-topics.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Testing NLU and keyword topics, Build and deploy NLU conversations, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Automated testing for Virtual Agent topics that use NLU topic discovery

Automated testing for your Virtual Agent topic flows uses the ServiceNow Automated Test Framework product through Assistant Designer. You can create and run automated tests through the Automated Test Framework to confirm that your topic flow works after making a change.

Create topic test cases through a topic's **Test** &gt; **Create test case** preview and view the topic's test cases through the Asset library's **Manage NLU/keyword test cases** button. Only run automated tests on a development, test, or other non-production instance to avoid data corruption and outage. For more information, see the Automated Test Framework.

Working with test cases is only available if you have:

-   Installed the com.glide.cs.atf plugin \(installed as a part of the Virtual Agent chatbot plugin\).
-   Received one of the following roles: atf\_test\_designer, atf\_ws\_designer, atf\_test\_admin, virtual\_agent\_admin, or admin.
-   Published topics with one of the following topic types: **Topic**, **Setup Topic**, or **Small talk**.

-   **[\(Legacy\) Manage and run automated test cases in Virtual Agent Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/manage-automated-test-cases.md)**  
Run reusable test cases of your published topics using the Automated Test Framework through Virtual Agent Designer to identify performance issues and prevent regressions before production.
-   **[\(Legacy\) Create an automated test in Virtual Agent Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/create-automated-test-vad.md)**  
Create automated tests in Virtual Agent Designer and run tests regularly against ideal conversation topic flows. You can create multiple automated tests for a topic to capture different conversation flows for various situations such as ideal conversation paths or errors.
-   **[\(Legacy\) Handle failures caused by dynamic inputs in user testing of Virtual Agent topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/t_handle-dynamic-inputs-user-testing.md)**  
Avoid failures when performing automated tests for topics in Assistant Designer by controlling which inputs that you want to run as part of a test case.

**Parent Topic:**[\(Legacy\) Testing NLU/Keyword topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-designer-testing.md)

