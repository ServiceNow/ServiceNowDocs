---
title: Setting up test definitions
description: Define tests for a particular service type, product model, or inventory to troubleshoot the service-related problems.
locale: en-US
release: xanadu
product: Customer Service Problem Management
classification: customer-service-problem-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Customer Service Problem Management, Customer Service Problem Management]
---

# Setting up test definitions

Define tests for a particular service type, product model, or inventory to troubleshoot the service-related problems.

Test definition includes characteristics, relationships, test measures definitions, measure consequences, and threshold rules. These entities enable the system to trigger relevant tests for the service problem that help to identify the root-cause of the problem. You can define these entities for each test based on your requirements.

A service test definition outlines the parameters to be configured and the metrics to be measured for a given service test. These parameters are defined in the test definition. They can be set during execution to run the tests that measures the service problem effectively. This structured approach confirms that the test is done correctly and collects all the data needed to identify the problem of the service.

-   **[Create a test definition](../task/create-test-specification.md)**  
Create a test definition to define tests that can help troubleshoot a problem encountered by a particular type of service or product model. For example, use a speed test to troubleshoot the internet-related issues.
-   **[Define a characteristic for the test definition](../task/add-characterisitc-for-test-specification.md)**  
Add a characteristic for a test to determine the properties that are required to run and evaluate the test.
-   **[Define the relationship between the test definitions](../task/define-test-spec-relationship.md)**  
Define relationships for a test definition to connect and associate it with other test specifications. This process ensures comprehensive testing coverage and that the tests are aligned with the testing goals.
-   **[Define the relationship between test definition and specifications or product model](../task/specification-to-test-definition.md)**  
Establish a relationship between test definitions and their respective specifications or product model to determine the tests that must be executed for a given inventory. This relationship ensures that the appropriate tests are identified and executed based on the defined specifications. Without this association, the system can’t accurately assign the necessary tests for each inventory item.
-   **[Define test measure definitions for a service test](../task/define-test-measure-spm.md)**  
Define unique test metrics, such as parameters and criteria to run the test on a given service during testing. These metrics help promote that the service meets the desired standards and requirements to provide a satisfactory user experience.
-   **[Define threshold rules for a test measure definition](../task/define-threshold-rules.md)**  
Set rules or criteria to evaluate the results of test measures. These rules establish thresholds that determine the acceptable performance and quality metrics for a service under evaluation. If test measure results exceed or fall below these thresholds, it indicates a deviation from expected performance levels.
-   **[Define measure consequences for the threshold rules](../task/define-threshold-consequences-spm.md)**  
Set actions or responses to trigger when the test measure results fall outside the predefined acceptable limits.
-   **[Publish test definitions](../task/publish-test-specification-spm.md)**  
Publish the test definitions to ensure that agents only see the approved versions of test definitions for execution. This also helps maintain consistency and control over both current and future test versions.

**Parent Topic:**[Configuring Customer Service Problem Management](configuring-spm.md)

