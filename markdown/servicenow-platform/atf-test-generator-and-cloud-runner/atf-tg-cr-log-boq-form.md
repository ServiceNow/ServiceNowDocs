---
title: Log entries in the BOQ form
description: Debug errors or track any critical transactions during the execution of the test suites, setting up the Cloud Runner or generating the tests by viewing the log entries in the BOQ form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/atf-test-generator-and-cloud-runner/atf-tg-cr-log-boq-form.html
release: zurich
product: ATF Test Generator and Cloud Runner
classification: atf-test-generator-and-cloud-runner
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, ATF Test Generator and Cloud Runner, Extend ServiceNow AI Platform capabilities]
---

# Log entries in the BOQ form

Debug errors or track any critical transactions during the execution of the test suites, setting up the Cloud Runner or generating the tests by viewing the log entries in the BOQ form.

You can now view important log entries in the BOQ form. When you go to the BOQ table, you will see the list of jobs. On entering one of the jobs, you will see some specific job log entries.

The following are some of the examples for log entries in the BOQ form for test execution.

-   Successful test run\[Omitted image "atf-tg-cr-successful-run-boq.png"\] Alt text: Image showing successful test run

    **Note:** Select See generated tests related link to view the automated tests. The list of generated tests shows up and is not editable. You can also view the state and the reasons of failure of the tests on the list. The See generated tests related link is visible for all the log entries in the BOQ form examples. \[Omitted image "atf-tg-cr-generated-tests.png"\] Alt text: Generated Tests list.

-   Test run got cancelled by user via root tracker\[Omitted image "atf-app-test-run-canceled.png"\] Alt text: Image showing canceled test run
-   If BOQ and BOS can be reached on an instance, but login is redirected.\[Omitted image "atf-app-login-redirected.png"\] Alt text: Image showing login redirected case

    **Note:** This might happen when the ADCv2 load balancer of the instance is misconfigured and you have a customization that redirects traffic via a client side script.

    \(the ADCv2 load balancer of the instance is misconfigured, the customer has a customization that redirects traffic via a client side script, etc…\)

-   If you have deleted an API key before the job is sent to BOS/BOQ\[Omitted image "atf-app-api-key-deleted.png"\] Alt text: Image showing API key deleted case
-   If the BOS is unable to login to an instance due to some client side script, API key being deleted after request has been sent to BOS/BOQ, etc.\[Omitted image "atf-app-unable-login.png"\] Alt text: Image showing unable to login case

**Parent Topic:**[ATF Test Generator and Cloud Runner reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/atf-test-generator-and-cloud-runner/atf-tg-cr-ref.md)

