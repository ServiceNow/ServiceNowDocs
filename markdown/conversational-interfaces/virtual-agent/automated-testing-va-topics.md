---
title: Automated testing for Virtual Agent topics that use NLU topic discovery
description: Automated testing for your Virtual Agent topic flows uses the ServiceNow Automated Test Framework product through Assistant Designer. You can create and run automated tests through the Automated Test Framework to confirm that your topic flow works after making a change.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/virtual-agent/automated-testing-va-topics.html
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Testing NLU/Keyword topics, Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Automated testing for Virtual Agent topics that use NLU topic discovery

Automated testing for your Virtual Agent topic flows uses the ServiceNow Automated Test Framework product through Assistant Designer. You can create and run automated tests through the Automated Test Framework to confirm that your topic flow works after making a change.

Create topic test cases through a topic's **Test** &gt; **Create test case** preview and view the topic's test cases through the Asset library's **Manage NLU/keyword test cases** button. Only run automated tests on a development, test, or other non-production instance to avoid data corruption and outage. For more information, see the [Automated Test Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/automated-test-framework-atf/automated-test-framework.md).

Working with test cases is only available if you have:

-   Installed the com.glide.cs.atf plugin \(installed as a part of the Virtual Agent chatbot plugin\).
-   Received one of the following roles: atf\_test\_designer, atf\_ws\_designer, atf\_test\_admin, virtual\_agent\_admin, or admin.
-   Published topics with one of the following topic types: **Topic**, **Setup Topic**, or **Small talk**.

-   **[Create an automated test in Virtual Agent Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/create-automated-test-vad.md)**  
Create automated tests in Virtual Agent Designer and run tests regularly against ideal conversation topic flows. You can create multiple automated tests for a topic to capture different conversation flows for various situations such as ideal conversation paths or errors.
-   **[Manage and run automated test cases in Virtual Agent Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/manage-automated-test-cases.md)**  
Run reusable test cases of your published topics using the Automated Test Framework through Virtual Agent Designer to identify performance issues and prevent regressions before production.
-   **[Handle failures caused by dynamic inputs in user testing of Virtual Agent topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/t_handle-dynamic-inputs-user-testing.md)**  
Avoid failures when performing automated tests for topics in Assistant Designer by controlling which inputs that you want to run as part of a test case.

**Parent Topic:**[Testing NLU/Keyword topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/va-designer-testing.md)

