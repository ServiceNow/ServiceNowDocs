---
title: Creating custom test step configurations
description: Step configuration records \(or step configs\) define how each step type behaves. You can create new step configurations that define custom steps that run on the server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/automated-test-framework-atf/atf-custom-step-types.html
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administering the Automated Test Framework \(ATF\), Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Creating custom test step configurations

Step configuration records \(or step configs\) define how each step type behaves. You can create new step configurations that define custom steps that run on the server.

When you add a step to an automated test, that step has a defined type such as Set Field Values, or Record Insert. Each step configuration has a number of characteristics that affect how steps of that type behave, including the inputs required, the actions performed, and so on.

These characteristics are defined in the step's step configuration record.

\[Omitted image "atf-architecture.png"\] Alt text: Diagram showing structure of test step records

The [Step execution script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-config-script.md) field determines the actions the system executes when a step with this config runs.

-   **[Create custom step configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-create-custom-step.md)**  
Create a custom step configuration that can form the basis of new steps that run on the server.
-   **[Create a custom step configuration category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-create-custom-category.md)**  
Create a custom step config category.

**Parent Topic:**[Administering the Automated Test Framework \(ATF\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-admin-overview.md)

**Related topics**  


[Step configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/step-configurations-module.md)

[Step execution scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-config-script.md)

